# CItest


[CI 101](https://www.youtube.com/watch?v=eCOv4AeC6Ic)

- this repo is at https://github.com/davebinkley/CItest/tree/main
- git@github.com:davebinkley/CItest.git

- might try again with private repo ....

## steps
 - IntelliJ
 - new java project, maven, java 17
 - git new public repo
 - add project to repo
 - git web page
    - actions
    - new workflow
    - maven

 - pom.xml **must** include at lease one dependency, for example
    <dependencies>
      <dependency>
        <groupId>org.junit.jupiter</groupId>
        <artifactId>junit-jupiter-engine</artifactId>
        <version>5.9.2</version>
      </dependency>
    </dependencies>
 - otherwise "TypeError: Cannot read properties of undefined (reading 'forEach')"
 - someone forgot to check for the empty list :)

 - also needed to add permissions (apparently at recent change)
   runs-on: ubuntu-latest
     permissions:
       contents: write
       pull-requests: write
       repository-projects: write

 - deleting these failed so i roll back to a past commit
  git reset --hard b94b39f14424f77a53e0abe74ab3d5c2d18c74d5
  HEAD is now at b94b39f apparently you need at least one dependency in pom.xml
  git push -f


