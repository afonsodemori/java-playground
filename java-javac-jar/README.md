# Compiling classes, generating jar files and executing .jar on docker

## Compiling

```bash
javac dev/afonso/java_playground/javac/Main.java
```

## Executing

```bash
java dev.afonso.java_playground.javac.Main
```

## Creating a jar

```bash
jar --create --file app.jar \
    --main-class dev/afonso/java_playground/javac/Main \
    dev/afonso/java_playground/javac/Main.class
```

## Executing a jar

```bash
java -jar app.jar
```

## Docker

```bash
docker run --rm -v $PWD:/app -w /app openjdk java -jar app.jar
```
