# To create Scala projects in Eclipse

1. Need the m2eclipse-scala plugin

<pre>
Under “Help -> Install New Software”, enter “http://alchim31.free.fr/m2e-scala/update-site” and hit enter. You should see “Maven Integration for Eclipse -> Maven Integration for Scala IDE”.
</pre>

2. Need to configure remote repository so scala-arch can be found
<pre>
I had same problem and it was solved by adding a remote catalog: http://repo1.maven.org/maven2/archetype-catalog.xml
</pre>

3. Have to add the following dependency to pom.xml once project is created

<pre>
<dependency>
        <groupId>org.specs2</groupId>
        <artifactId>specs2-junit_${scala.compat.version}</artifactId>
        <version>2.4.16</version>
        <scope>test</scope>
    </dependency>
</pre> 
