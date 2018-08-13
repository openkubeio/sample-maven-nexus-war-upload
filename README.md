# sample-maven-nexus-war-upload

# ..\.m2\settings.xml 

**************settings.xml********************
<settings>
<servers>
    <server>
      <id>nexus</id>
      <username>admin</username>
      <password>admin123</password>
    </server>
 </servers>
</settings>
**********************************************

***************pom.xml************************
<distributionManagement>
  
    <repository>
      <id>nexus</id>
      <name>Releases</name>
      <url>http://localhost:8081/repository/maven-releases</url>
    </repository>
    
    <snapshotRepository>
      <id>nexus</id>
      <name>Snapshot</name>
      <url>http://localhost:8081/repository/maven-snapshots</url>
    </snapshotRepository>
    
</distributionManagement>
***********************************************
#
# mvn clean test deploy
#
