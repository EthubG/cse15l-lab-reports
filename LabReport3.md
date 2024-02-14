# Lab Report 3

## Part 1

Buggy Program Code: I chose the `reversed` method in `ArrayExamples.java`.

1. A failure-inducing input for the buggy program:
```
@Test
public void goodTestReversed() {
  int[] input1 = { 1, 2, 3 };
  assertArrayEquals(new int[]{ 3, 2, 1 }, ArrayExamples.reversed(input1));
}
```

2. An input that doesn't induce a failure:
```
@Test
public void badTestReversed() {
  int[] input1 = { };
  assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
}
```

3. The symptom, as the output of running the tests:
![image one](https://github.com/EthubG/cse15l-lab-reports/blob/main/Screen%20Shot%202024-02-13%20at%204.31.11%20PM.png)

4. The bug:

`reversed` method before with the bug:
```
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = newArray[arr.length - i - 1];
  }
  return arr;
}
```
`reversed` method after with the bug fixed:
```
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    newArray[i] = arr[arr.length - i - 1];
  }
  return newArray;
}
```
Now the `newArray` array is updated and returned rather than the original array. The reversed elements are now properly assigned to the `newArray`.

## Part 2

`find` command-line options:

`-newer`

Use 1:
```
(base) ethan@Ethans-MacBook-Air-4 biomed % find . -newer rr37.txt         
.
./rr73.txt
./rr74.txt
```
Use 2: 
```
(base) ethan@Ethans-MacBook-Air-4 biomed % find . -newer gb-2003-4-9-r60.txt
.
./rr73.txt
./rr74.txt
./rr171.txt
./rr167.txt
./rr166.txt
./rr172.txt
./rr37.txt
./rr196.txt
./rr191.txt
```
The `-newer` option searches for files that have been modified after the file that is given as an argument. This can be useful if you want to see which files were most recently modified or if you want to sort your files by modification time.

Found at: [https://www.freecodecamp.org/news/how-to-search-files-effectively-in-linux/](https://www.freecodecamp.org/news/how-to-search-files-effectively-in-linux/)

`-regex`

Use 1:
```
(base) ethan@Ethans-MacBook-Air-4 biomed % find . -regex "./rr.*"
./rr73.txt
./rr74.txt
./rr171.txt
./rr167.txt
./rr166.txt
./rr172.txt
./rr37.txt
./rr196.txt
./rr191.txt
```
Use 2:
```
(base) ethan@Ethans-MacBook-Air-4 biomed % find . -regex "./cvm.*"
./cvm-2-1-038.txt
./cvm-2-6-278.txt
./cvm-2-4-180.txt
./cvm-2-6-286.txt
./cvm-2-4-187.txt
```
The `-regex` option searches for files whose name starts with the provided argument. This can be useful if you know the beginning of the name of the file that you are searching for.

Found at: [https://www.freecodecamp.org/news/how-to-search-files-effectively-in-linux/](https://www.freecodecamp.org/news/how-to-search-files-effectively-in-linux/)

`-size`

Use 1:
```
(base) ethan@Ethans-MacBook-Air-4 biomed % find . -size -10000c
./1472-6769-1-4.txt
./1471-2490-3-2.txt
./1471-2334-3-13.txt
```
Use 2:
```
(base) ethan@Ethans-MacBook-Air-4 biomed % find . -size -12000c
./1472-6769-1-4.txt
./1471-2490-3-2.txt
./cc973.txt
./1471-2334-3-13.txt
./1471-2156-2-8.txt
./1471-230X-2-17.txt
./1471-2350-2-8.txt
```
The `-size` option searches for files that are equal to, greater than, or less than the specified size depending on the arguments given to it. This can be useful if you want to sort your files by size or are looking for small/big files.

Found at: [https://www.computerhope.com/unix/ufind.htm](https://www.computerhope.com/unix/ufind.htm)

`-type`

Use 1:
```
(base) ethan@Ethans-MacBook-Air-4 technical % find . -type d 
.
./government
./government/About_LSC
./government/Env_Prot_Agen
./government/Alcohol_Problems
./government/Gen_Account_Office
./government/Post_Rate_Comm
./government/Media
./plos
./biomed
./911report
```
Use 2:
```
(base) ethan@Ethans-MacBook-Air-4 911report % find . -type f
./chapter-13.4.txt
./chapter-13.5.txt
./chapter-13.1.txt
./chapter-13.2.txt
./chapter-13.3.txt
./chapter-3.txt
./chapter-2.txt
./chapter-1.txt
./chapter-5.txt
./chapter-6.txt
./chapter-7.txt
./chapter-9.txt
./chapter-8.txt
./preface.txt
./chapter-12.txt
./chapter-10.txt
./chapter-11.txt
```
The `-type` option searches for files that are of the specified type. This can be useful when you only want to view files of a specific type such as when we only wanted to look at text files in the lab.

Found at: [https://www.redhat.com/sysadmin/linux-find-command](https://www.redhat.com/sysadmin/linux-find-command)
