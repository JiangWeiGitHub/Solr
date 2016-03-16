#### General introduction:
Solr is a search engine server that uses lucene, and lucene is a search engine library.<p>

***

#### Related reference:
[*Lucene & Solr*](https://github.com/apache/lucene-solr)<p>
[*Solr Quick Start*](http://lucene.apache.org/solr/quickstart.html)<p>
  
***

#### Deployment:
###### Precondition:
+ Ubuntu 14.04 64bit<p>
+ JDK (Using u55 or later)<p>
  - [*Lastest Version Download Path*](http://www.oracle.com/technetwork/cn/java/javase/downloads/jdk8-downloads-2133151-zhs.html)<p>
  - Install JDK<p>
    **Untar**<p>
    `tar -zxvf jdk-8u73-linux-x64.tar.gz`<p>

    **Create /usr/lib/jvm folder**<p>
    `(sudo) mkdir -p /usr/lib/jvm`<p>
    
    **Move jdk1.8.0_73 folder to /usr/lib/jvm folder**<p>
    `(sudo) mv jdk1.8.0_73/ /usr/lib/jvm/`<p>

    **Edit bashrc file**<p>
    `vim ~/.bashrc`<p>
    
        export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_73
        export JRE_HOME=${JAVA_HOME}/jre
        export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
        export PATH=${JAVA_HOME}/bin:$PATH

  
#### :
