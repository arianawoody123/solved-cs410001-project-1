Download Link: https://assignmentchef.com/product/solved-cs410001-project-1
<br>






<ol>

 <li>Project Objective

  <ol>

   <li>Implement a single-cycle functional processor simulator.</li>

   <li>Design your own test case to test the functionality of your simulator.</li>

  </ol></li>

</ol>




<ol start="2">

 <li>Project Description</li>

 <li>Architecture Design:

  <ul>

   <li>Refer to textbook <em>Chapter 2 “Instructions”</em> and <em>Chapter 4.1~4.4 “The Processor”</em>.</li>

   <li>The executable file should be named “single_cycle” and take <strong>no command-line arguments.</strong></li>

   <li>All registers, except PC and $sp, are initialized to 0’s.</li>

   <li>Assume that the instruction memory is of 1K bytes size and all contents are initialized to 0’s.</li>

   <li>The data memory is of 1K bytes size and the memory contents are initialized to 0’s.</li>

   <li>Your test case should run no more than 500,000 cycles.</li>

  </ul></li>

</ol>




<ol>

 <li>Instruction Set:</li>

</ol>

<ul>

 <li>Implement all the instructions specified in the reduced MIPS R3000 ISA in <strong><em>Appendix A</em>, “<em>Datasheet for the Reduced MIPS R3000 ISA</em>”</strong>.</li>

 <li>The execution of the single-cycle processor simulator should <strong>terminate </strong>after executing the <strong>“halt” instruction</strong>.</li>

</ul>




<ol>

 <li>Input Test Case File and Format:</li>

</ol>

<ul>

 <li>Design your own test case by providing the following two<strong> binary files</strong>:</li>

</ul>

<ol>

 <li><strong>iimage.bin</strong>:

  <ol>

   <li>This file specifies the instruction image (in <strong>big-endian</strong> format, encoded in binary).</li>

   <li>The first four bytes indicate the initial value of PC, i.e. the starting address to load the instruction image.</li>

   <li>The next four bytes specify the number of words to be loaded into instruction memory.</li>

   <li>The remaining are the program instructions to be loaded into I-memory.</li>

   <li><strong>dimage.bin</strong>:</li>

   <li>This file specifies the data image (in <strong>big-endian</strong> format, encoded in binary).</li>

   <li>The first four bytes indicate the initial value of $sp.</li>

   <li>The next four bytes specify the number of words to be loaded into data memory, starting from address 0.</li>

  </ol></li>

</ol>

<ul>

 <li>For format details, please refer to <strong><em>Appendix B</em>, “<em>Input Samples</em>”</strong>.</li>

 <li>Place both “iimage.bin” and “dimage.bin” under a folder named testcase/ at the same directory where your executable file resides.</li>

 <li>We will pool all test cases from the class to evaluate everyone’s simulator. Your (valid) test case gets higher grade if more simulators failed running your test case.</li>

</ul>




<ol>

 <li>Output File and Format:</li>

</ol>

<ul>

 <li>For each test case, generate the following two output files:

  <ol>

   <li><strong>rpt</strong>: Record all the register values at each cycle.</li>

   <li><strong>rpt</strong>: Record any error messages.</li>

  </ol></li>

 <li>Place the output files at the same directory where your executable file resides.</li>

 <li>For details, please refer to <strong><em>Appendix C-1, “Output Samples for Project 1”</em></strong> and <strong><em>Appendix D, “Error Detection Samples”</em></strong>.</li>

</ul>




<ol>

 <li>Modularized implementation</li>

</ol>

<ul>

 <li>Suggest that you should <strong>modularize</strong> your simulator implementation based on processor architecture. For example, this is a possible program structure:

  <ol>

   <li>c     // Define simulator behaviors and main function</li>

   <li>c // Define &amp; decode instructions</li>

   <li>c             // Register function</li>

   <li>c       // Memory function (for both instruction &amp; data memories)</li>

   <li>c……             // other miscellaneous functions</li>

  </ol></li>

</ul>

<ul>

 <li>Appropriate header file or object-oriented programming format are also highly recommended design pattern.</li>

</ul>




