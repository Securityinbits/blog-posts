dumper.java code is copied from [Reversing an obfuscated java malware by Extreme Coders](https://onedrive.live.com/?authkey=%21AP%2DLGmNO74brJ6s&cid=E91E11F5FA1D754C&id=E91E11F5FA1D754C%21219&parId=E91E11F5FA1D754C%21126&o=OneUp)

Uploded the jar file generated using following cmds:
```
javac dumper.java
jar cmf MANIFEST.MF dumper.jar dumper.class transformer.class
```

To dump the class file of malware.jar:
```
java -javaagent:dumper.jar -jar malware.jar
```

Import note: Another important point is there must be a new line at the end of the MANIFEST file. Otherwise, the last header is ignored.
