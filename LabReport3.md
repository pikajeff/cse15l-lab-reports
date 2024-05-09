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
### Command Chosen: grep
1. `grep -i` : case-insensitive search<br>
a.
   `grep -i "cardiovascular" 1468-6708-3-1.txt`<br>
        `trials to detect survival differences or cardiovascular`<br>
          `Study design: The Cardiovascular Health`<br>
          `The Cardiovascular Health Study (CHS) is a`<br>
          `cardiovascular disease (prevalent heart disease,`<br>
        `CHS Cardiovascular Health Study`<br>
	This is useful when I want to look for all the lines that contain the work "cardiovascular" regardless of whether characters are uppercase or lowercase.<br>
b.

3. `grep -l` : restricts search to filenames
   a. `$ grep -l "dna" *.txt`<br>
`1471-2091-2-13.txt`<br>
`1471-2105-3-6.txt`<br>
`1471-213X-1-9.txt`<br>
`1471-2180-1-12.txt`<br>
`1471-2180-3-10.txt`<br>
`1471-2180-3-13.txt`<br>
`gb-2001-2-12-research0054.txt`<br>
`gb-2002-3-3-research0012.txt`<br>
`gb-2002-4-1-r2.txt`<br>
This specific command helps the user look for the files where dna is a subject, and not each specific linw. This can be useful as the user may want to read files about dna, and isnt looking for every instance of it.<br>

   b.
   `$ grep -l "2005" *.txt`<br>
`journal.pbio.0020028.txt`<br>
`journal.pbio.0020161.txt`<br>
`journal.pbio.0030056.txt`<br>
`pmed.0020016.txt`<br>
`pmed.0020023.txt`<br>
`pmed.0020039.txt`<br>
`pmed.0020061.txt`<br>
`pmed.0020067.txt`<br>
`pmed.0020158.txt`<br>
`pmed.0020160.txt`<br>
`pmed.0020208.txt`<br>
`pmed.0020209.txt`<br>
`pmed.0020210.txt`<br>
`pmed.0020216.txt`<br>
`pmed.0020278.txt`<br>
`pmed.0020281.txt`<br>
This command is useful in this scenario because the user can look for files that correspond to a specific timeframe, such as articles from the year "2005", in this specific scenario.
5. `grep -n` : shows the exact line numbers of search
   a.
   `$ grep -n "Gonzalez" chapter-1.txt`<br>
`78:    At 8:21, one of the American employees receiving Ong's call in North Carolina...`<br>
`86:    At 8:38, Ong told Gonzalez that the plane was flying erratically again`<br>
`92:    At 8:44, Gonzalez reported losing phone contact with Ong.`<br>
I have cut short the descriptions due to space restrictions, but this command could be very useful in situations where the chronological order of things matter, like in this case where we can see the exact lines in the 911report where Gonzalez is in communication with others, and the number of events that have passed in between.<br>
   b.
   
7. `grep -r` : recursively searches through directories
   a.
   `$ grep -r "President"`<br>
`About_LSC/Comments_on_semiannual.txt:President of the United States with the advice and consent of the`<br>
`Env_Prot_Agen/final.txt:III. Health and Environmental Benefits of the President's`<br>
`Media/Barnes_new_job.txt:our national creed. I, for one, will not forget President Bush's`<br>
`Post_Rate_Comm/Gleiman_EMASpeech.txt:Kappel Commission---appointed by the President to study the future`<br>
Again, I have cut down the output significantly, however, this shows how I use the `grep -r` command for a directory such as `government` with numerous subdirectories to look for specific words recursively.<br>
   b.
   
   
