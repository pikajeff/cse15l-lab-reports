# Lab Report 3 - Bugs and Commands (Week 5)
## Part 1 - Bugs
1. Failure-Inducing Input<br>
`  @Test`<br>
   `public void testReverseInPlace() {`<br>
    `int[] input = {1, 2, 3, 4};`<br>
    `ArrayExamples.reverseInPlace(input);`<br>
    `assertArrayEquals(new int[]{4, 3, 2, 1}, input);`<br>
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
6. The Fix Explained
## Part 2 - Researching Commands
