---
layout: post
title: (转)26款Android逆向工具
tags: Android
---	
译文: http://www.freebuf.com/sectool/111532.html
原文: https://hackerlists.com/android-reverse-engineering-tools

	工欲善其事必先利其器，好的Android逆向工程工具在逆向破解工程中起到事半功倍的作用。
<h2><strong>1. SMALI/BAKSMALI</strong></h2>
<p>SMALI/BAKSMALI是一个强大的apk文件编辑工具，用于Dalvik虚拟机（Google公司自己设计用于Android平台的虚拟机）来反编译和回编译classes.dex。其语法是一种宽松式的Jasmin/dedexer语法，而且它实现了.dex格式所有功能（注解，调试信息，线路信息等）。</p>
<p>下载地址：<span style="color: windowtext;"><u><a href="http://code.google.com/p/smali/downloads/list">传送门</a></u></span></p>
<h2><strong>2. ANDBUG</strong></h2>
<p>Andbug是一款针对Android平台的Dalvik虚拟机的调试工具，工具基于jdwp协议，使用了python封装，其灵活性和可定制性对逆向工程师和开发人员而言可谓是神器级别的安卓安全工具。它与Android的Eclipse插件调试使用相同的接口，其Java 调试线协议（JDWP）和Dalvik调试监视器（DDM）允许用户监视Dalvik虚拟机，检查进程状态。</p>
<p>不同于谷歌自己的Android软件开发工具包调试工具，AndBug不要求源代码。但是，它需要使用python封装，因为对于大多数重要的任务，它需要使用一个脚本断点（scripted breakpoints）的概念，称为“hooks”。</p>
<p>下载地址：<span style="color: windowtext;"><u><a href="https://github.com/swdunlop/AndBug">传送门</a></u></span></p>
<h2><strong>3. ANDROGUARD</strong></h2>
<p>androguard (也称Android guard) 是 Android 应用程序的逆向工程，提供恶意软件分析等功能。其特征为：</p>
<blockquote><p>使用DAD作为反编译器；</p>
<p>可以分析恶意软件；<span></span></p>
<p>主要由Python 编写；</p>
<p>支持可视化；</p>
</blockquote>
<p>androguard 支持：</p>
<blockquote><p>DEX, ODEX；</p>
<p>APK；</p>
<p>Android的二进制XML； </p>
<p>Android资源文件； </p>
<p>分解的DEX/ODEX 字节； </p>
<p>DEX/ODEX 文件反编译程序；</p>
</blockquote>
<p>下载地址：<span style="color: windowtext;"><u><a href="https://github.com/androguard/androguard">传送门</a>&nbsp;</u></span></p>
<h2><strong>4. APKTOOL</strong></h2>
<p>APKTool是GOOGLE提供的APK编译工具，能够反编译及回编译apk，同时安装反编译系统apk所需要的framework-res框架，清理上次反编译文件夹等功能。它可以完整解包APK，解包后你可以看到 APK 里面的声明文件、布局文件、图片资源文件、由 dex 解包出来的 smali 文件、语言文件等。如果你要汉化、修改界面、修改代码的话，apktool 可以帮你一站式完成。</p>
<p>特征：</p>
<blockquote><p>反编译资源文件到原始格式（包括resources.arsc，classes.dex，9.png以及XML等）；</p>
<p>将解码资源重建回二进制APK / JAR；</p>
<p>组织和处理依赖于框架资源的APK；</p>
<p>Smali调试（2.1.0中移除，被IdeaSmali取代）；</p>
<p>协助重复性任务；</p>
</blockquote>
<p>下载地址：<span style="color: windowtext;"><u><a href="http://code.google.com/p/android-apktool/">传送门</a>&nbsp;</u></span></p>
<h2><strong>5. AFE</strong></h2>
<p>AFE（Android Frameworkfor Exploitation）是一个开源项目，运行在Unix-based 的操作系统中，能够用来证明Android操作系统中存在安全漏洞，它还表明Android僵尸网络是能够存在的。使用AFE能够非常容易的自动创建一个Android平台的恶意软件，发现应用软件的漏洞（例如Leaking Content Providers，Insecure FileStorage，Directory Traversal等），以及在受感染的设备上执行任意命令。</p>
<p>AFE包含两个部分，PC端（以下称为AFE）和手机端（以下称为AFEServer）。AFE大部分是完全使用Python编写的。AFE是可扩展的，可以自由添加其他的模块或者将已有的工具移植到AFE框架下。AFEServer是一个在手机上运行的Android应用，用来和AFE的Python界面进行连接，执行AFE发送到手机的命令。</p>
<p>功能：</p>
<blockquote><p>完善的命令行界面；</p>
<p>发现应用漏洞；</p>
<p>自动化创建恶意应用；</p>
</blockquote>
<p>下载地址：<span style="color: windowtext;"><u><a href="https://github.com/appknox/AFE">传送门</a>&nbsp;</u></span></p>
<h2><strong>6. BYPASS SIGNATURE AND PERMISSION CHECKS FORIPCS</strong></h2>
<p>该工具通过使用Cydia Substrate为IPCs提供绕过签名和权限检查服务。</p>
<p><strong>关于Cydia Substrate</strong></p>
<p>Cydia Substrate是一个代码修改平台。它可以修改任何主进程的代码，不管是用Java还是C/C++（native代码）编写的。</p>
<p>下载地址：<span style="color: windowtext;"><u><a href="https://github.com/iSECPartners/Android-KillPermAndSigChecks">传送门</a>&nbsp;</u></span></p>
<h2><strong>7. ANDROID OPENDEBUG</strong></h2>
<p>该工具利用Cydia Substrate将所有的应用程序在设备上运行；一旦安装任意应用程序就会有一个debugger连接到它们。</p>
<p>注意：该工具只能在测试设备中使用！</p>
<p>下载地址：<span style="color: windowtext;"><u><a href="https://github.com/iSECPartners/Android-OpenDebug">传送门</a></u></span></p>
<h2><strong>8. DARE</strong></h2>
<p>Dare是宾州大学计算机系发布的apk逆向工程工具，可以将Android系统中使用的apk文件反编译为JavaClass文件，这些Class文件随后可以通过现有的Java工具（包括反编译）进行处理。目前支持Linux和Mac OS X中使用。</p>
<p>下载地址：<u><a href="http://siis.cse.psu.edu/dare/downloads.html">传送门</a></u></p>
<h2><strong>9. DEX2JAR</strong></h2>
<p>dex2jar是一个能操作Android的dalvik(.dex)文件格式和Java的(.class)的工具集合。包含以下几个功能</p>
<blockquote><p>dex-reader/writer：用于读写 DalvikExecutable (.dex) 文件格式. 包含一个简单的API(与<a href="https://sourceforge.net/p/dex2jar/wiki/Faq#markdown-header-want-to-read-dex-file-using-dex2jar"><span style="color: windowtext;">ASM</span></a>相似)；</p>
<p>d2j-dex2jar：执行dex到class的文件格式转换；</p>
<p>smali/baksmali：与smali工具功能一致，但是对中文更友好；</p>
<p>其他工具：<a href="https://sourceforge.net/p/dex2jar/wiki/DecryptStrings"><span style="color: windowtext;">字符串解密</span></a></p>
</blockquote>
<p>下载地址：<span style="color: windowtext;"><u><a href="https://sourceforge.net/projects/dex2jar/">传送门</a>&nbsp;</u></span></p>
<h2><strong>10. ENJARIFY</strong></h2>
<p>Enjarify是由Google推出的一款基于Python3开发，类似dex2jar的反编译工具，它可以将Dalvik字节码转换成相对应的Java字节码，有比dex2jar更优秀的兼容性，准确性及更高的效率。</p>
<p>下载地址：<span style="color: windowtext;"><u><a href="https://github.com/google/enjarify">传送门</a>&nbsp;</u></span></p>
<h2><strong>11. DEDEXER</strong></h2>
<p>Dedexer是一款反编译dex文件的开源工具。特征包含：</p>
<blockquote><p>不需要在android模拟器中运行；</p>
<p>能够将dex文件按照java源代码package的目录结构建好了目录，每个class文件对应一个ddx文件；</p>
<p>可作为像jasmin一样的反编译引擎；</p>
</blockquote>
<p>下载地址：<span style="color: windowtext;"><u><a href="https://sourceforge.net/projects/dedexer/">传送门</a>&nbsp;</u></span></p>
<h2><strong>12. FINO</strong></h2>
<p>一款Android动态分析工具。</p>
<p>下载地址：<a href="https://github.com/sysdream/fino">传送门</a></p>
<h2><strong>13. INDROID</strong></h2>
<p>该项目的目的是证实在nix 系统a.k.a ptrace函数上的一个简单的调试功能可以被恶意软件滥用，在远程进程中注入恶意代码。Indroid为基于ARM的 nix设备提供创建远程线程（CreateRemoteThread）。</p>
<p>如果你想更深入地了解该框架，可以点击如下链接：</p>
<p>观看Defcon 19相关视频：<a href="http://www.youtube.com/watchv=vju6tq1lp0k">传送门</a></p>
<p>查看报告详情：<a href="http://www.slideshare.net/null0x00/project-jugaad">传送门</a></p>
<p>CreateRemoteThread是创建一个在其它进程地址空间中运行的线程(也称创建远程线程)。</p>
<h2><strong>14. INTENT SNIFFER</strong></h2>
<p>Intent Sniffer工具可以在任何运行谷歌Android操作系统的设备上使用。在Android平台中，Intent是应用程序之间进行通信的最常用的方式之一，Intent Sniffer工具实现监控运行时路由的广播Intent，也就是在系统上的应用程序之间发送的Intent。它并不监控显式广播的Intent，而是默认为（大多数情况下）无优先权的广播。</p>
<p>该工具也能够针对那些基于应用反射和动态审查安装程序的Intent来动态升级扫描的Action和Category。</p>
<p>下载地址：<a href="https://www.isecpartners.com/media/4589/intentsniffer.zip">传送门</a></p>
<h2><strong>15. INTROSPY</strong></h2>
<p>Introspy是一款黑盒测试工具，帮助我们理解Android应用程序在运行时的行为，协助我们识别潜在的安全问题。</p>
<p>下载地址：<a href="https://github.com/iSECPartners/Introspy-iOS/releases">传送门</a></p>
<h2><strong>16. JAD</strong></h2>
<p>JAD是一款Java反编译工具，可以通过命令行把Java的class文件反编译成源代码。</p>
<p>下载地址：<a href="http://www.varaneckas.com/jad">传送门</a></p>
<h2><strong>17. JD-GUI</strong></h2>
<p>JD-GUI是一个独立的显示“.class” 文件Java源代码的图形用户界面工具。用户可以使用JD-GUI浏览和重建源代码的即时访问方法和字段，以代码高度方式来显示反编译过来的代码。</p>
<p>下载地址：<a href="http://jd.benow.ca/jd-gui/downloads/#jd-gui">传送门</a></p>
<h2><strong>18. CFR</strong></h2>
<p>CFR(Class File Reader)，Java反编译器，支持Java 8的lamda表达式，Java 7 的字符串转换等，开发者为LeeBenfield。</p>
<p>下载地址：<a href="http://www.benf.org/other/cfr/">传送门</a></p>
<h2><strong>19. KRAKATAU</strong></h2>
<p>Krakatau开发者为Storyyeller，目前主要包含三个工具——java类文件的反编译和反汇编工具，创建类文件的汇编工具。</p>
<p>下载地址：<a href="https://github.com/Storyyeller/Krakatau" target="_blank">传送门</a></p>
<h2><strong>20. PROCYON</strong></h2>
<p>Java反编译器和元编程框架Procyon可以在反编译工具中立足，显然是具有其独到优势的。它有进行控制流分析，以及类型推断，也支持java8特性，其开发者为Mike Strobel。</p>
<p>下载地址：<a href="https://bitbucket.org/mstrobel/procyon/downloads">传送门</a></p>
<h2><strong>21. FERNFLOWER</strong></h2>
<p>Fernflower是一个对Java程序进行反编译分析的利器。目前正处于开发阶段，如有bug报告和改进建议可发送邮件至fernflower.decompiler@gmail.com</p>
<p>下载地址：<a href="https://github.com/MinecraftForge/FernFlower">传送门</a></p>
<h2><strong>22. REDEXER</strong></h2>
<p>Redexer是Dalvik 字节码（用于安卓APP）分析框架，它是一套基于OCaml的实用工具，帮助程序员解析，操作Dalvik虚拟机。Redexer由来自马里兰大学帕克分校的PLUM组织开发完成，主要作者是：Jinseong Jeon，Kristopher Micinski以及Jeff Foster。</p>
<p><strong>关于OCaml</strong></p>
<p>OCaml是Caml编程语言的主要实现，由XavierLeroy，Jérme Vouillon，Damien Doligez，Didier Rémy及其他人于1996年创立。</p>
<p>下载地址：<a href="https://github.com/plum-umd/redexer">传送门</a></p>
<h2><strong>23. SIMPLIFY安卓反混淆工具</strong></h2>
<p>Simplify安卓反混淆工具实际上是通过执行一个APP来解读其行为，随后尝试通过优化代码来实现行为一致，但是更容易被人理解的目的。每一种优化类型都是非常简单通用的，所以无论用的是什么特殊类型的混淆技术都没关系。其主要由3部分组成：smalivm，simplify以及demo app。</p>
<p>下载地址：<u><a href="https://github.com/CalebFenton/simplify">传送门</a></u></p>
<h2><strong>24. BYTECODE VIEWER</strong></h2>
<p>Bytecode Viewer是一个高级的轻量级Java字节码查看器，GUIProcyon Java 反编译器, GUI CFR Java 反编译器, GUI FernFlower Java 反编译器, GUI Jar-Jar, Hex 查器看, 代码搜索器, 调试器等。</p>
<p>这款开源工具完全采用Java编程语言进行开发。这款工具由Konloch设计并开发，目前也主要是Konloch正在维护这一开源项目。</p>
<p>在这款工具中，还设计有一个插件系统，它可以允许你与加载的类文件进行交互。比如说，你可以写一个字符串的反混淆工具，恶意代码搜索器，或者其他的一些你所能想到的东西。</p>
<p>你不仅可以使用一个他人预先编写完成的插件，而且你也可以使用你自己写的插件。不仅如此，它还支持使用Groovy脚本，Python脚本，以及Ruby脚本。当插件状态被激活之后，它会将每一个单独的类文件加载进BCV中，这样一来，用户就可以使用ASM来控制这些加载的类文件了。</p>
<p>下载地址：<a href="https://github.com/konloch/bytecode-viewer">传送门</a></p>
<h2><strong>25. RADARE2</strong></h2>
<p>radare2是一款开放源代码的逆向工程平台，它可以反汇编、调试、分析和操作二进制文件。</p>
<p>主要特点：</p>
<blockquote><p>多平台多架构的；</p>
<p>高度脚本； </p>
<p>十六进制编辑器； </p>
<p>IO包裹； </p>
<p>文件系统支持； </p>
<p>调试器支持等；</p>
</blockquote>
<p>下载地址：<a href="https://github.com/radare/radare2">传送门</a></p>
<h2><strong>26. JEB FOR ANDROID</strong></h2>
<p>JEB是一个功能强大的为安全专业人士设计的Android应用程序的反编译工具。用于逆向工程或审计APK文件，可以提高效率减少许多工程师的分析时间。</p>
<p>特征表现为：</p>
<blockquote><p>全面的Dalvik反编译器；</p>
<p>交互性；</p>
<p>可全面测试APK文件内容；</p>
<p>多平台（支持Windows， Linux和Mac等操作系统）</p>
</blockquote>
<p>官网地址：<u><a href="https://www.pnfsoftware.com/">传送门</a></u></p>
<p>下载地址：<a href="https://www.pnfsoftware.com/jeb2/#android" target="_blank">传送门</a></p>