# OML Example

An example demonstrating the OML language

## Clone the repository

Clone the project in some folder in your disk:

```
   git clone git@github.com:modelware/oml-example.git
   cd oml-example
```

## Work from Command Line

### Vocabularies

1. Nvaigate
```
   cd vocabularies
```

2. Build

```
   ./gradlew build
```

3. Publish to Maven Local

```
   ./gradlew publishToMavenLocal
```

4. Generate Documentation

```
   ./gradlew generateDocs
```

### Descriptions

Prepreq: You must have published the vocabularies (above) to your Maven Local repo

1. Nvaigate
```
   cd descriptions
```

2. Build

```
   ./gradlew build
```

3. Publish to Maven Local

```
   ./gradlew publishToMavenLocal
```

4. Generate Documentation

```
   ./gradlew generateDocs
```

5. Start Fuseki
Prereq: Fuseki is not running

```
   ./gradlew startFuseki
```

5. Run Queries
Prereq: Fuseki is running

```
   ./gradlew owlQuery
```

5. Stop Fuseki
Prereq: Fuseki is running

```
   ./gradlew startFuseki
```

## Work in Rosetta

Download the OML [Rosetta](https://github.com/opencaesar/oml-rosetta/releases/tag/0.5.0) Workbench zip file for your OS

Unzip the archive and double click on the Rosetta icon to launch (notice: Rosetta is an Eclipse RCP)

In Project Explorer viwew (menu): Filters and Customizations -> (uncheck) Gradle build folder

## Import Projects

Import the project In Rosetta: File -> Import -> Existing Gradle Project -> Next -> Browse (to the oml-example/vocabularies) -> Finish

Import the project In Rosetta: File -> Import -> Existing Gradle Project -> Next -> Browse (to the oml-example/descriptions) -> Finish

## Run Analysis Tools

Show the Gradle views: Window -> Show View -> Other... -> Gradle -> (select both views) -> Open

In Gradle Tasks view (view menu): Show All Tasks

### Vocabularies

In Gradle Tasks view: Expand vocabularies

Select the following tools:

```other/build```: to build the project

```publishing/publishToMavenLocal```: to publish to maven local

### Desriptions

Prepreq: You must have published the vocabularies (above) to your Maven Local repo

In Gradle Tasks view: Expand vocabularies

Select the following tools:

```other/build```: to build the project

```publishing/publishToMavenLocal```: to publish to maven local

```other/startFuseki```: to start a Fuseki server

```other/owlQuery```: to run the SPARQL queries

```other/stopFuseki```: to stop a Fuseki server


**Note**: After each Gradle operation above, right click on the relevant project in Project Explorer view and select Refresh and inspect the results in the build folder
