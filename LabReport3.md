# Lab Report 3 - Bugs and Commands (Week 5)
## Part 1 - Bugs
1. Failure-Inducing Input<br>
`@Test`<br>
   `public void testReverseInPlace2() {`<br>
    `int[] input2 = {1, 2, 3, 4};`<br>
    `ArrayExamples.reverseInPlace(input2);`<br>
    `assertArrayEquals(new int[]{4, 3, 2, 1}, input2);`<br>
	`}`
2. Non-Failure-Inducing Input<br>
`@Test` <br>
 `public void testReverseInPlace() {`<br>
    `int[] input1 = { 3 };`<br>
    `ArrayExamples.reverseInPlace(input1);`<br>
    `assertArrayEquals(new int[]{ 3 }, input1);`<br>
	`}`
4. Symptoms<br>
5. Bug (Before & After)<br>
   Before:<br>
     `static void reverseInPlace(int[] arr) {`<br>
    `for(int i = 0; i < arr.length; i += 1) {`<br>
     `arr[i] = arr[arr.length - i - 1];`<br>
    `}}`<br>
   After:<br>
    `static void reverseInPlace(int[] arr) {`<br>
    `int temp;`<br>
    `for(int i = 0; i < arr.length/2; i += 1) {`<br>
      `temp = arr[i];`<br>
      `arr[i] = arr[arr.length - i - 1];`<br>
      `arr[arr.length - i - 1] = temp;`<br>
    `}}`<br>
7. The Fix Explained<br>
   The bugged code (BEFORE) tried to traverse through the array and directly replace values at indexes with the values on the corresponding indexes at the other end, hence trying to reverse the array. However, it failed to realize that when the first few index values are replaced with new values, we lose the values that were initially stored there, that can no longer be retrieved and used to replace the latter part of the array. The reverseInPlace code that I fixed (AFTER) introduced a `temp` variable that stored the index's initial values before replacing them with new values. This way, we don't lose the initial values, and can therefore replace the reverse index values with the stored values.  
## Part 2 - Researching Commands
