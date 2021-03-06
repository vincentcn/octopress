---
layout: post
title: "Java备忘-Java运行环境中的Environment variables和System Properties"
date: 2013-12-28 19:49:59 +0800
comments: true
sharing: true
categories: [Java,备忘录] 
---
这篇Java备忘录，主要记录Java runtime的参数配置。
##1. Environment Variables##
Environment Variables主要是运行平台相关的变量，包含了VM运行在的OS的环境变量，在Eclipse中可以通过debug/run配置界面(见下图)的对系统变量进行扩展/替代设置。
  
  ![Eclipse中Environment Variables的设置][1]
  
Java代码中可以通过下面语句访问。
```
Map<String, String> env = System.getenv();
```  
  
下面的列表是在Win64环境中的一个运行实例中的Envrionment Variables列表。
```
USERPROFILE = C:\Users\Vincent Xue
ProgramData = C:\ProgramData
PATHEXT = .COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC;.RB;.RBW
JAVA_HOME = C:\Program Files\Java\jdk1.7.0_40
ProgramFiles(x86) = C:\Program Files (x86)
TEMP = C:\Users\VINCEN~1\AppData\Local\Temp
SystemDrive = C:
ProgramFiles = C:\Program Files
M2 = D:\DevTools\maven\apache-maven-3.1.1-bin\bin
Path = C:\Program Files (x86)\SenchaSDKTools-2.0.0-beta3;C:\Ruby200-x64\bin;C:\Program Files (x86)\NVIDIA Corporation\PhysX\Common;C:\Windows\system32;C:\Windows;C:\Windows\System32\Wbem;C:\Windows\System32\WindowsPowerShell\v1.0\;C:\Program Files\Intel\WiFi\bin\;C:\Program Files\Common Files\Intel\WirelessCommon\;C:\Program Files (x86)\Intel\OpenCL SDK\2.0\bin\x86;C:\Program Files (x86)\Intel\OpenCL SDK\2.0\bin\x64;C:\Program Files\Java\jdk1.7.0_40\bin;C:\Program Files\nodejs\;D:\DevTools\mysql-5.5.20-winx64\bin;C:\Program Files (x86)\Microsoft SQL Server\100\Tools\Binn\;C:\Program Files\Microsoft SQL Server\100\Tools\Binn\;C:\Program Files\Microsoft SQL Server\100\DTS\Binn\;D:\DevTools\maven\apache-maven-3.1.1-bin\bin;C:\Program Files\Intel\WiFi\bin\;C:\Program Files\Common Files\Intel\WirelessCommon\;C:\Users\Vincent Xue\AppData\Roaming\npm
HOMEDRIVE = C:
PROCESSOR_REVISION = 2a07
USERDOMAIN = VincentXue-PC
SSL_CERT_FILE = D:\ruby\cert\cacert.pem
ALLUSERSPROFILE = C:\ProgramData
ProgramW6432 = C:\Program Files
PROCESSOR_IDENTIFIER = Intel64 Family 6 Model 42 Stepping 7, GenuineIntel
SESSIONNAME = Console
M2_REPO = D:\DevTools\maven\M2_Repo
TMP = C:\Users\VINCEN~1\AppData\Local\Temp
MAVEN_OPTS = -Xms256m -Xmx512m
CommonProgramFiles = C:\Program Files\Common Files
LOGONSERVER = \\VINCENTXUE-PC
M2_HOME = D:\DevTools\maven\apache-maven-3.1.1-bin
PROCESSOR_ARCHITECTURE = AMD64
FP_NO_HOST_CHECK = NO
OS = Windows_NT
8HOMEPATH = \Users\Vincent Xue
VS100COMNTOOLS = C:\Program Files (x86)\Microsoft Visual Studio 10.0\Common7\Tools\
PROCESSOR_LEVEL = 6
CommonProgramW6432 = C:\Program Files\Common Files
SENCHA_SDK_TOOLS_2_0_0_BETA3 = C:\Program Files (x86)\SenchaSDKTools-2.0.0-beta3
LOCALAPPDATA = C:\Users\Vincent Xue\AppData\Local
COMPUTERNAME = VINCENTXUE-PC
windir = C:\Windows
SystemRoot = C:\Windows
asl.log = Destination=file
NUMBER_OF_PROCESSORS = 8
USERNAME = Vincent Xue
PUBLIC = C:\Users\Public
PSModulePath = C:\Windows\system32\WindowsPowerShell\v1.0\Modules\
CommonProgramFiles(x86) = C:\Program Files (x86)\Common Files
ComSpec = C:\Windows\system32\cmd.exe
APPDATA = C:\Users\Vincent Xue\AppData\Roaming
```
  
##2. System Properties##
System Properties主要是VM运行的属性，也可以通过debug/run配置界面进行扩展(下图)  
  
  ![Eclipse中VM Arguments的设置][2]
  
在Java代码中可以通过下面语句访问。
```
Properties props = System.getProperties();
```
  
