<li><b>Map-Reduce Examples</b></li>
      <ol>
        <li>Download Hadoop2.0+(&lt;Hadoop3.0).</li>
        <li>Unzip the tarfile and open a new project in IntelliJ.</li>
        <li>
          Navigate to the project dependencies pane(For IntelliJ,it is under ProjectStructure).
        </li>
        <li>Click on Add Dependencies/JARs; you want to add the directories</li>
        <ol>
          <li>hadoop-2.x.x/share/Hadoop/common</li>
          <li>hadoop-2.x.x/share/Hadoop/hdfs</li>
          <li>hadoop-2.x.x/share/Hadoop/MapReduce</li>
          <li>hadoop-2.x.x/share/Hadoop/yarn</li>
          <li>hadoop-2.x.x/share/Hadoop/common/lib</li>
        </ol>
        <li>Download Windows binaries from corresponding builds.</li>
        <li>
          Copy the corresponding bin folder to hadoop-2.x.x/share/Hadoop/commondirectory.
        </li>
        <li>
          Now create a new directory named "winutils";I make this directory under C:/winutils
        </li>
        <li>Navigate inside and make a sub-directory bin.</li>
        <li>
          Copy winutils.exe and hadoop.dll from winutils-master/hadoop-2.x.x/bintoC:/winutils/bin.
        </li>
        <li>
          Add a new system variable HADOOP\_HOME and point it to the C:/winutils directory.
        </li>
        <li>
          Also, edit the system PATH variable and add %HADOOP\_HOME%/bin to the list.
        </li>
        <li>
          You need to change the path for the input and output file that has
          been specified in the code.We have given the absolute path for processing.
        </li>
        <li>Restart the system and run the codes.</li>
      </ol>
