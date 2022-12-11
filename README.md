# CPSC_531_Adv_DB
## DEPLOYMENT AND RUNNING INSTRUCTIONS:

<ol>
      <li><b>Search Engine</b></li>
      <ol>
        <li>Install Java to your system.(Recommended to install in C drive)</li>
        <li>DownloadHadoop2.0+(&lt;Hadoop3.0).</li>
        <ol>
          <li>Extract Hadoop at C:\hadoop\</li>
          <li>Download the Windows binaries for Hadoop Versions.(https://github.com/steveloughran/winutils)</li>
          <li>Extract the contents to C:/hadoop/bin</li>
        </ol>
        <li>Set the HADOOP\_HOMEvariable. Path-> <b>"C:/hadoop/bin/"</b></li>
        <li>Set the JAVA\_HOMEvariable.Path-> <b>"C:/Java/"</b></li>
        <li>Set Hadoop and Java bin directories</li>
        <ol>
          <li>Path-> <b>"C:/Java/bin"</b></li>
          <li>Path-> <b>"C:/hadoop/bin/"</b></li>
          <li>Path-> <b>"C:/hadoop/sbin/"</b></li>
        </ol>
        <li>Verify the Java and Hadoop installed andsetup</li>
        <ol>
          <li>javac-version</li>
          <li>hadoop-version</li>
        </ol>
        <li>Hadoop Configuration– You need to modify 6files</li>
        <ol>
          <li>
            You need to create two folders <b>"datanode"</b> and
            <b>"namenode"</b> inside the data folder(C:/hadoop/data)
          </li>
          <li>
            Configuration of the below listed can be found[<a
              href="https://drive.google.com/drive/folders/1VDGJ-iO7BRlmHXoE28ARVrezPZ7jrC5E?usp=share_link"
              >here</a>].
          </li>
          <li>5 files in "Hadoop/bin"</li>
          <ol>
            <li>Core-site.xml</li>
            <li>Mapred-site.xml</li>
            <li>Hdfs-site.xml</li>
            <li>Yarn-site.xml</li>
            <li>Hadoop-env.cmd</li>
          </ol>
        </ol>
        <li>
          Open the command prompt(Run as Administrator)and type the following command.
        </li>
        <ol>
          <li>hdfs namenode -format</li>
        </ol>
        <li>
          Now you can start the process to run the project. Make sure you run the command prompt as
          <b>Administrator</b>
        </li>
        <ol>
          <li>cd C:/hadoop/sbin</li>
          <li>start-all(starting all the Hadoop services)</li>
          <li>cd C:/Hadoop or cd..</li>
          <li>
            hadoop fs mkdir /EnWikiSubset (creating an EnWikiSubset directory in HDFS)
          </li>
          <li>
            hadoop fs -put /path to the directory where you cloned the folder/EnWikiSubset/*
            /EnWikiSubsetNote – "/*" is used to transfer all files from that
            folder to the directory in HDFS.
          </li>
          <li>
            hadoop fs -ls/EnWikiSubset (check whether all the files have been successfully uploaded in the HDFS EnWikiSubset directory).
          </li>
          <li>
            hadoop jar/path to the directory where you cloned the folder/search_engine.jar Indexer /EnWikiSubset (Running the Indexer Engine)
          </li>
          <li>
            hadoop jar/path to the directory where you cloned the folder
            /search_engine.jar Query N "query text" (Running the Ranker Engine.
            'N'is the number which user will input like 1,2,3,4,…,to get that many relevances for
            the query text)
          </li>
          <li>stop-all (To stop all HDFS services running currently)</li>
        </ol>
      </ol>
      <h3>Note:- Dataset is not fully uploaded as the size of dataset is in GB. Complete dataset can be found <a href="https://drive.google.com/drive/folders/1-Tr3EJpSogf4ysgL17csd-U_gsB0-zwJ?usp=sharing">here</a></h3>
      <br>
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
    </ol>
