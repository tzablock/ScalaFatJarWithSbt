1. Create assembly.sbt file in PROJECT_ROOT_FOLDER/project root (not in PROJECT_ROOT_FOLER where is build.sbt)
2. add content into assebly.sbt:
addSbtPlugin("com.eed3si9n" % "sbt-assembly" % "0.14.7")
3. Set in build.sbt proper scalaVersion := "..."
4. Run in PROJECT_ROOT_FOLDER sbt assembly
 Our fat jar will be created according to logs:
"Packaging /path/OUR_JAR.jar ... "
5. Than if it contains main object we can run it like:
     a) if we have java installed: java -cp OUR_JAR.jar packages.MAIN_OBJECT
     b) if we have scala installed: scala OUR_JAR.jar packages.MAIN_OBJECT
       (as well work just "scala OUR_JAR.jar" if we have one main object)

Structure:
- RootFolder
    -- bin
    -- project
        --- assembly.sbt
        --- build.properties 
    -- src
        --- scala
            ---- ...scala
    -- target
    -- buildt.sbt
