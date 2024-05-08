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
4. Symptoms
5. Bug (Before & After)
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
7. The Fix Explained
## Part 2 - Researching Commands