下面的列表是在Win64环境中的一个运行实例中的System Properties列表。
```
java.runtime.name = Java(TM) SE Runtime Environment
sun.boot.library.path = C:\Program Files\Java\jre7\bin
java.vm.version = 24.0-b56
java.vm.vendor = Oracle Corporation
java.vendor.url = http://java.oracle.com/
path.separator = ;
java.vm.name = Java HotSpot(TM) 64-Bit Server VM
file.encoding.pkg = sun.io
user.country = US
user.script = 
sun.java.launcher = SUN_STANDARD
sun.os.patch.level = Service Pack 1
java.vm.specification.name = Java Virtual Machine Specification
user.dir = D:\Java\JavaWorkspace\TaskProcessSystem
java.runtime.version = 1.7.0_40-b43
java.awt.graphicsenv = sun.awt.Win32GraphicsEnvironment
java.endorsed.dirs = C:\Program Files\Java\jre7\lib\endorsed
os.arch = amd64
java.io.tmpdir = C:\Users\VINCEN~1\AppData\Local\Temp\
line.separator = 
java.vm.specification.vendor = Oracle Corporation
user.variant = 
os.name = Windows 7
sun.jnu.encoding = GBK
java.library.path = C:\Program Files\Java\jre7\bin;C:\Windows\Sun\Java\bin;C:\Windows\system32;C:\Windows;C:\Program Files (x86)\SenchaSDKTools-2.0.0-beta3;C:\Ruby200-x64\bin;C:\Program Files (x86)\NVIDIA Corporation\PhysX\Common;C:\Windows\system32;C:\Windows;C:\Windows\System32\Wbem;C:\Windows\System32\WindowsPowerShell\v1.0\;C:\Program Files\Intel\WiFi\bin\;C:\Program Files\Common Files\Intel\WirelessCommon\;C:\Program Files (x86)\Intel\OpenCL SDK\2.0\bin\x86;C:\Program Files (x86)\Intel\OpenCL SDK\2.0\bin\x64;C:\Program Files\Java\jdk1.7.0_40\bin;C:\Program Files\nodejs\;D:\DevTools\mysql-5.5.20-winx64\bin;C:\Program Files (x86)\Microsoft SQL Server\100\Tools\Binn\;C:\Program Files\Microsoft SQL Server\100\Tools\Binn\;C:\Program Files\Microsoft SQL Server\100\DTS\Binn\;D:\DevTools\maven\apache-maven-3.1.1-bin\bin;C:\Program Files\Intel\WiFi\bin\;C:\Program Files\Common Files\Intel\WirelessCommon\;C:\Users\Vincent Xue\AppData\Roaming\npm;.
java.specification.name = Java Platform API Specification
java.class.version = 51.0
sun.management.compiler = HotSpot 64-Bit Tiered Compilers
os.version = 6.1
user.home = C:\Users\Vincent Xue
user.timezone = Asia/Shanghai
java.awt.printerjob = sun.awt.windows.WPrinterJob
file.encoding = GBK
java.specification.version = 1.7
java.class.path = D:\Java\JavaWorkspace\TaskProcessSystem\bin;D:\Java\JavaWorkspace\TaskProcessSystem\libs\log4j-api-2.0-beta9.jar;D:\Java\JavaWorkspace\TaskProcessSystem\libs\log4j-core-2.0-beta9.jar
user.name = Vincent Xue
java.vm.specification.version = 1.7
sun.java.command = me.vxue.tps.consumer.SimpleCalculationConsumer
java.home = C:\Program Files\Java\jre7
sun.arch.data.model = 64
user.language = en
java.specification.vendor = Oracle Corporation
awt.toolkit = sun.awt.windows.WToolkit
java.vm.info = mixed mode
java.version = 1.7.0_40
java.ext.dirs = C:\Program Files\Java\jre7\lib\ext;C:\Windows\Sun\Java\lib\ext
sun.boot.class.path = C:\Program Files\Java\jre7\lib\resources.jar;C:\Program Files\Java\jre7\lib\rt.jar;C:\Program Files\Java\jre7\lib\sunrsasign.jar;C:\Program Files\Java\jre7\lib\jsse.jar;C:\Program Files\Java\jre7\lib\jce.jar;C:\Program Files\Java\jre7\lib\charsets.jar;C:\Program Files\Java\jre7\lib\jfr.jar;C:\Program Files\Java\jre7\classes
java.vendor = Oracle Corporation
file.separator = \
java.vendor.url.bug = http://bugreport.sun.com/bugreport/
sun.io.unicode.encoding = UnicodeLittle
sun.cpu.endian = little
sun.desktop = windows
sun.cpu.isalist = amd64
```

[1]: http://vxue.u.qiniudn.com/blog.pic.eclipse_config_env.jpg "Eclipse中Environment Variables的设置"
[2]: http://vxue.u.qiniudn.com/blog.pic.eclipse_config_vm_arguments.jpg "Eclipse中VM Arguments的设置"