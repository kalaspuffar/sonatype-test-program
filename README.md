# sonatype-test-program

This program is just a test to fetch a bunch of packages from a local repository.

### Settings.xml

In your local repository settings file you need to specify the user you want to use to talk to your repository.
And the second part is specifying the mirror to use for packages. We will use the public repository that contains snapshots, releases and the central repository.
```
<settings>
  <servers>
    <server>
      <id>central</id>
      <username>[username]</username>
      <password>[password]</password>
    </server>
  </servers>
  <mirrors>
    <mirror>
      <id>central</id>
      <name>central</name>
      <url>http://[host+port]/repository/maven-public/</url>
      <mirrorOf>*</mirrorOf>
    </mirror>
  </mirrors>
</settings>
```