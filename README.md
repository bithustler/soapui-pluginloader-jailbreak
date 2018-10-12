# SoapUI PluginLoader Jailbreak

Bypasses SoapUI plugin signature check.

Needed only for homemade plugins and for SoapUI OpenSource since version 5.2.1

## Build with Maven
mvn clean package

## Install

Copy from `target/soapui-pluginloader-jailbreak-5.4.0.jar` to `$SOAPUI_HOME/bin/ext/`

Add the following line to the `$SOAPUI_HOME\bin\soapui.sh`:

```sh
JAVA_OPTS="$JAVA_OPTS -Djava.ext.dirs=${SOAPUI_HOME}/bin/ext:${JAVA_HOME}/jre/lib/ext"
```
