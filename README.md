#### General introduction:
Solr is a search engine server that uses lucene, and lucene is a search engine library.<p>

***

#### Related reference:
[*Lucene & Solr*](https://github.com/apache/lucene-solr)<p>
[*Solr Quick Start*](http://lucene.apache.org/solr/quickstart.html)<p>
  
***

#### Deployment:
#### Precondition:
+ Ubuntu 14.04 64bit<p>
+ JDK (Using u55 or later)<p>
  - [*Lastest Version Download Path*](http://www.oracle.com/technetwork/cn/java/javase/downloads/jdk8-downloads-2133151-zhs.html)<p>
        *name: jdk-8u73-linux-x64.tar.gz*<p>
        *md5: 1b0120970aa8bc182606a16bf848a686*<p>
  - Install JDK<p>
    **Untar**<p>
    `tar -zxvf jdk-8u73-linux-x64.tar.gz`<p>

    **Create /usr/lib/jvm folder**<p>
    `(sudo) mkdir -p /usr/lib/jvm`<p>
    
    **Move jdk1.8.0_73 folder under /usr/lib/jvm folder**<p>
    `(sudo) mv jdk1.8.0_73/ /usr/lib/jvm/`<p>

    **Edit bashrc file**<p>
    `vim ~/.bashrc`<p>

        # add a few lines as follows to the end of the file. 
        export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_73
        export JRE_HOME=${JAVA_HOME}/jre
        export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
        export PATH=${JAVA_HOME}/bin:$PATH

    **Configure default JDK version**<p>
    `(sudo) update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk1.8.0_73/bin/java 300`<p>
    update-alternatives: using /usr/lib/jvm/jdk1.8.0_73/bin/java to provide /usr/bin/java (java) in auto mode<p>

    `(sudo) update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk1.8.0_73/bin/javac 300`<p>
    update-alternatives: using /usr/lib/jvm/jdk1.8.0_73/bin/javac to provide /usr/bin/javac (javac) in auto mode

    `(sudo) update-alternatives --install /usr/bin/jar jar /usr/lib/jvm/jdk1.8.0_73/bin/jar 300`<p>
    update-alternatives: using /usr/lib/jvm/jdk1.8.0_73/bin/jar to provide /usr/bin/jar (jar) in auto mode

    **Check system configuration for java**<p>
    `(sudo) update-alternatives --config java`<p>
    There is only one alternative in link group java (providing /usr/bin/java): /usr/lib/jvm/jdk1.8.0_73/bin/java<p>
    Nothing to configure.

    **Check the version**<p>
    `java -version`<p>
    
        java version "1.8.0_73"
        Java(TM) SE Runtime Environment (build 1.8.0_73-b02)
        Java HotSpot(TM) 64-Bit Server VM (build 25.73-b02, mixed mode)

    **Done**<p>
    
#### Install Solr:
+ Download<p>
[*Download Path*](http://apache.opencas.org/lucene/solr/5.5.0/solr-5.5.0.tgz)
+ Untar<p>
`tar -zxvf solr-5.5.0.tgz`<p>
+ Enter the folder<p>
`cd solr-5.5.0`<p>
+ Run first hello world<p>
`bin/solr start -e cloud -noprompt`<p>
*PS: open browser with http://localhost:8983/solr/*<p>

#### Use Solr:
