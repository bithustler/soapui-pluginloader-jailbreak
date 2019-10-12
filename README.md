# SoapUI PluginLoader Jailbreak

Bypasses SoapUI plugin signature check.

Needed only for homemade plugins and for SoapUI OpenSource since version 5.2.1

## Build with Maven

```sh
git clone https://github.com/bithustler/soapui-pluginloader-jailbreak.git
cd soapui-pluginloader-jailbreak
mvn clean package
```

## Install

Download [`soapui-pluginloader-jailbreak-5.5.0.jar`](https://github.com/bithustler/soapui-pluginloader-jailbreak/releases/download/v5.5.0/soapui-pluginloader-jailbreak-5.5.0.jar) and copy into the `$SOAPUI_HOME/bin/ext/` folder.

**Configure Command Line**

Add the following line to the `$SOAPUI_HOME\bin\soapui.sh`:

```sh
JAVA_OPTS="$JAVA_OPTS -Djava.ext.dirs=${SOAPUI_HOME}/bin/ext:${JAVA_HOME}/jre/lib/ext"
```

**Configure Install4J**

On MacOS the SoapUI package installer will place the application under `/Applications/SoapUI-5.5.0.app` where the SoapUI home is `/Applications/SoapUI-5.5.0.app/Contents/java/app`.

Add the following line below the `-Xmx[1000m]` VM heap settings in the `/Applications/SoapUI-5.5.0.app/Contents/vmoptions.txt` file:

```properties
-Djava.ext.dirs=/Applications/SoapUI-5.5.0.app/Contents/Resources/app/bin/ext:/Applications/SoapUI-5.5.0.app/Contents/PlugIns/jre.bundle/Contents/Home/jre/lib/ext
```