<ol start="3">

 <li>The 2-submission Process</li>

 <li>Each project has two submissions. The second due date is normally one week after the first one.

  <ul>

   <li>Before 1<sup>st</sup> submission: we will release a <strong>golden executable</strong> and <strong>open test cases</strong> to help you verify your designs.</li>

   <li>1<sup>st</sup> submission: submit your simulator and test case for evaluation.</li>

   <li>After 1<sup>st</sup> submission (before 2<sup>nd</sup> submission): we will release <strong>all test cases</strong> <strong>(including hidden test cases and all test cases submitted by the class) </strong>for you to polish your simulator.</li>

   <li>2<sup>nd</sup> submission: submit your revised simulator and project <strong>report</strong> (format is specified in the Grading Policy section).</li>

  </ul></li>

</ol>

<ol>

 <li>Prepare your project package for development and submission</li>

</ol>

<ul>

 <li>Before you start your project

  <ol>

   <li>Use SSH to access workstation.</li>

   <li>Clone sample files from GitHub to your home directory.</li>

  </ol></li>

</ul>

l Clone a repository NTHU Architecture 2016 from GitHub and name it as studentID_01/ under /home/archi/studentID. Inside the folder, it contains two folders:

<ol>

 <li>simulator/ : contains your Makefile, and source code.</li>

 <li>Your Makefile should support the following two functions:</li>

</ol>

<ul>

 <li>make – to build your simulation environment</li>

 <li>make clean – to erase from the build tree the files built by make all.</li>

</ul>

<ol>

 <li>Modulize your source code as recommended.</li>

 <li>testcase/ : contains your test case files for evaluation.</li>

 <li>Do coding/debugging/testing using Git version control tool.</li>

</ol>

<ul>

 <li>Before submission and after completing your project

  <ol>

   <li>Check your output file format using test_script.py</li>

   <li>Compress the folder studentID_01 as studentID_01.tar.gz, and upload studentID_01.tar.gz and studentID_report.pdf to the iLMS system.</li>

  </ol></li>

</ul>




<ul>

 <li><strong>Note:</strong> TAs will check your Git log during 1-on-1 Demo. Please follow version control rule when doing programming.</li>

 <li><strong>Note:</strong>. Verify your package format by executing test_script.py before each submission. <strong>Wrong submission format earns no points. </strong></li>

</ul>




<ol start="4">

 <li>Grading Policy</li>

 <li>First submission</li>

</ol>

<ul>

 <li>Correctness of simulator: 25%

  <ol>

   <li>TA’s open test cases: 15%</li>

   <li>TA’s hidden test cases: 5%*Correct Ratio</li>

   <li>Students’ valid test cases: 5%*Correct Ratio</li>

  </ol></li>

</ul>

<ul>

 <li>Test case strength: 20%*(1 – [1.5]<sup>-n</sup>), n: number of other simulators defeated 1. Submit your test case to participate in the pool test.</li>

</ul>

l             <strong>Note:</strong> You get zero points if your test case is invalid.

<ol>

 <li>Second submission</li>

</ol>

<ul>

 <li>Correctness of simulator: 30%</li>

</ul>

<ol>

 <li>TA’s open test cases: 5%</li>

 <li>TA’s hidden test cases: 10%*Correct Ratio</li>

 <li>Students’ valid test cases: 15%*Correct Ratio</li>

</ol>

<ul>

 <li>Performance: 5%</li>

</ul>

<ol>

 <li>TA will collect the execution time of your simulator running all the valid test cases (including all open, hidden and students’ test cases).</li>

 <li>TA will rank all execution times in 5 levels and grade accordingly.</li>

</ol>

l <strong>Note: </strong>If your simulator fails to execute the valid test cases you will get the lowest performance grade.

<ul>

 <li>Report &amp; Demo: 20%</li>

</ul>

<ol>

 <li>The report file should be named <strong><em>studentIDpdf</em></strong>, where <strong><em>studentID </em></strong>is the NTHU student id you used for school registration.</li>

 <li>Each person should reserve a 15-min demo with TA. During the 1-on-1 demo, TA’s will ask you questions related to your project report, test case and your implemented code on workstation.</li>

 <li>Your project report is recommended to follow this outline:</li>

</ol>




1) Project Description




<ul>

 <li>Program Flow Chart</li>

</ul>




<ul>

 <li>Detailed Description</li>

</ul>




2) Test case Design

<sup>                 </sup>2-1) Detailed Description of Test case







<strong>Note:</strong> The project report is limited to 10 pages.

<strong>Note:</strong> Your report can be either in Chinese or English, or mixed.

<strong>Note: </strong>For convenience, please synchronize your submission code with your code in workstation. This allows smoother demo on workstation.





