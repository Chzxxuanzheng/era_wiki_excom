<div style="display:none">

这个东西是用MarkDown语法写的,当你看到这句话时说明你并没有以正确的方式打开,edge浏览器上有阅读MarkDown的插件,vscode也有阅读MarkDown的插件

</div>

# era basic excom汉化

# 前言

对wiki的[excom](https://wiki.eragames.rip/index.php/Emuera/excom)进行翻译,并根据自身理解添加了一些示例

该文本主要用于查奇奇怪怪的命令,不适合也不能够用作新手教程

该文本的命令并不全,不过译者找不到比它整理的更全的命令说明
反正译者遇到不懂的命令都是在这里找的

感谢噫啊诶歪M汉化小群兼瞎聊群提供的帮助

*--by Mr.Lee*

# 目录

> ### 1	[PRINT系](#1)
> ###### 1.1	[PRINT(|V|S|FORM|FORMS)(|K|D)(|L|W)](#1.1)
> ###### 1.2	[PRINTSINGLE(|V|S|FORM|FORMS)(|K|D)](#1.2)
> ###### 1.3	[PRINT(|FORM)(C|LC)(|K|D)](#1.3)
> ###### 1.4	[PRINTDATA(|K|D)(|L|W)](#1.4)
> ###### 1.5	[PRINTBUTTON(|C|LC) <字符串表达式>, <整形 或 字符串表达式>](#1.5)
> ###### 1.6	[PRINTPLAIN(|FORM)](#1.6)
> ###### 1.7	[CUSTOMDRAWLINE <字符串>](#1.7)
> ###### 1.8	[DRAWLINEFORM <格式化字符串>](#1.8)
> ###### 1.9	[REUSELASTLINE <格式化字符串>](#1.9)
> ###### 1.10	[CLEARLINE <整形 消除行数>](#1.10)
> ###### 1.11	[PRINT_IMG <字符串表达式 图像名>](#1.11)
> ###### 1.12	[PRINT_RECT <整形 长度>](#1.12)
> ###### 1.13	[PRINT_RECT <整形 x>, <整形 y>, <整形 宽>, <整形 高>](#1.13)
> ###### 1.14	[PRINT_SPACE <整形 长度>](#1.14)
> ### 2	[色彩·字体·显示规格操作](#2)
> ###### 2.1	[SETCOLOR <整形 R>, <整形 G>, <整形 B>](#2.1)
> ###### 2.2	[SETCOLOR <整形 RGB>](#2.2)
> ###### 2.3	[RESETCOLOR](#2.3)
> ###### 2.4	[SETBGCOLOR <整形 R>, <整形 G>, <整形 B>](#2.4)
> ###### 2.5	[SETBGCOLOR <整形 RGB>](#2.5)
> ###### 2.6	[RESETBGCOLOR](#2.6)
> ###### 2.7	[SETCOLORBYNAME <字符串>](#2.7)
> ###### 2.8	[SETBGCOLORBYNAME <字符串>](#2.8)
> ###### 2.9	[GETCOLOR](#2.9)
> ###### 2.10	[GETDEFCOLOR](#2.10)
> ###### 2.11	[GETBGCOLOR](#2.11)
> ###### 2.12	[GETDEFBGCOLOR](#2.12)
> ###### 2.13	[GETFOCUSCOLOR](#2.13)
> ###### 2.14	[FONTBOLD](#2.14)
> ###### 2.15	[FONTITALIC](#2.15)
> ###### 2.16	[FONTREGULAR](#2.16)
> ###### 2.17	[FONTSTYLE <整形>](#2.17)
> ###### 2.18	[GETSTYLE](#2.18)
> ###### 2.19	[CHKFONT <字符串表达式>](#2.19)
> ###### 2.20	[SETFONT <字符串表达式>](#2.20)
> ###### 2.21	[GETFONT](#2.21)
> ###### 2.22	[FORCEKANA <整形>](#2.22)
> ###### 2.23	[ALIGNMENT <字符串>](#2.23)
> ###### 2.24	[CURRENTALIGN](#2.24)
> ###### 2.25	[REDRAW <整形>](#2.25)
> ###### 2.26	[CURRENTREDRAW](#2.26)
> ###### 2.27	[PRINTCPERLINE](#2.27)
> ###### 2.28	[LINEISEMPTY](#2.28)
> ###### 2.29	[BARSTR <整形 変量>, <整形 最大値>, <整形 长度>](#2.29)
> ###### 2.30	[MONEYSTR <整形>{, <字符串表达式 指定格式>}](#2.30)
> ###### 2.31	[SKIPDISP <整形>](#2.31)
> ###### 2.32	[NOSKIP](#2.32)
> ###### 2.33	[ENDNOSKIP](#2.33)
> ###### 2.34	[ISSKIP](#2.34)
> ###### 2.35	[MOUSESKIP](#2.35)
> ### 3	[字符串操作・示例](#3)
> ###### 3.1	[TOUPPER <字符串表达式>](#3.1)
> ###### 3.2	[TOLOWER <字符串表达式>](#3.2)
> ###### 3.3	[TOHALF <字符串表达式>](#3.3)
> ###### 3.4	[TOFULL <字符串表达式>](#3.4)
> ###### 3.5	[TOSTR <整形>{, <字符串表达式 指定格式>}](#3.5)
> ###### 3.6	[ISNUMERIC <字符串表达式>](#3.6)
> ###### 3.7	[TOINT <字符串表达式>](#3.7)
> ###### 3.8	[STRLEN <字符串>](#3.8)
> ###### 3.9	[STRLENS <字符串表达式>](#3.9)
> ###### 3.10	[STRLENFORM <格式化字符串>](#3.10)
> ###### 3.11	[STRLENU <字符串>](#3.11)
> ###### 3.12	[STRLENSU <字符串表达式>](#3.12)
> ###### 3.13	[STRLENFORMU <格式化字符串>](#3.13)
> ###### 3.14	[SUBSTRING <字符串表达式>, <整形 起始>, <整形 结束>](#3.14)
> ###### 3.15	[SUBSTRINGU <字符串表达式>, <整形 起始>, <整形 结束>](#3.15)
> ###### 3.16	[CHARATU <字符串表达式>, <文字位置>](#3.16)
> ###### 3.17	[STRFIND <字符串表达式 检索对象>, <字符串表达式 要检索的字符串>{, <整形 起始索引>}](#3.17)
> ###### 3.18	[STRFINDU <字符串表达式 检索对象>, <字符串表达式 要检索的字符串>{ , <整形 起始索引>}](#3.18)
> ###### 3.19	[STRCOUNT <字符串表达式 检索对象>, <字符串表达式 要检索的字符串>](#3.19)
> ###### 3.20	[SPLIT <字符串表达式 被分割字符串>, <字符串表达式 分割标准>, <字符串表达式数组>](#3.20)
> ###### 3.21	[REPLACE <字符串表达式 替换对象>, <字符串表达式 要替换内容>, <字符串表达式 替换内容>](#3.21)
> ###### 3.22	[ESCAPE <字符串>](#3.22)
> ###### 3.23	[UNICODE <整形>](#3.23)
> ###### 3.24	[ENCODETOUNI <格式化字符串表达式 对象>](#3.24)
> ### 4	[运算](#4)
> ###### 4.1	[POWER <整形 结果>, <整形 底数>, <整形 指数>](#4.1)
> ###### 4.2	[ABS <整形>](#4.2)
> ###### 4.3	[SIGN <整形>](#4.3)
> ###### 4.4	[SQRT <整形>](#4.4)
> ###### 4.5	[GETBIT <整形 操作变量>, <整形 操作位置>](#4.5)
> ###### 4.6	[MAX <整形>(, <整形>...)](#4.6)
> ###### 4.7	[MIN <整形>(, <整形>...)](#4.7)
> ###### 4.8	[LIMIT <整形 值>, <整形 下限>, <整形 上限>](#4.8)
> ###### 4.9	[INRANGE <整形 值>, <整形 下限>, <整形 上限>](#4.9)
> ###### 4.10	[SETBIT <整形 操作变量>, <整形 操作位置>{, <整形 操作位置>,...}](#4.10)
> ###### 4.11	[CLEARBIT <整形 操作变量>, <整形 操作位置>{, <整形 操作位置>,...}](#4.11)
> ###### 4.12	[INVERTBIT <整形 操作变量>, <整形 操作位置>{, <整形 操作位置>,...}](#4.12)
> ### 5	[角色操作・示例](#5)
> ###### 5.1	[ADDCHARA <整形 角色番号1>{, <整形 角色番号2>, <整形 角色番号3>, ...}](#5.1)
> ###### 5.2	[DELCHARA <整形 角色番号1>{, <整形 角色番号2>, <整形 角色番号3>, ...}](#5.2)
> ###### 5.3	[SWAPCHARA <整形 角色番号1>, <整形 角色番号2>](#5.3)
> ###### 5.4	[SORTCHARA {<角色变量> , < FORWARD / BACK>}](#5.4)
> ###### 5.5	[GETCHARA <整形 角色番号(NO)>](#5.5)
> ###### 5.6	[ADDDEFCHARA](#5.6)
> ###### 5.7	[ADDVOIDCHARA](#5.7)
> ###### 5.8	[DELALLCHARA <整形 角色编号>](#5.8)
> ###### 5.9	[PICKUPCHARA <整形 角色编号>{, <整形 角色编号>, ....}](#5.9)
> ###### 5.10	[EXISTCSV <整形 角色番号>](#5.10)
> ###### 5.11	[FINDCHARA <角色变量>, <值>{, <整形 起始>, <整形 结束>}](#5.11)
> ###### 5.12	[FINDLASTCHARA <角色变量>, <值>{, <整形 起始>, <整形 结束>}](#5.12)
> ###### 5.13	[COPYCHARA <整形 角色编号>, <](#5.13)
> ###### 5.14	[ADDCOPYCHARA <整形 角色编号>](#5.14)
> ### 6	[变量操作・CSV读取・数组操作](#6)
> ##### 6.1	[VARSIZE <变量名>](#6.1)
> ##### 6.2	[RESETDATA](#6.2)
> ##### 6.3	[RESETGLOBAL](#6.3)
> ##### 6.4	[RESET_STAIN <整形 角色编号>](#6.4)
> ##### 6.5	[SWAP <変量1>, <変量2>](#6.5)
> ##### 6.6	[CSVNAME <整形 角色番号>](#6.6)
> ##### 6.7	[CSVCALLNAME <整形 角色番号>](#6.7)
> ##### 6.8	[CSVNICKNAME <整形 角色番号>](#6.8)
> ##### 6.9	[CSVMASTERNAME <整形 角色番号>](#6.9)
> ##### 6.10	[CSVBASE <整形 角色番号>, <整形 索引>](#6.10)
> ##### 6.11	[CSVCSTR <整形 角色番号>, <整形 索引>](#6.11)
> ##### 6.12	[CSVABL <整形 角色番号>, <整形 索引>](#6.12)
> ##### 6.13	[CSVTALENT <整形 角色番号>, <整形 索引>](#6.13)
> ##### 6.14	[CSVMARK <整形 角色番号>, <整形 索引>](#6.14)
> ##### 6.15	[CSVEXP <整形 角色番号>, <整形 索引>](#6.15)
> ##### 6.16	[CSVRELATION <整形 角色番号>, <整形 索引>, <整形 索引>](#6.16)
> ##### 6.17	[CSVJULE <整形 角色番号>, <整形 索引>](#6.17)
> ##### 6.18	[CSVEQUIP <整形 角色番号>, <整形 索引>](#6.18)
> ##### 6.19	[CSVCFLAG <整形 角色番号>, <整形 索引>](#6.19)
> ##### 6.20	[GETNUM < CSV名>, < 字符串表达式>](#6.20)
> ##### 6.21	[GETPALAMLV <整形>, <整形 上限>](#6.21)
> ##### 6.22	[GETEXPLV <整形>, <整形 上限>](#6.22)
> ##### 6.23	[FINDELEMENT <变量名>, <要检索的内容(类型必须与变量相同)>{, <起始位置>, <中止位置+1>, <整形 字符串完全一致>}](#6.23)
> ##### 6.24	[FINDLASTELEMENT <变量名>, <要检索的内容(类型必须与变量相同)>{, <起始位置>, <中止位置+1>, <整形 字符串完全一致>}](#6.24)
> ##### 6.25	[VARSET <变量名>{, <整形 or 字符串式>, <起始位置>, <中止位置+1>}](#6.25)
> ##### 6.26	[CVARSET <角色变量名>{, <索引>, <值>, <起始角色编号>, <结束角色编号+1>}](#6.26)
> ##### 6.27	[ARRAYSHIFT <对象变量>, <整形 错开位数>, <偏移后的空白区域的初始值>{, <整形 起始位置>, <整形 结束位置>}](#6.27)
> ##### 6.28	[ARRAYREMOVE <对象变量>, <整形 起始位置>, <整形 删除个数>](#6.28)
> ##### 6.29	[ARRAYSORT <对象变量>{, <排序方式(FORWARD or BACK)>, <起始索引>, <整形 对象元素数>}](#6.29)
> ##### 6.30	[ARRAYCOPY <字符串表达式 原始变量名>, <字符串表达式 目标变量名>](#6.30)
> ##### 6.31	[ARRAYMSORT <数组1>{, <数组2>...}](#6.31)
> ##### 6.32	[CUPCHECK <整形 登录角色的编号>](#6.32)
> ### 7	[读写操作](#7)
> ###### 7.1	[SAVEDATA <整形 存档编号>, <字符串表达式 备注信息>](#7.1)
> ###### 7.2	[LOADDATA <整形 存档编号>](#7.2)
> ###### 7.3	[DELDATA <整形 存档编号>](#7.3)
> ###### 7.4	[CHKDATA <整形 存档编号>](#7.4)
> ###### 7.5	[SAVENOS <整形>](#7.5)
> ###### 7.6	[SAVEGLOBAL](#7.6)
> ###### 7.7	[LOADGLOBAL](#7.7)
> ###### 7.8	[OUTPUTLOG](#7.8)
> ###### 7.9	[SAVECHARA <字符串表达式 文件名>, <字符串表达式 备注信息>, <整形 角色1登录编号>{, <整形 角色2登录编号>, ...}](#7.9)
> ###### 7.10 [LOADCHARA <字符串表达式 文件名>](#7.10)
> ###### 7.11 [CHKCHARADATA <字符串表达式 文件名>](#7.11)
> ###### 7.12 [FIND_CHARADATA <字符串表达式 文件名>](#7.12)
> ###### 7.13 [SAVETEXT <字符串表达式 文本内容>, <整形 文件编号>{, <整形 保存在sav文件夹>, <整形 用UTF-8编码>}](#7.13)
> ###### 7.14 [LOADTEXT <整形 文件编号>{, <整形 保存在sav文件夹>, <整形 用UTF-8编码>}](#7.14)
> ### 8	[日期・时间取得](#8)
> ###### 8.1	[GETTIME](#8.1)
> ###### 8.2	[GETMILLISECOND](#8.2)
> ###### 8.3	[GETSECOND](#8.3)
> ### 9	[输入・WAIT](#9)
> ###### 9.1	[FORCEWAIT](#9.1)
> ###### 9.2	[INPUT {<整形 默认值>}](#9.2)
> ###### 9.3	[INPUTS {< 字符串 默认值>}](#9.3)
> ###### 9.4	[TINPUT <整形 时间(ms)>, <整形 超时返回值>{, <整形 显示剩余时间> = 1, < 字符串表达式 超时文本>}](#9.4)
> ###### 9.5	[TINPUTS <整形 时间(ms)>, <字符串表达式 超时返回值>{, <整形 显示剩余时间> = 1, < 字符串表达式 超时文本>}](#9.5)
> ###### 9.6	[TWAIT <整形 时间(ms)>, <整形 接受输入标志>](#9.6)
> ###### 9.7	[ONEINPUT {<整形 默认值>}](#9.7)
> ###### 9.8	[ONEINPUTS {< 字符串表达式 默认值>}](#9.8)
> ###### 9.9	[TONEINPUT <整形 时间(ms)>, <整形 超时返回值>{, <整形 显示剩余时间> = 1, < 字符串表达式 超时文本>}](#9.9)
> ###### 9.10	[TONEINPUTS <整形 时间(ms)>, < 字符串表达式 超时返回值>{, <整形 显示剩余时间> = 1, < 字符串表达式 超时文本>}</font></h4>](#9.10)
> ###### 9.11	[WAITANYKEY</font></h4>](#9.11)
> ###### 9.12	[INPUTMOUSEKEY {<整形 时间(ms)>}</font></h4>](#9.12)
> ### 10	[循环](#10)
> ###### 10.1	[FOR <整形变量>, <整形 起始>, <整形 中止>{, <整形 步长> = 1}](#10.1)
> ###### 10.2	[NEXT](#10.2)
> ###### 10.3	[WHILE <条件>](#10.3)
> ###### 10.4	[WEND](#10.4)
> ###### 10.5	[DO](#10.5)
> ###### 10.6	[LOOP <条件>](#10.6)
> ###### 10.7	[SELECTCASE <变量>](#10.7)
> ###### 10.8	[CASE < CASE 判定条件>{, < CASE 判定条件>, < CASE 判定条件> ……} <条件>](#10.8)
> ###### 10.9	[CASEELSE <条件>](#10.9)
> ###### 10.10	[ENDSELECT <条件>](#10.10)
> ### 11	[随机数生成](#11)
> ###### 11.1	[RANDOMIZE <整形>](#11.1)
> ###### 11.2	[DUMPRAND](#11.2)
> ###### 11.3	[INITRAND](#11.3)
> ### 12	[流程控制・调试辅助](#12)
> ###### 12.1	[BEGIN <关键字>](#12.1)
> ###### 12.2	[CALLTRAIN <整形 COM编号>](#12.2)
> ###### 12.3	[DOTRAIN <整形>](#12.3)
> ###### 12.4	[THROW <格式字符串>](#12.4)
> ### 13	[CALL・JUMP・GOTO系](#13)
> ###### 13.1	[TRYJUMP <字符串 函数名> {, <参数1>, <参数2>……}](#13.1)
> ###### 13.2	[TRYCALL <字符串 函数名> {, <参数1>, <参数2>……}](#13.2)
> ###### 13.3	[TRYGOTO <字符串 函数名>](#13.3)
> ###### 13.4	[JUMPFORM <格式化字符串 函数名> {, <参数1>, <参数2>……}](#13.4)
> ###### 13.5	[CALLFORM <格式化字符串 函数名> {, <参数1>, <参数2>……}](#13.5)
> ###### 13.6	[GOTOFORM <格式化字符串 函数名>](#13.6)
> ###### 13.7	[TRYJUMPFORM <格式化字符串 函数名> {, <参数1>, <参数2>……}](#13.7)
> ###### 13.8	[TRYCALLFORM <格式化字符串 函数名> {, <参数1>, <参数2>……}](#13.8)
> ###### 13.9	[TRYGOTOFORM <格式化字符串 函数名>](#13.9)
> ###### 13.10	[CALLF <字符串 函数名> {, <参数1>, <参数2>……}](#13.10)
> ###### 13.11	[CALLFORMF <字符串 函数名> {, <参数1>, <参数2>……}](#13.11)
> ###### 13.12	[CALLEVENT <字符串 函数名>](#13.12)
> ### 14	[CALL・JUMP・GOTO系2 (TRYC-CATCH-ENDCATCH)](#14)
> ###### 14.1	[TRYCJUMP <字符串 函数名> {, <参数1>, <参数2>……}](#14.1)
> ###### 14.2	[TRYCCALL <字符串 函数名> {, <参数1>, <参数2>……}](#14.2)
> ###### 14.3	[TRYCGOTO <字符串 函数名>](#14.3)
> ###### 14.4	[TRYCJUMPFORM <格式字符串 函数名> {, <参数1>, <参数2>……}](#14.4)
> ###### 14.5	[TRYCCALLFORM <格式字符串 函数名> {, <参数1>, <参数2>……}](#14.5)
> ###### 14.6	[TRYCGOTOFORM <格式字符串 函数名>](#14.6)
> ###### 14.7	[CATCH](#14.7)
> ###### 14.8	[ENDCATCH](#14.8)
> ###### 14.9	[TRYCALLLIST](#14.9)
> ###### 14.10	[TRYJUMPLIST</font></h4>](#14.10)
> ###### 14.11	[TRYGOTOLIST</font></h4>](#14.11)
> ###### 14.12	[FUNC <字符串 函数名> {, <参数1>, <参数2>……}</font></h4>](#14.12)
> ###### 14.13	[ENDFUNC</font></h4>](#14.13)
> ### 15	[RETURN系](#15)
> ###### 15.1	[RETURN <整形>{, <整形>, <整形>, ...}](#15.1)
> ###### 15.2	[RETURNFORM <格式字符串>{，<格式字符串>，<格式字符串>，…}](#15.2)
> ###### 15.3	[RETURNF <表达式>](#15.3)
> ### 16	[DEBUG系](#16)
> ###### 16.1	[DEBUGPRINT <字符串>](#16.1)
> ###### 16.2	[DEBUGPRINTL <字符串>](#16.2)
> ###### 16.3	[DEBUGPRINTFORM <格式化字符串>](#16.3)
> ###### 16.4	[DEBUGPRINTFORML <格式化字符串>](#16.4)
> ###### 16.5	[DEBUGCLEAR](#16.5)
> ###### 16.6	[ASSERT <整形>](#16.6)
> ### 17	[提示工具系](#17)
> ###### 17.1	[TOOLTIP_SETCOLOR <整形>, <整形>](#17.1)
> ###### 17.2	[TOOLTIP_SETDELAY <整形>](#17.2)
> ###### 17.3	[TOOLTIP_SETDURATION <整形 显示时间>](#17.3)
> ### 18	[HTML系](#18)
> ###### 18.1	[HTML_PRINT <字符串表达式>](#18.1)
> ###### 18.2	[HTML_TAGSPLIT <字符串表达式>{, <整形变量>, <字符串变量>}](#18.2)
> ### 19	[AWAIT相关](#19)
> ###### 19.1	[AWAIT {<整形 等待时间(ms)>}](#19.1)
> ###### 19.2	[GETKEY <整形 按键代码>](#19.2)
> ###### 19.3	[GETKEYTRIGGERED <整形 按键代码>](#19.3)
> ###### 19.4	[MOUSEX](#19.4)
> ###### 19.5	[MOUSEY](#19.5)
> ###### 19.6	[ISACTIVE](#19.6)
> ### 20	[图像处理相关](#20)
> ###### 20.1	[GCREATE <整形 ID>, <整形 宽>, <整形 高>](#20.1)
> ###### 20.2	[GCREATEFROMFILE <整形 ID>, <字符串表达式 文件位置>](#20.2)
> ###### 20.3	[GDISPOSE <整形 ID>](#20.3)
> ###### 20.4	[GCLEAR <整形 ID> <整形 cARGB>](#20.4)
> ###### 20.5	[GFILLRECTANGLE <整形 ID>, <整形 x>, <整形 y>, <整形 宽>, <整形 高>](#20.5)
> ###### 20.6	[GDRAWG <整形 桌面ID>, <整形 源图像ID>, <整形 桌面X>, <整形 桌面Y>, <整形 桌面宽>, <整形 桌面高>, <整形 源图像X>, <整形 源图像Y>, <整形 源图像宽>, <整形 源图像高>](#20.6)
> ###### 20.7	[GDRAWG <整形 桌面ID>, <整形 源图像ID>, <整形 桌面X>, <整形 桌面Y>, <整形 桌面宽>, <整形 桌面高>, <整形 源图像X>, <整形 源图像Y>, <整形 源图像宽>, <整形 源图像高>, <整形 颜色矩阵>](#20.7)
> ###### 20.8	[GDRAWGWITHMASK <整形 桌面ID>, <整形 源图像ID>, <整形 蒙版ID>, <整形 桌面X>, <整形 桌面Y>](#20.8)
> ###### 20.9	[GDRAWSPRITE <整形 桌面ID>, <字符串表达式 雪碧图>](#20.9)
> ###### 20.10	[GDRAWSPRITE <整形 桌面ID>, <字符串表达式 雪碧图>, <整形 桌面X>, <整形 桌面Y>](#20.10)
> ###### 20.11	[GDRAWSPRITE <整形 桌面ID>, <字符串表达式 雪碧图>, <整形 桌面X>, <整形 桌面Y>, <整形 桌面宽>, <整形 桌面高>](#20.11)
> ###### 20.12	[GDRAWSPRITE <整形 桌面ID>, <字符串表达式 雪碧图>, <整形 桌面X>, <整形 桌面Y>, <整形 桌面宽>, <整形 桌面高>, <整形 颜色矩阵>](#20.12)
> ###### 20.13	[GSETCOLOR <整形 ID>, <整形 cARGB>, <整形 X>, <整形 y>](#20.13)
> ###### 20.14	[GSETBRUSH <整形 ID>, <整形 cARGB>](#20.14)
> ###### 20.15	[GSETFONT <整形 ID>, <字符串表达式 字体名>, <整形 字体大小>](#20.15)
> ###### 20.16	[GSETPEN <整形 ID>, <整形 cARGB>, <整形 宽度>](#20.16)
> ###### 20.17	[GCREATED <整形 ID>](#20.17)
> ###### 20.18	[GWIDTH <整形 ID>](#20.18)
> ###### 20.19	[GHEIGHT <整形 ID>](#20.19)
> ###### 20.20	[GGETCOLOR <整形 ID>, <整形 X>, <整形 Y>](#20.20)
> ###### 20.21	[GSAVE <整形 ID>, <整形 文件编号>](#20.21)
> ###### 20.22	[GLOAD <整形 ID>, <整形 文件编号>](#20.22)
> ###### 20.23	[SPRITECREATE <字符串表达式 雪碧图名>, <整形 ID>](#20.23)
> ###### 20.24	[SPRITECREATE <字符串表达式 雪碧图名>, <整形 ID>, <整形 X>, <整形 Y>, <整形 宽>, <整形 高>](#20.24)
> ###### 20.25	[SPRITEANIMECREATE <字符串表达式 雪碧图名>, <整形 宽>, <整形 高>](#20.25)
> ###### 20.26	[SPRITEANIMEADDFRAME <字符串表达式 雪碧图名>, <整形 ID>, <整形 X>, <整形 Y>, <整形 宽>, <整形 高>, <整形 雪碧图X>, <整形 雪碧图Y>, <整形 时间(ms)>](#20.26)
> ###### 20.27	[SPRITEDISPOSE <字符串表达式 雪碧图名>](#20.27)
> ###### 20.28	[SPRITEGETCOLOR <字符串表达式 雪碧图名>, <整形 X>, <整形 Y>](#20.28)
> ###### 20.29	[SPRITECREATED <字符串表达式 雪碧图名>](#20.29)
> ###### 20.30	[SPRITEWIDTH <字符串表达式 雪碧图名>](#20.30)
> ###### 20.31	[SPRITEHEIGHT <字符串表达式 雪碧图名>](#20.31)
> ###### 20.32	[SPRITEPOSX <字符串表达式 雪碧图名>](#20.32)
> ###### 20.33	[SPRITEPOSY <字符串表达式 雪碧图名>](#20.33)
> ###### 20.34	[SPRITESETPOS <字符串表达式 雪碧图名>, <整形 X>, <整形 Y>](#20.34)
> ###### 20.35	[SPRITEMOVE <字符串表达式 雪碧图名>, <整形 X>, <整形 Y>](#20.35)
> ###### 20.36	[CBGSETG <整形 ID>, <整形 X>, <整形 Y>, <整形 Z>](#20.36)
> ###### 20.37	[20.37 CBGSETSPRITE <字符串表达式 雪碧图名>, <整形 X>, <整形 Y>, <整形 Z>](#20.37)
> ###### 20.38	[CBGCLEAR](#20.38)
> ###### 20.39	[CBGCLEARBUTTON](#20.39)
> ###### 20.40	[CBGREMOVERANGE <整形 Zmin>, <整形 Zmax>](#20.40)
> ###### 20.41	[CBGREMOVEBMAP](#20.41)
> ###### 20.42	[CBGSETBMAPG <整形 ID>](#20.42)
> ###### 20.43	[CBGSETBUTTONSPRITE <整形 按钮值>, <字符串表达式 雪碧图名A>, <字符串表达式 雪碧图名B>, <整形 X>, <整形 Y>, <整形 Z>](#20.43)
> ###### 20.44	[CBGSETBUTTONSPRITE <整形 按钮值>, <字符串表达式 雪碧图名A>, <字符串表达式 雪碧图名B>, <整形 X>, <整形 Y>, <整形 Z>, <格式化字符串 提示工具>](#20.44)
> ###### 20.45	[SETANIMETIMER <整形 时间(ms)>](#20.45)
> ### 21	[未整理項目](#21)
> ###### 21.1	[CLEARTEXTBOX](#21.1)
> ###### 21.2	[STRDATA](#21.2)
> ###### 21.3	[STOPCALLTRAIN](#21.3)

## 正文

<h3 id="1"><font color=MidNightBlue>1 PRINT系</font></h3>
<h4 id="1.1"><font color=MediumBlue>1.1 PRINT(|V|S|FORM|FORMS)(|K|D)(|L|W)</font></h4>

PRINT系是系统的基本命令  

第1个括号内关键字指定变量类型
无 - (\<字符串\>)
V - (<变量> <变量> ,<变量> ……)
S - \<字符串表达式\>
FORM - (<格式化字符串>)
FORMS - <格式化字符串表达式>

###### 示例

	LOCAL = 495
	LOCALS:0 = 测试内容 1, \%LOCALS:1\%
	LOCALS:1 = 测试内容 2

	;打印字符串
	PRINTL LOCALS:0, %LOCALS:0%
	PRINTFORML LOCALS:0, %LOCALS:0%
	PRINTL

	;打印字符串表达式
	PRINTSL LOCALS:0
	PRINTFORMSL LOCALS:0
	PRINTL

	;打印变量
	PRINTVL 495 	;因为495相等于一个整形变量的值,所以不会报错
	PRINTVL LOCAL
	PRINTVL "四百九十五年的波纹"
	PRINTVL LOCALS:0, LOCALS:1
	PRINTL

	;错误写法,报错
	PRINTSL 测试内容4
	PRINTFORMS 测试内容 4
结果

	LOCALS:0, %LOCALS:0%
	LOCALS:0, 测试内容 1, %LOCALS:1%
	
	测试内容 1, %LOCALS:1%
	测试内容 1, 测试内容 2
	
	495
	495
	四百九十五年的波纹
	测试内容 1, %LOCALS:1%测试内容 2

	报错:
	错误内容：无法被解析的标示符"测试内容4"

第2个括号中的关键字K指定[FORCEKANA](#2.22)指令的应用。还有关键字"D"指定无视[SETCOLOR](#2.1)指令。ve> r1.736现在不能同时指定D和K

* 无 - 无视FORCEKANA,使用[SETCOLOR](#2.1)指定的颜色
* K - 用[FORCEKANA](#2.22)来描绘
* D - 无视[SETCOLOR](#2.1)

第3个括号指定打印后是否换行或者WAIT

* 无 - 不换行也不执行WAIT
* L - PRINT后换行
* W - PRINT后执行WAIT命令

例如PRINTSDW，你可以使用指定<字符串表达式>作为参数,无视[SETCOLOR](#2.1),并在打印后暂停
<br/>

<h4 id="1.2"><font color=MediumBlue>1.2 PRINTSINGLE(|V|S|FORM|FORMS)(|K|D)</font></h4>

PRINTSINGLE系与PRINTL系基本相同.但PRINT在文字超出窗口大小时会换行继续打印,而PRINTSINGLE不会

超过画面边缘的文字不会被打印
打印完自动换行,关键字作用和PRINT一样
<br/>
<h4 id="1.3"><font color=MediumBlue>1.3 PRINT(|FORM)(C|LC)(|K|D)</font></h4>

PRINTC系命令
会自动补充半角空格的命令,直至输出文字数为PRINTC指定的文字数(默认25)
另外,Emuera在打印的字符串的按钮化处理中,对PRINTC类命令有些特别处理

第1个括号中的关键词指定自变量类型
* 无 - \<字符串>
* FORM - <格式化字符串>

第2个括号内的关键词指定对齐位置。

* C - 右对齐(左側用半角空格补充)
* LC - 左对齐(右側用半角空格补充)

第2个括号内的关键词K,D作用与PRINT相同
<br/>
<h4 id="1.4"><font color=MediumBlue>1.4 PRINTDATA(|K|D)(|L|W)</font></h4>

PRINTDATA系命令,wiki摘自私家改造版的readme

###### 示例:

	PRINTDATA (整形变量)
		DATA (字符串)
		DATAFORM (格式化字符串)
		DATALIST
			(DATA / DATAFORM)
			(DATA / DATAFORM)
			...
		ENDLIST
	ENDDATA
> 说明:
> 　　DATA、DATAFORM和DATALIST～ENDLIST的字符> 随机显示
> 　　不使用IF和RAND就可以实现随机显示
> 　　DATA的索引会赋值给整形变量
> 　　方便你对相应的字符串进行处理
> 　　DATALIST～ENDLIST中的(DATA / DATAFORM)> 当于1行

K,D,L,W关键字的效果与打印系统相同。
PRINTDATA ~ ENDDATA内部没有内容时,什么也不做继续进行
PRINTDATA ~ ENDDATA,以及DATALIST ~ ENDLIST内不能使用上述以外的语法

译者的理解
###### 示例:

	PRINTDATA LOCAL
		DATAFORM 测试内容1
		DATAFORM 测试内容2
		DATAFORM 测试内容3
		DATALIST
			DATAFORM 测试内容4
		ENDLIST
		DATALIST
			DATAFORM 测试内容{LOCAL}
			DATA 测试内容5
		ENDLIST
	ENDDATA

等价于:

	IF RAND:5 == 0
		PRINTFORM 测试内容1
		LOCAL = 0
	ELSEIF RAND:4 == 0
		PRINTFORM 测试内容2
		LOCAL = 1
	ELSEIF RAND:3 == 0
		PRINTFORM 测试内容3
		LOCAL = 2
	ELSEIF RAND:2 == 0
		PRINTFORM 测试内容4
		LOCAL = 3
	ELSE
		PRINTFORML 测试内容{LOCAL}
		PRINT 测试内容5
		LOCAL = 4
	ENDIF

译者测试时,L,W等关键词不可用(可能是我的emuera太老了把).PRINTDATA里面DATAFORM,DATA,DATALIST,ENDLIST以外的语句会被忽视(是不是可以不用[SKIPSTART]来写注释了?)
但PRINTDATA里面不能进行数据处理,有点可惜
<br/>
<h4 id="1.5"><font color=MediumBlue>1.5 PRINTBUTTON(|C|LC) <字符串表达式>, <整形 或 字符串表达式></font></h4>

PRINTBUTTON指令是用来生成可以用鼠标点击的按钮的指令。
格式与PRINTS指令相近，但第二参数，指定点击时输入的数字或字符串。如果你的第一个参数中有换行，它将被限制,不会执行换行

在中Emuera像"[300] 保存"这样用[]包裹数字时,会自动连同周围的字符串被识别成按钮
PRINTBUTTON是为了强制生成这样的按钮
这个命令例如在以下的情况下有用

	PRINT 这样可以吗? [0] 确定	 [1] 取消
	INPUT

Emuera的自动识别会把"这样可以吗? [0] 确定"识别为一个按钮,"[1] 取消"识别为一个按钮
用PRINTBUTTON写的话就可以解决问题了

	PRINTS "这样可以吗? "
	PRINTBUTTON "[0] 确定", 0
	PRINTS "	  "
	PRINTBUTTON "[1] 取消", 1
	INPUT

(用PRINTS来代替PRINT指令，是为了明确半角空格的数量)
这样一来，"这样可以吗? "不再是按钮,"[0] 确定","[1] 取消"是按钮。
另外,在PRITNBUTTON命令中显示的"[0]"和"[1]"不是必须的,但是如果完全不显示对应的数字,会让用键盘操作的人感到困惑

另外，PRINTBUTTON指令不仅可以创建输入数字的按钮，还可以创建输入字码串的。然后你可以在执行INPUTS指令时点击按钮

	PRINTL 请输入名字
	PRINTBUTTON "[阿巴阿巴] ", "阿巴阿巴"
	PRINTBUTTON "[巴拉巴拉] ", "巴拉巴拉"
	PRINTBUTTON "[风华] ", "风华"
	INPUTS

括号内关键字代表对齐位置

* 无 - 不对齐
* C - 和PRINTC一样,右对齐
* LC - 和PRINTLC一样,左对齐

<br/>
<h4 id="1.6"><font color=MediumBlue>1.6 PRINTPLAIN(|FORM)</font></h4>

打印字符串,打印内容不会被识别为按钮
###### 示例

	PRINTL [0] 开始游戏 [1] 退出
	PRINTPLAIN 当你点击 [1] 退出 时游戏会退出
	INPUT

括号内关键字指定自变量类型

* 无 - <字符串>
* FORM - <格式化字符串>

<br/>
<h4 id="1.7"><font color=MediumBlue>1.7 CUSTOMDRAWLINE <字符串></font></h4>
<h4 id="1.8"><font color=MediumBlue>1.8 DRAWLINEFORM <格式化字符串></font></h4>

使用指定的字符串显示一行的分隔。DRAWLINEFORM为对应的FORM语法

<br/>
<h4 id="1.9"><font color=MediumBlue>1.9 REUSELASTLINE <格式化字符串></font></h4>

用指定的字符串重写最后一行文字
它改写的行会在下一句话打印时被替换
基本上只会在INPUT,INPUTS中使用
参数与PRINTFORM类似

	$INPUT_LOOP
	INPUT
	IF RESULT != 0
	　　;!;CLEARLINE 1
	　　;!;REUSELASTLINE 无效数值
	　　GOTO INPUT_LOOP
	ENDIF

像这样，在GOTO INPUT_LOOP之前调用REUSELASTLINE，
前一个输入将从屏幕上删除，下一个输入显示在与前一个输入相同的行上
因此，即使重复无效输入，行数也不会增加
可以避免错误数字积累把选项挤出屏幕外的情况...应该(译者:玩家不会向上拉窗口?)

顺便说一下，建议在@USERXXX系统函数的条件分支的最后添加这些
(对象有三个:@USERCOM、@USERSHOP、@USERABLUP)

	;!;ELSE
	　　;!;REUSELASTLINE
	ENDIF

(;!;表示Emuera专用,Era Maker不会执行)(译者:这都啥年头了,era maker是啥?)

<br/>
<h4 id="1.10"><font color=MediumBlue>1.10 CLEARLINE <整形 消除行数></font></h4>

行数以PRINTL等换行为止为一行。
另外,被分割成多行的长字符串只算一行

<br/>
<h4 id="1.11"><font color=MediumBlue>1.11 PRINT_IMG <字符串表达式 图像名></font></h4>

在行中显示指定的图像。
相当于HTML_PRINT指令的\<img>

译者补充下用法,字符串表达式填resources里CSV对应的图片名字就行了

<br/>
<h4 id="1.12"><font color=MediumBlue>1.12 PRINT_RECT <整形 长度></font></h4>

在行中显示长方形,参数为长方形长度,参数为100时长度与全角字符相等
可以像改变字体颜色一样通过[SETCOLOR](#2.1)命令来改变颜色
相当于HTML_PRINT指令的<shape type='rect'>

<br/>
<h4 id="1.13"><font color=MediumBlue>1.13 PRINT_RECT <整形 x>, <整形 y>, <整形 宽>, <整形 高></font></h4>

在行中显示指定x、y、宽、高的长方形
参数为100时长度与全角字符相等
可以像改变字体颜色一样通过[SETCOLOR](#2.1)命令来改变颜色
相当于HTML _print指令的<shape type='rect'>

<br/>
<h4 id="1.14"><font color=MediumBlue>1.14 PRINT_SPACE <整形 长度></font></h4>

留出指定大小的空格,参数为100时长度与全角字符相等
相当于HTML_PRINT指令的<shape type='space'>
<br/>

<h3 id="2"><font color=MidNightBlue>2 色彩·字体·显示规格操作</font></h3>
<h4 id="2.1"><font color=MediumBlue>2.1 SETCOLOR <整形 R>, <整形 G>, <整形 B></font></h4>
<h4 id="2.2"><font color=MediumBlue>2.2 SETCOLOR <整形 RGB></font></h4>
<h4 id="2.3"><font color=MediumBlue>2.3 RESETCOLOR</font></h4>

将文字颜色变更为指定的颜色，直到使用RESETCOLOR为止
在SETCOLOR中指定的颜色可以通过RESETCOLOR重置
当前字体颜色色可以通过[GETCOLOR](#2.9)获取，默认字体颜色色可以通过[GETDEFCOLOR](#2.10)获取
1.731以后可以在SETCOLOR中以0xRRGGBB形式指定了
###### 示例:

	SETCOLOR 255, 128, 0
	SETCOLOR 0xFF8000

这两行都是相同的意思。通过GETCOLOR指令可以获得执行后颜色的值

<br/>
<h4 id="2.4"><font color=MediumBlue>2.4 SETBGCOLOR <整形 R>, <整形 G>, <整形 B></font></h4>
<h4 id="2.5"><font color=MediumBlue>2.5 SETBGCOLOR <整形 RGB></font></h4>
<h4 id="2.6"><font color=MediumBlue>2.6 RESETBGCOLOR</font></h4>

将背景色改为指定颜色的命令。
基本方法与[SETCOLOR](#2.1),[RESETCOLOR](#2.3)相同，
为了安全,变更后0.2秒以内再次变更的情况下,到0.2秒为止强制WAIT(译者没有暂时发现不安全问题,无法对其润色,就采用直译了)
当前字体颜色色可以通过[GETBGCOLOR](#2.11)获取，默认字体颜色色可以通过[GETDEFBGCOLOR](#2.12)获取

<br/>
<h4 id="2.7"><font color=MediumBlue>2.7 SETCOLORBYNAME <字符串></font></h4>
<h4 id="2.8"><font color=MediumBlue>2.8 SETBGCOLORBYNAME <字符串></font></h4>

从已定义的颜色名称中指定字体显示颜色和背景颜色的命令。
其他的方法都与[SETCOLOR](#2.1)·[SETBGCOLOR](#2.5)相同
自变量是颜色名称。已经定义的颜色名称请参考[KnownColor枚举](https://learn.microsoft.com/zh-cn/dotnet/api/system.drawing.knowncolor?view=net-6.0)

<br/>
<h4 id="2.9"><font color=MediumBlue>2.9 GETCOLOR</font></h4>
将当前的文字颜色存入RESULT:0中
返回值是16进制的0xRRGGBB
例如,如果橙色(R,G,B) = (255, 128, 0),则返回0xff8000(十进制16744448)。
颜色和数字的对应可以参考介绍web color的网站
1.731的变更后，SETCOLOR命令也可以用SETCOLOR 0xff8000那样的形式来指定了

<br/>
<h4 id="2.10"><font color=MediumBlue>2.10 GETDEFCOLOR</font></h4>
GETDEFCOLOR
将标识中指定的文字颜色存入RESULT:0中
和[GETCOLOR](#2.9)类似

<br/>
<h4 id="2.11"><font color=MediumBlue>2.11 GETDEFCOLOR</font></h4>
GETBGCOLOR
将当前的背景颜色存入RESULT:0中
和[GETCOLOR](#2.9)类似

<br/>
<h4 id="2.12"><font color=MediumBlue>2.12 GETDEFCOLOR</font></h4>
GETDEFBGCOLOR
将标识中指定的背景颜色存入RESULT:0中
和G[GETCOLOR](#2.9)类似

<br/>
<h4 id="2.13"><font color=MediumBlue>2.13 GETDEFCOLOR</font></h4>
GETFOCUSCOLOR
将选项按钮的颜色代码存入RESULT:0
和G[GETCOLOR](#2.9)类似

<br/>
<h4 id="2.14"><font color=MediumBlue>2.14 FONTBOLD</font></h4>
<h4 id="2.15"><font color=MediumBlue>2.15 FONTITALIC</font></h4>
<h4 id="2.16"><font color=MediumBlue>2.16 FONTREGULAR</font></font></h4>

FONTBOLD 粗体
FONTITALIC 斜体
将之后的文字样式变更为指定的样式
BOLD和ITALIC可重复(粗体斜体)
调用REGULAR的话,返回默认样式

<br/>
<h4 id="2.17"><font color=MediumBlue>2.17 FONTSTYLE <整形></font></h4>


将之后的文字样式变更为指定的样式
位运算 0是正常的,1是粗体,2是斜体,4是删除线,8是下划线
可以按位组合
例如FONTSTYLE 3是粗体且斜体
[FONTBOLD](#2.14)、[FONTITALIC](#2.15)效果和FONTSTYLE 1, FONTSTYLE 2相同
[FONTREGULAR](#2.16)等价于FONTSTYLE 0, 也就是恢复默认样式

	FONTSTYLE 1 + 2
	PRINTL 粗体＋斜体
	FONTSTYLE 5
	PRINTL 粗体＋删除线
	FONTITALIC
	PRINTL 粗体＋斜体＋删除线
	FONTSTYLE 0
	PRINTL 通常
	<实际结果请自行运行>

译者强烈建议不了解位运算的去学下

<br/>
<h4 id="2.18"><font color=MediumBlue>2.18 GETSTYLE</font></h4>

将当前字体的样式(粗体、斜线等)存入RESULT:0
字体样式和SETSTYLE是一样的
如果没有特殊样式,则返回0

<br/>
<h4 id="2.19"><font color=MediumBlue>2.19 CHKFONT <字符串表达式 字体名></font></h4>

检查是否安装了指定名称的字体
如果安装了的话返回1,如果没有安装则返回0,返回值存在RESULT:0中
使用示例请参考[SETFONT](#2.20)指令

<br/>
<h4 id="2.20"><font color=MediumBlue>2.20 SETFONT <字符串表达式 字体名></font></h4>

SETFONT命令之后的字符串将使用指定的字体显示
省略参数或传入空字串时,则返回emuera.config中指定的默认字体
如果没有安装指定的字体,可以考虑使用"Microsoft Sans Serif"代替
如果要指定可能没有安装的字体，请在SETFONT之前使用[CHKFONT](#2.19)命令判断

	PRINTL abc123あいう(默认字体)
	CHKFONT "ＭＳ Ｐゴシック"
	IF RESULT
		SETFONT "ＭＳ Ｐゴシック"
		PRINTL abc123あいう(ＭＳ Ｐゴシック)
	ENDIF
	CHKFONT "ＭＳ 明朝"
	IF RESULT
		SETFONT "ＭＳ 明朝"
		PRINTL abc123あいう(ＭＳ 明朝)
	ENDIF
	STR:0 = ＭＳ Ｐ明朝
	CHKFONT STR:0
	IF RESULT
		SETFONT STR:0
		PRINTL abc123あいう(ＭＳ Ｐ明朝)
	ENDIF
	SETFONT
*注:"ＭＳ Ｐゴシック","ＭＳ 明朝","ＭＳ Ｐ明朝"是字体名*

<br/>
<h4 id="2.21"><font color=MediumBlue>2.21 GETFONT</font></h4>

将当前字体的名称存入RESULTS:0
返回值和[SETFONT](#2.20)命令中指定的名字一样
当没有使用[SETFONT](#2.20)命令时，将返回emuera.config中指定的默认字体名

<br/>
<h4 id="2.22"><font color=MediumBlue>2.22 FORCEKANA <整形></font></h4>

指定的平假名、片假名的使用
仅对包含关键字"K"的各种打印类指令有效
根据自变量指定的值，有以下影响

* 0:不进行变换
* 1:平假名→片假名
* 2:片假名→平假名(仅全角)
* 3:片假名→平假名(全角、半角均可)

(译者:你都来看翻译版的了,这个应该用不上吧)

<br/>
<h4 id="2.23"><font color=MediumBlue>2.23 ALIGNMENT <字符串></font></h4>

将ALIGNMENT之后的行对齐到指定的位置
可以传入"LEFT"、"CENTER"、"RIGHT"中的一个关键词
通常的表示是"ALIGNMENT LEFT",左对齐
可以通过"ALIGNMENT CENTER"达到和标题画面一样中央能对齐的效果
ALIGNMENT的效果在换行时生效
例:

	ALIGNMENT RIGHT
	PRINT あああ
	ALIGNMENT CENTER
	PRINTL いいい
	ALIGNMENT LEFT

"あああいいい"这段字符串被打印到了屏幕中央
当前ALIGNMENT的设定可以通过[CURRENTALIGN](#2.24)来获取

<br/>
<h4 id="2.24"><font color=MediumBlue>2.24 CURRENTALIGN</font></h4>

将当前的ALIGNMENT存入RESULTS:0。
返回值与用[ALIGNMENT](#2.23)命令指定的字符串相同(大写)
如果没有执行过[ALIGNMENT](#2.23)指令,则返回初始值LEFT

<br/>
<h4 id="2.25"><font color=MediumBlue>2.25 REDRAW <整形></font></h4>

绘图控制命令
在参数中指定0,只在用户需要输入的时候进行绘图
在参数中指定1后，就会按照"每秒帧"的格式,在指定的时间进行绘图
如果参数大于1(如REDRAW 2或REDRAW 3),除了上述效果外,还会在执行REDRAW指令的瞬间强制绘图
你可以通过[CURRENTREDRAW](#2.26)获取当前的REDRAW状态(0或1)

<br/>
<h4 id="2.26"><font color=MediumBlue>2.26 CURRENTREDRAW</font></h4>

将当前的REDRAW状态存入RESULT:0
返值通常是1,若使用[REDRAW](#2.25)命令抑制了绘图时变成0

<br/>
<h4 id="2.27"><font color=MediumBlue>2.27 PRINTCPERLINE</font></h4>

将emuera中玩家设置的"PRINTCを並べる数"(emuera1824中文版中为"PRINTC并列数量")值返回到RESULT:0中,默认是3

<br/>
<h4 id="2.28"><font color=MediumBlue>2.28 LINEISEMPTY</font></h4>

判断当前打印的行是否为空行
如果你在执行这个指令的时候想要进行"PRINTL"
如果结果只是空行,则返回1,否则返回0,存在RESULT:0中
在PRINTC系中,根据条件依次书写按钮时,最后使用该指令
可以判断是否有按钮被打印,可以做出当没有按钮被打印时的特殊按钮

<br/>
<h4 id="2.29"><font color=MediumBlue>2.29 BARSTR <整形 変量>, <整形 最大値>, <整形 长度></font></h4>

机翻译者看不懂,自己研究了下,按自己的理解改了改
用与BAR指令相同的参数来绘制类似血条的东西,返回值存在RESULTS:0里
###### 示例

	BARSTR 7, 20, 5
	PRINTSL RESULTS
	BARSTR 7, 20, 20
	PRINTSL RESULTS
	BARSTR 495, 500, 20
	PRINTSL RESULTS

结果

	[*....]
	[*******.............]
	[*******************.]
译者个人感觉这是个做血条的东西,変量为当前HP,最大値为HP最大值,长度为血条长度

<br/>
<h4 id="2.30"><font color=MediumBlue>2.30 MONEYSTR <整形>{, <字符串表达式 指定格式>}</font></h4>


将给定参数的数值加上金钱单位后存入RESULTS:0。
会自动处理单位的前置和后置
第二个参数的用法与[TOSTR](#3.5)命令的差不多

<br/>
<h4 id="2.31"><font color=MediumBlue>2.31 SKIPDISP <整形></font></h4>


以下摘自私家改造版的说明

> 添加SKIPDISP指令,可以无视诸如PRINT之类的画面输出指令和诸如WAIT、TWAIT之类的标志指令
> 　格式：SKIPDISP <整形>
> 　参数：0 　　不无视
> 　　　　0以外 无视PRINT等指令
> 　内容：如果启用了该标志,PRINT等输出均不会进行
> 　　　　另外,在该标志启用期间遇到INPUT/INPUTS时
> 　　　　用户会不知道该做什么,如果跳过可能会进入死循环
> 　　　　使用时应注明警告及用法
> 　　现在一般配合口上使用,使口上隐藏成为可能
> 　　显示和不显示会改变命令的结果,动作也会改变
> 　　因此,如果在此基础上调出口供,口上就不会被显示,而是进行其他的处理
> 　　在显示/隐藏时除了打印之外的处理均相同
> 　　如果有INPUT/INPUTS的话,可以用[NOSKIP](#2.32)~[ENDNOSKIP](#2.33)来处理
> 　　也可以先让SKIPDISP为0，在INPUT处理后再让SKIPDISP为1(姑且推荐前者)
> 　　顺便说一下，你也可以通过[ISSKIP](#2.34)()来获取该标志

从ver1.808开始，即使放在SIF里也能运行。另外，使用SKIPDISP时，无论传入什么参数，RESULT:0都将被重置为0

<br/>
<h4 id="2.32"><font color=MediumBlue>2.32 NOSKIP</font></h4>
<h4 id="2.33"><font color=MediumBlue>2.33 ENDNOSKIP</font></h4>

以下摘自私家改造版的说明

> NOSKIP~ENDNOSKIP包裹的区间可以无视显示关系
> 　　二者之间的区域将以SKIPDISP 1显示
> 　　主要在有INPUT的场合使用比较好
> 　　另外,此指令不受SKIPDISP的状态影响
> 　　可以在有SKIPDISP出现的环境下使用(例如:显示,隐藏口上)
> 　　有了它,你可以很好的显示必要显示的地方

<br/>
<h4 id="2.34"><font color=MediumBlue>2.34 ISSKIP</font></h4>

如果[SKIPDISP](#2.31)的标志不是0(忽略打印等输出),就返回1,否则返回0,返回结果储存在RESULT:0中

<br/>
<h4 id="2.35"><font color=MediumBlue>2.35 MOUSESKIP</font></h4>

如果右键被按下,若处于WAIT跳过状态，则返回1,否则返回0,返回值存入RESULT:0
宏处理的跳过返回0
如果宏处理的跳过和右键冲突,宏优先,返回0
(译者:宏处理是啥我也不知道,有知道的可以告诉我)
<br/>

<h3 id="3"><font color=MidNightBlue>3 字符串操作・示例</font></h3>
<h4 id="3.1"><font color=MediumBlue>3.1 TOUPPER <字符串表达式></font></h4>
<h4 id="3.2"><font color=MediumBlue>3.2 TOLOWER <字符串表达式></font></h4>
<h4 id="3.3"><font color=MediumBlue>3.3 TOHALF <字符串表达式></font></h4>
<h4 id="3.4"><font color=MediumBlue>3.4 TOFULL <字符串表达式></font></h4>

将对变量进行特定的变换,并将结果存入RESULTS:0
TOUPPER返回大写字母、TOLOWER返回小写字母
TOHALF把全角字符转换为半角,但没有半角的字符不会被转变
TOFULL把全角转化为半角

<br/>
<h4 id="3.5"><font color=MediumBlue>3.5 TOSTR <整形>{, <字符串表达式 指定格式>}</font></h4>

是将数值转换成字符串的命令
将想要转换的数字指定为第一参数,转换的格式为第二参数
第二参数可以省略,但是省略的情况和PRINTFORM{}一样,只是字符串
这个函数在内部是C#的Int64的ToString()函数,可以用和C#相同的格式。如果第二个参数不合适,就会报错
简单的格式指定的例子请参考[exmeth 式中で使える関数](https://osdn.net/projects/emuera/wiki/exmeth)。<指定格式>的详细内容请参考关于C#的数值格式指定字符串进行解说的网站

###### 示例
	LOCAL = 495
	LOCAL:1 = 2004
	PRINTFORML %TOSTR(LOCAL,@"495转换后结果:0,0,.,0\%,支持%CALLNAME%")%
	PRINTFORML %TOSTR(LOCAL:1,@"2\\0\\04转换后结果0,0,.,0\%,支持%CALLNAME%")%
结果

	495转换后结果:49.5%支持芙兰
	2004转换后结果200.4%支持芙兰

<br/>
<h4 id="3.6"><font color=MediumBlue>3.6 ISNUMERIC <字符串表达式></font></h4>

判断字符串是否可以作为数值解析(是否可以用[TOINT](#3.7)取值)。
可以的话返回1,否则返回0,结果存在RESULT:0中

<br/>
<h4 id="3.7"><font color=MediumBlue>3.7 TOINT <字符串表达式></font></h4>

将参数转化为整形类型,返回值存入RESULT:0。但是,只能转化半角字符,全角字符不会被转化
参数不能被解析为数值时,或者传入全角字符时,返回值为0

<br/>
<h4 id="3.8"><font color=MediumBlue>3.8 STRLEN <字符串></font></h4>
<h4 id="3.9"><font color=MediumBlue>3.9 STRLENS <字符串表达式></font></h4>
<h4 id="3.10"><font color=MediumBlue>3.10 STRLENFORM <格式化字符串></font></h4>

测量字符串的长度,返回值存入RESULT:0中
长度是按半角字符计算的,全角字符会被算作2个
###### 示例

	STRLEN ABCあいう
	PRINTFORML <TEST1> = {RESULT}

	STR:0 = ABCあいう
	STRLENS STR:0
	PRINTFORML <TEST2> = {RESULT}

	STRLENFORM abc%STR:0%
	PRINTFORML <TEST3> = {RESULT}

	;STRLENS也支持STR表达式
	STRLENS "abc" + STR:0
	PRINTFORML <TEST4> = {RESULT}
	WAIT
結果

	<TEST1> = 9
	<TEST2> = 9
	<TEST3> = 12
	<TEST4> = 12

<br/>
<h4 id="3.11"><font color=MediumBlue>3.11 STRLENU <字符串></font></h4>
<h4 id="3.12"><font color=MediumBlue>3.12 STRLENSU <字符串表达式></font></h4>
<h4 id="3.13"><font color=MediumBlue>3.13 STRLENFORMU <格式化字符串></font></h4>

[STRLEN](#3.8)、[STRLENS](#3.9)和[STRLENFORM](#3.10)的Unicode版本,不同的是全角文字也算作一个

<br/>
<h4 id="3.14"><font color=MediumBlue>3.14 SUBSTRING <字符串表达式>, <整形 起始>, <整形 结束></font></h4>

返回字符串的指定部位,结果存入RESULT:0中
字符串的第一个字符位置为0。如果起始位置大于原字符串的长度,空字符串""将被返回。
字符数由半角字符来确定,全角字符算2个
如果你将结束位置传入一个负值,或者比字符串长度更大的数,返回值将是整个字符串
如果你指定的起始位置不能切片(指你指定的起始位置的是全角字符的中间位置),就会认为后面一个字符为起始位置
请注意,因此会出现比你预期的结果多一个字符的情况

###### 示例

	STR:0 = 01234あいうえお

	SUBSTRING STR:0, 0, -1
	PRINTFORML <TEST1> = %RESULTS:0%

	SUBSTRING STR:0, 1, 3
	PRINTFORML <TEST2> = %RESULTS:0%

	SUBSTRING STR:0, 6, 3
	PRINTFORML <TEST3> = %RESULTS:0%
	
	SUBSTRING STR:0, 100, -1
	PRINTFORML <TEST4> = %RESULTS:0%
	WAIT
结果

	<TEST1> = 01234あいうえお
	<TEST2> = 123
	<TEST3> = いう
	<TEST4> = 

<br/>
<h4 id="3.15"><font color=MediumBlue>3.15 SUBSTRINGU <字符串表达式>, <整形 起始>, <整形 结束></font></h4>
[SUBSTRING](#3.14)的Unicode版本。不同的是字符长度中,全角文字也算作一个

<br/>
<h4 id="3.16"><font color=MediumBlue>3.16 CHARATU <字符串表达式>, <文字位置></font></h4>

以下摘自私家改造版的说明

> 添加表达式中函数CHARATU获取字符串中的任意字符数中的字符
> 　書式：CHARATU(<参照字符串>, [取得文字位置])
> 　内容：获取字符串中指定位置的字符
> 　　　　处理系统中全角字符占一个索引

###### 示例

	STR:0 = QED「495年的波纹」
	CHARATU STR:0, 7
	PRINTFORM %RESULTS%
结果

	年

<br/>
<h4 id="3.17"><font color=MediumBlue>3.17 STRFIND <字符串表达式 检索对象>, <字符串表达式 要检索的字符串>{, <整形 起始索引>}</font></h4>

是字符串检索命令。
第一个参数是检索对象
第二个参数是要检索的字符串
以0为开始索引检索,全角字符站2个索引,没找到返回-1,返回值存在RESULT:0

	STR:0 = abcdefghi
	STR:1 = あいうえお
	STR:2 = うえ

	STRFIND STR:0, "cde"
	PRINTFORML <TEST1> = {RESULT:0}

	STRFIND STR:1, "いうえ"
	PRINTFORML <TEST2> = {RESULT:0}

	STRFIND STR:1, STR:2
	PRINTFORML <TEST3> = {RESULT:0}

	STRFIND STR:1, "か"
	PRINTFORML <TEST4> = {RESULT:0}
结果

	<TEST1> = 2
	<TEST2> = 2
	<TEST3> = 4
	<TEST4> = -1

从1.712开始,STRFIND命令可以指定第三个参数
可以指定检索的起始索引

	STRFIND "abcdeabced","a",3
	PRINTFORML <TEST5> = {RESULT:0}
结果

	<TEST5> = 5

虽然"a"也在0的位置,但是根据第三参数,检索从3的位置("d")开始,所以最先找到的"a"是5的位置

<br/>
<h4 id="3.18"><font color=MediumBlue>3.18 STRFINDU <字符串表达式 检索对象>, <字符串表达式 要检索的字符串>{ , <整形 起始索引>}</font></h4>

以下摘自私家改造版的说明

> 全角字符只占一个索引的[STRFIND](#3.17)
> 　書式：STRFINDU(<检索对象>, <要检索的字符串>{, <起始索引>})
> 　内容：全角字符只占一个索引的[STRFIND](#3.17),返回值的字符位置和起始索引中全角字符只占一个索引

<br/>
<h4 id="3.19"><font color=MediumBlue>3.19 STRCOUNT <字符串表达式 检索对象>, <字符串表达式 要检索的字符串></font></h4>

获取该字符串中含多少要检索的字符串的命令。返回值将被存入RESULT:0中
检索字码串的格式以c#的正则表达式的规范为准

###### 

	STR:0 = 测试内容1测试内容2测试内容3测试内容4
	STRCOUNT STR:0, "测试内容"
	PRINTFORM 结果 = {RESULT}

结果

	结果 = 4

<br/>
<h4 id="3.20"><font color=MediumBlue>3.20 SPLIT <字符串表达式 被分割字符串>, <字符串表达式 分割标准>, <字符串表达式数组></font></h4>

第一个参数指定被分割的字符串,第二个参数为分割的标准,第三个参数用来存储结果
另外,分割后的元素数量将返回到RESULT:0中
第三个参数必须是数组
注意:这个数组将被存入

###### 示例

	LOCALS:0 = 测试内容1
	LOCALS:1 = 测试内容2
	PRINTFORML 调用前LOACLS:0 = %LOCALS:0%
	PRINTFORML 调用前LOACLS:1 = %LOCALS:1%
	SPLIT "あい,うえ,,お", ",", LOCALS
	PRINTL 调用后
	REPEAT RESULT
		PRINTFORML LOCALS:{COUNT} = %LOCALS:COUNT%
	REND

结果

	调用前LOACLS:0 = 测试内容1
	调用前LOACLS:1 = 测试内容2
	调用后
	LOCALS:0 = あい
	LOCALS:1 = うえ
	LOCALS:2 = 
	LOCALS:3 = お

*不建议使用REPEAT,也不建议直接使用RESULT,这里只是图方便*

如果拆分后的元素数超过了可以代入第三参数的元素数，就不会被代入。
RESULT中会加入实际的分割数,请在那里进行判断

<br/>
<h4 id="3.21"><font color=MediumBlue>3.21 REPLACE <字符串表达式 替换对象>, <字符串表达式 要替换内容>, <字符串表达式 替换内容></font></h4>

以下摘自私家改造版的说明

> 实现了字符串替换命令REPLACE
> 　格式：REPLACE(<替换对象>, <要替换内容>, <替换内容>)
> 　内容：对替换对象进行查找,找到要替换内容后将其替换为替换内容
> 　　内部处理完全是正则表达式。第二个参数按照c#的正则表达式的规范操作
> 　　因此，()、[]、$、/.*+等正则表达式中使用的符号必须要转义的

###### 示例1

	STR:0 = 测试内容1测试内容2测试内容3
	REPLACE STR:0, "内容", "项目"
	PRINTFORML %RESULTS%
结果

	测试项目1测试项目2测试项目3
<br>

###### 示例2

	LOCALS = CFLAG:1,CFLAG:2,TFLAG:1,TFLAG:2,FLAG:1,CFLAG:3
	PRINTL 替换前
	PRINTSL LOCALS
	PRINTL
	PRINTL 替换后
	PRINTSL REPLACE(LOCALS, "CFLAG:[1-9]*", "角色标志")
结果

	替换前
	CFLAG:1,CFLAG:2,TFLAG:1,TFLAG:2,FLAG:1,CFLAG:3
	
	替换后
	角色标志,角色标志,TFLAG:1,TFLAG:2,FLAG:1,角色标志

<br/>
<h4 id="3.22"><font color=MediumBlue>3.22 ESCAPE <字符串></font></h4>

以下摘自私家改造版的说明

> 添加了用于将字符串转义用于正则表达式的式中函数ESCAPE
> 　格式：ESCAPE([字符串])
> 　内容：将参数中的字符串的正则表达式元字符转义返回，使得字符串在正则表达式中为明文

*这个是纯机翻的*

<br/>
<h4 id="3.23"><font color=MediumBlue>3.23 UNICODE <整形></font></h4>

是将自变量的值对应的unicode的字符返回RESULT:0的命令
例如,下面的脚本会显示白色的心形符号。
另外,如果字体不对应的话就无法显示。

	UNICODE 0x2661
	PRINTFORMW %RESULTS%

另外，请注意Emuera的Unicode对应并不完整
例如Emuera在使用代理对(surrogate pair)的情况下，不能保证正确的操作
*代理对是啥译者也不知道*

<br/>
<h4 id="3.24"><font color=MediumBlue>3.24 ENCODETOUNI <格式化字符串表达式 对象></font></h4>


以下摘自私家改造版的说明

> 实现了返回字符串的Uncode编码的命令ENCODETOUNI
> 　格式：ENCODETOUNI <对象字符串(格式化字符串)>
> 　内容：将给定的字符串编码转化为Uncode编码,并将长度返回给RESULT:0
> 　　　　RESULT:0 　文字数
> 　　　　RESULT:1～ 字节数

###### 示例

	STR:0 = 测试内容1
	ENCODETOUNI %STR:0%
	PRINTFORML {RESULT}
	REPEAT RESULT
		PRINTFORML {RESULT:(COUNT + 1), 5}, %UNICODE(RESULT:(COUNT + 1))%
	REND
结果

	27979, 测
	35797, 试
	20869, 内
	23481, 容
		49, 1
<br/>

<h3 id="4"><font color=MidNightBlue>4 运算</font></h3>
<h4 id="4.1"><font color=MediumBlue>4.1 POWER <整形 结果>, <整形 底数>, <整形 指数></font></h4>

将乘方代入指定的变量中。
例如POWER A, X, Y的话,将X的Y次方代入A。
运算结果如果发生溢出的话就会出错。

###### 示例

	X = 11
	Y = 2
	POWER A, X, 2
	PRINTFORML <TEST1> = {A}
	POWER CFLAG:2, X + 1, Y + 1
	PRINTFORML <TEST2> = {CFLAG:2}
结果(不考虑TARGET有问题)

　<TEST1> = 121
　<TEST2> = 1728

<br/>
<h4 id="4.2"><font color=MediumBlue>4.2 ABS <整形></font></h4>

将参数的绝对值返回到RESULT:0中

<br/>
<h4 id="4.3"><font color=MediumBlue>4.3 SIGN <整形></font></h4>

将参数的正负返回到RESULT:0中
负值返回-1,正值返回1,0返回0

<br/>
<h4 id="4.4"><font color=MediumBlue>4.4 SQRT <整形></font></h4>

将参数的平方根返回到RESULT:0中

<br/>
<h4 id="4.5"><font color=MediumBlue>4.5 GETBIT <整形 操作变量>, <整形 操作位置></font></h4>

建议和[SETBIT](#4.10)[CLEARBIT](#4.11)[INVERTBIT](#4.12)一起观看

获得目标参数的指定位,结果返回到RESULT:0中
第一个参数指定目标变量,第二个参数指定想要获取的比特位。第二参数可以指定的值为0 ~ 63,超出该范围会报错
如果第二个参数是常数,例如5，

	GETBIT X, 5
	(X & 1p5) != 0

二者结果相同
(译者:强烈建议学习位运算)

<br/>
<h4 id="4.6"><font color=MediumBlue>4.6 MAX <整形>{, <整形>...}</font></h4>

将参数中的最大值返回到RESULT:0中

<br/>
<h4 id="4.7"><font color=MediumBlue>4.7 MIN <整形>{, <整形>...}</font></h4>

将参数中的最小值返回到RESULT:0中

<br/>
<h4 id="4.8"><font color=MediumBlue>4.8 LIMIT <整形 值>, <整形 下限>, <整形 上限></font></h4>

将第一个参数的值返回到RESULT:0中
但是,如果第一个参数小于第二个参数,则返回第二个参数,如果大于第三个参数,则返回第三个参数
例如,如果你想将X - Y存入A,但希望代入后的值大于或等于0,小于或等于100，通常这样写

	A = X - Y
	SIF A < 0
		A = 0
	SIF A > 100
		A = 100

有了LIMIT命令后可以这样写

	LIMIT X - Y, 0, 100
	A = RESULT
	;一般这样写的比较多
	A = LIMIT(X - Y, 0, 100)

<br/>
<h4 id="4.9"><font color=MediumBlue>4.9 INRANGE <整形 值>, <整形 下限>, <整形 上限></font></h4>

如果第一个参数大于或等于第二个参数且小于等于第三个参数，就用1代替，如果第一个参数小于第二个参数或大于第三个参数，就用0代替RESULT:0
说人话,第一个参数属于[下限,上限]返回1,否则返回0

<br/>
<h4 id="4.10"><font color=MediumBlue>4.10 SETBIT <整形 操作变量>, <整形 操作位置>{, <整形 操作位置>,...}</font></h4>
<h4 id="4.11"><font color=MediumBlue>4.11 CLEARBIT <整形 操作变量>, <整形 操作位置>{, <整形 操作位置>,...}</font></h4>
<h4 id="4.12"><font color=MediumBlue>4.12 INVERTBIT <整形 操作变量>, <整形 操作位置>{, <整形 操作位置>,...}</font></h4>

位操作函数

建议和[GETBIT](#4.5)一起观看

对第一个参数中,第二个及往后变量指定的位置,进行操作
SETBIT设为1,CLEARBIT设为0,INVERTBIT将值进行反转

	SETBIT X, A
	CLEARBIT Y, B
	INVERTBIT Z, C

和下面结果相同

	X |= 1 << A
	Y &= ~(1 << B)
	Z ^= 1 << C

另外,这些位操作函数的格式与[GETBIT](#4.5)函数类似
你可以在通过[GETBIT](#4.5)(X, A)来观察"SETBIT X, A"指令导致的位变化
<br/>

<h3 id="5"><font color=MidNightBlue>5 角色操作・示例</font></h3>
<h4 id="5.1"><font color=MediumBlue>5.1 ADDCHARA <整形 角色番号1>{, <整形 角色番号2>, <整形 角色番号3>, ...}</font></h4>
<h4 id="5.2"><font color=MediumBlue>5.2 DELCHARA <整形 角色番号1>{, <整形 角色番号2>, <整形 角色番号3>, ...}</font></h4>

来自eramaker的命令,添加指定角色番号的角色,现在可以一次添加和消除很多角色

<br/>
<h4 id="5.3"><font color=MediumBlue>5.3 SWAPCHARA <整形 角色登录编号1>, <整形 角色登录编号2></font></h4>

更换指定的两个人的所有角色数据

###### 示例

	;增加人物
	ADDCHARA 1000
	ADDCHARA 2001
	LOCAL = CHARANUM - 1
	LOCAL:1 = CHARANUM - 2

	;角色变量赋值
	custom_talent:LOCAL:0 = 100
	custom_talent:(LOCAL:1):0 = 200
	CFLAG:(LOCAL):0 = 100
	CFLAG:(LOCAL:1):0 = 200
	
	PRINTL 交换前
	PRINTFORML NO:{LOCAL} = {NO:LOCAL}, NO:{LOCAL:1} = {NO:(LOCAL:1)}
	PRINTFORML custom_talent:{LOCAL}:0 = {custom_talent:LOCAL:0}, custom_talent:{LOCAL:1}:0 = {custom_talent:(LOCAL:1):0}
	PRINTFORML CFLAG:{LOCAL}:0 = {CFLAG:(LOCAL):0} CFLAG:{LOCAL:1}:0 = {CFLAG:(LOCAL:1):0}
	
	SWAPCHARA LOCAL, LOCAL:1

	PRINTL 交换后
	PRINTFORML NO:{LOCAL} = {NO:LOCAL}, NO:{LOCAL:1} = {NO:(LOCAL:1)}
	PRINTFORML custom_talent:{LOCAL}:0 = {custom_talent:LOCAL:0}, custom_talent:{LOCAL:1}:0 = {custom_talent:(LOCAL:1):0}
	PRINTFORML CFLAG:{LOCAL}:0 = {CFLAG:(LOCAL):0} CFLAG:{LOCAL:1}:0 = {CFLAG:(LOCAL:1):0}
结果

	交换前
	NO:3 = 2001, NO:2 = 1000
	custom_talent:3:0 = 100, custom_talent:2:0 = 200
	CFLAG:3:0 = 100 CFLAG:2:0 = 200
	交换后
	NO:3 = 1000, NO:2 = 2001
	custom_talent:3:0 = 200, custom_talent:2:0 = 100
	CFLAG:3:0 = 200 CFLAG:2:0 = 100
*注:custom_talent是YM里自定义的角色变量*

<br/>
<h4 id="5.4"><font color=MediumBlue>5.4 SORTCHARA {<角色变量> , < FORWARD / BACK>}</font></h4>

根据指定的键,对角色列表进行排序
排序的键可以是NAME这样的字符串表达式,也可以是NO这样的整形变量,CFLAG这样的整形变量也可以进行排序
<角色变量>可以省略,省略后将以角色番号进行排序
FORWARD是升序,BACK是降序。省略的情况按升序排序。
MASTER不会成为排序的对象。
另外,TARGET:0和ASSI:0会自动跟踪,使用后无需手动操作。
但是TARGET:1等的变量算需要手动跟踪角色的

	;NO升序排序
	SORTCHARA
	;NO降序排序
	SORTCHARA BACK
	;CFLAG:2升序排序
	SORTCHARA CFLAG:2
	;NAME降序排序
	SORTCHARA NAME, BACK

另外,即使TARGET不在角色编号范围内,也不会出错,因为不是实际参考CFLAG:2等值。

<br/>
<h4 id="5.5"><font color=MediumBlue>5.5 GETCHARA <整形 角色番号(NO)></font></h4>

确定当前拥有的角色中是否有这个角色,如果有的话就返回该角色的编号,如果没有的话返回-1
可以确定角色列表中是否有该角色

<br/>
<h4 id="5.6"><font color=MediumBlue>5.6 ADDDEFCHARA</font></h4>

是进行游戏开始时的系统的角色追加处理的命令
追加chara0*.csv中定义的角色和gamebase.csv中指定的初始角色
"[ADDCHARA](#5.1) 0"是寻找角色NO为0的角色并添加,ADDDEFCHARA是用csv的号码追加角色
如果没有相应的csv,则创建一个类似ADDVOIDCHARA的空角色
这是为了再现eramaker的初始化处理的命令,在@SYSTEM_TITLE以外的函数不能使用

<br/>
<h4 id="5.7"><font color=MediumBlue>5.7 ADDVOIDCHARA</font></h4>

是不依赖csv追加角色的命令
用ADDVOIDCHARA被追加的角色全部变量都为0或""(空字符串)

<br/>
<h4 id="5.8"><font color=MediumBlue>5.8 DELALLCHARA <整形 角色登录编号></font></h4>


删除已登录的角色,下面的脚本是用来删除所有登录角色的

	REPEAT CHARANUM
		DELCHARA 0
	REND

<br/>
<h4 id="5.9"><font color=MediumBlue>5.9 PICKUPCHARA <整形 角色登录编号>{, <整形 角色登录编号>, ....}</font></h4>

是只留下用自变量指定的登录角色,其余登录角色全部删除的命令。
MASTER:0、TARGET:0、ASSI:0等会自动跟随。调用后无需手动重新设定
如果TARGET:0等变量的值没有照应角色(为不合法数值或者照应的角色被删了),则值调整为-1

<br/>
<h4 id="5.10"><font color=MediumBlue>5.10 EXISTCSV <整形 角色番号></font></h4>

检查对应的角色是否在CSV中被定义,结果返回到RESULT:0中
如果被定义则返回1,如果没有被定义则返回0。
通过检测可以保证"[ADDCHARA](#5.1) NO"不报错的进行

<br/>
<h4 id="5.11"><font color=MediumBlue>5.11 FINDCHARA <角色变量>, <值>{, <整形 起始>, <整形 结束(不取)>}</font></h4>
<h4 id="5.12"><font color=MediumBlue>5.12 FINDLASTCHARA <角色变量>, <值>{, <整形 起始>, <整形 结束(不取)>}</font></h4>

FINDCHARA指令用于查找角色变量为指定值的角色编号,结果返回到RESULT:0中
在找到多个结果的情况下,FINDCHARA会返回找到的第一个角色编号
FINDLASTCHARA是到着查的剩下和FINDCHARA相同
如果没有找到的话返回-1。
另外,指定第三参数可以指定搜索开始的位置,指定第四参数可以指定搜索结束的位置。
但是,搜索范围超过角色数的范围的情况会报错

###### 示例(打印CFLAG:10为123的角色名)

	X = -1
	WHILE 1
		FINDCHARA CFLAG:10, 123, X + 1
		X = RESULT
		SIF X < 0
			BREAK
		PRINTFORML %NAME:X%
	WEND

<br/>
<h4 id="5.13"><font color=MediumBlue>5.13 COPYCHARA <整形 角色编号>, <整形 角色编号></font></h4>

将第一个参数指定的角色的所有数据复制到第二个参数指定的角色中

<br/>
<h4 id="5.14"><font color=MediumBlue>5.14 ADDCOPYCHARA <整形 角色编号></font></h4>

追加与指定角色数据相同的角色。也就是[ADDCHARA](#5.13)的变种。
<br\>

<h3 id="6"><font color=MidNightBlue>6 变量操作・CSV读取・数组操作</font></h3>
<h4 id="6.1"><font color=MediumBlue>6.1 VARSIZE <变量名></font></h4>

将指定变数组的尺寸返回RESULT:0中
多维数组变量的情况下,将各个维度的尺寸依次返回RESULT:0, RESULT:1, RESULT:2。
排列的尺寸是是用variablezee.csv指定的值

###### 示例

	VARSIZE FLAG
	PRINTFORML <TEST1> = {RESULT:0}
	VARSIZE SAVESTR
	PRINTFORML <TEST2> = {RESULT:0}
	VARSIZE TALENT
	PRINTFORML <TEST3> = {RESULT:0}
	WAIT
结果(没有改变尺寸的情况下)

	<TEST1> = 10000
	<TEST2> = 100
	<TEST3> = 1000

※因为该参数只是作为参照。所以在上面的例子中,TARGET不在角色编号范围内的情况下,试图引用第一个TALENT也不会出错

<br/>
<h4 id="6.2"><font color=MediumBlue>6.2 RESETDATA</font></h4>

初始化除GLOBAL和GLOBALS以外的所有变量
具体来说就是删除所有的角色,并将0或""赋值到所有的局部变量和普通变量
另外,若PALAMLV等设定有初始值的变量,将赋值为初始值

<br/>
<h4 id="6.3"><font color=MediumBlue>6.3 RESETGLOBAL</font></h4>

初始化全局变量
具体做法是将GLOBAL赋值为0,将GLOBALS赋值为""

<br/>
<h4 id="6.4"><font color=MediumBlue>6.4 RESET_STAIN <整形 角色登录编号></font></h4>

初始化指定角色的STAIN的命令
初始值和BEGIN TRAIN时被代入的值一样,可以用_replact.csv的“汚れの初期値”来指定。

<br/>
<h4 id="6.5"><font color=MediumBlue>6.5 SWAP <変量1>, <変量2></font></h4>


替换变量1和变量2的内容
需要交换的两个变量必须是相同类型(整数和整数，串字和串字)。

<br/>
<h4 id="6.6"><font color=MediumBlue>6.6 CSVNAME <整形 角色番号></font></h4>
<h4 id="6.7"><font color=MediumBlue>6.7 CSVCALLNAME <整形 角色番号></font></h4>
<h4 id="6.8"><font color=MediumBlue>6.8 CSVNICKNAME <整形 角色番号></font></h4>
<h4 id="6.9"><font color=MediumBlue>6.9 CSVMASTERNAME <整形 角色番号></font></h4>

该函数可以直接调用CSV中定义的NAME、CALLNAME、NICKNAME和MASTERNAME
如果你想要没有登录的角色信息可以通过这些函数调用
第一个参数是角色番号(NO)

<br/>
<h4 id="6.10"><font color=MediumBlue>6.10 CSVBASE <整形 角色番号>, <整形 索引></font></h4>
<h4 id="6.11"><font color=MediumBlue>6.11 CSVCSTR <整形 角色番号>, <整形 索引></font></h4>
<h4 id="6.12"><font color=MediumBlue>6.12 CSVABL <整形 角色番号>, <整形 索引></font></h4>
<h4 id="6.13"><font color=MediumBlue>6.13 CSVTALENT <整形 角色番号>, <整形 索引></font></h4>
<h4 id="6.14"><font color=MediumBlue>6.14 CSVMARK <整形 角色番号>, <整形 索引></font></h4>
<h4 id="6.15"><font color=MediumBlue>6.15 CSVEXP <整形 角色番号>, <整形 索引></font></h4>
<h4 id="6.16"><font color=MediumBlue>6.16 CSVRELATION <整形 角色番号>, <整形 索引>, <整形 索引></font></h4>
<h4 id="6.17"><font color=MediumBlue>6.17 CSVJULE <整形 角色番号>, <整形 索引></font></h4>
<h4 id="6.18"><font color=MediumBlue>6.18 CSVEQUIP <整形 角色番号>, <整形 索引></font></h4>
<h4 id="6.19"><font color=MediumBlue>6.19 CSVCFLAG <整形 角色番号>, <整形 索引></font></h4>

是直接读取CSV中定义的值的函数
第一个参数是角色番号,第二个参数是各变量的索引
字符串变量的结果返回到RESULTS:0中,整形变量的结果返回到RESULT:0中

<br/>
<h4 id="6.20"><font color=MediumBlue>6.20 GETNUM <字符串 CSV名>, <字符串表达式></font></h4>

读取CSV中对被定义名字的索引,将其代入RESULT:0。
例如，如果在ABL.csv中定义了“2,技巧”，那么GETNUM ABL, “技巧”的结果是将2赋值给RESULT:0。
没有被定义则返回-1
csv和变量的对应以[[exetc](https://wiki.eragames.rip/index.php/Emuera/exetc) Emueraの拡張文法#一般]的页面的「文字列による配列変数の要素の指定」为准

<br/>
<h4 id="6.21"><font color=MediumBlue>6.21 GETPALAMLV <整形>, <整形 上限></font></h4>
<h4 id="6.22"><font color=MediumBlue>6.22 GETEXPLV <整形>, <整形 上限></font></h4>

将给定值的与PALAMLV·EXPLV进行比较,将不超过指定值的PALAMLV·EXPLV返回到RESULT:0中
第二个参数表示要调查的LV上限
请设定PALAMLV·EXPLV的值后再使用

<br/>
<h4 id="6.23"><font color=MediumBlue>6.23 FINDELEMENT <变量名>, <要检索的内容(类型必须与变量相同)>{, <起始位置>, <中止位置(不取)>, <整形 是否完全一致>}</font></h4>
<h4 id="6.24"><font color=MediumBlue>6.24 FINDLASTELEMENT <变量名>, <要检索的内容(类型必须与变量相同)>{, <起始位置>, <中止位置(不取)>, <整形 完全一致>}</font></h4>

从第一个参数指定的变量所在的数组中获取指定存储指定值的变量的索引
在第一个参数指定的变量所在的数组中,在第三,第四个参数指定范围内找到与第二个参数值相同的元素时返回其索引
如果有多个结果,FINDELEMENT只会返回第一个结果
FINDLASTELEMENT是倒着查的
如果没有找到,则返回-1
如果搜索的对象是字符串,可以像[REPLACE](#3.21)一样使用正则表达式
第五个参数只有在第一个参数类型为STR时才生效,若为0若字符串中包含要检索的内容即可返回其索引
如果是0以外的话,只有和字符串完全一致的情况下才OK

###### 示例
	LOCAL:0 = 1
	LOCAL:1 = 1
	LOCAL:2 = 2
	LOCAL:3 = 1
	LOCAL:4 = 1
	LOCAL:5 = 1
	PRINTFORML <TEST1> = {FINDELEMENT(LOCAL, 1)}
	PRINTFORML <TEST2> = {FINDELEMENT(LOCAL, 1, 1, 3)}
	PRINTFORML <TEST3> = {FINDLASTELEMENT(LOCAL, 1, 3, 5)}

	LOCALS:0 = 测试内容1
	LOCALS:1 = 测试内容2
	LOCALS:2 = 测试项目1
	LOCALS:3 = 测试项目2
	PRINTFORML <TEST4> = {FINDELEMENT(LOCALS, "测试内容", 0, STRLENS(LOCALS), 0)}
	PRINTFORML <TEST5> = {FINDELEMENT(LOCALS, "测试内容", 0, STRLENS(LOCALS), 1)}
	PRINTFORML <TEST6> = {FINDELEMENT(LOCALS, "测试内容2", 0, STRLENS(LOCALS), 1)}
结果

	<TEST1> = 0
	<TEST2> = 1
	<TEST3> = 4
	<TEST4> = 0
	<TEST5> = -1
	<TEST6> = 1

<br/>
<h4 id="6.25"><font color=MediumBlue>6.25 VARSET <变量名>{, <整形 or 字符串式>, <起始位置>, <中止位置(不取)>}</font></h4>

将第二参数的值代入指定变量所在数组的指定范围
在省略第二参数的情况下,0或空字串被代入
省略第三自变量之后的部分,该数组的所有变量均将被带入
###### 示例
	VARSET FLAG, 0
	VARSET STR, "あああ", 0, 10
	VARSET TA:0:0:0,5678

在这个例子中,FLAG的所有元素都被赋值为0
STR:0到STR:9都被赋值为"あああ"，TA的第三维所有元素都被赋值为5678
同样的事情也可以在ERB上使用FOR-NEXT循环等来完成,但是当循环次数达到数几十万次时,运行时间就不能忽视了
VARSET指令可以比在ERB上的代入更快地完成处理
将角色变量作为VARSET命令的对象时,只用代入指定的角色要素
###### 示例
	VARSET CFLAG:MASTER:0, 0
	VARSET CSTR, ""

在这个例子中MASTER的CFLAG:0 ~ 999(没有变更CFLAG范围的话)都将变成0,但是其他角色的CFLAG不受影响
另外,省略对象的情况和通常一样被认为是TARGET，所以TARGET的CSTR全部变成"".而其他角色的CSTR不受影响
除了一维数组和数组型字符变量以外,DITEMTYPE和TA等使用的时,若不写索引(如VARSET TA),所有元素将都被赋值

<br/>
<h4 id="6.26"><font color=MediumBlue>6.26 CVARSET <角色变量名>{, <索引>, <值>, <起始角色编号>, <结束角色编号(不取)>}</font></h4>

是将指定值带入所有已注册的角色的角色变量指定的元素
效果参考下方示例
对于NAME、ISASSI等一维数组变量,第二参数不会影响处理。因此，在不省略第三个参数时,请指定适当的值
在省略第三参数的情况下,将带入0或""(空字符串)
第二参数也省略的情况下,将代入第0个元素
如果省略了第四参数级以后的部分,值将被带入所有已注册的角色中
###### 示例
	CVARSET CFLAG, 10, 123

该代码等同于下方代码

	REPEAT CHARANUM
		CFLAG:COUNT:10 = 123
	REND

<br/>
<h4 id="6.27"><font color=MediumBlue>6.27 ARRAYSHIFT <对象变量>, <整形 错开位数>, <偏移后的空白区域的初始值>{, <整形 起始位置>, <整形 结束位置>}</font></h4>

以下摘自私家改造版的说明

> 实现了使数组偏移的命令ARRAYSHIFT
> 　格式:ARRAYSHIFT <对象变量>, <错开位数>, <偏移后的空白区域的初始值>{,<起始位置>, <结束位置>}
> 　内容:按照指定的数量错开数组变量,正值向下标增大的方向移动,负值向减小的方向移动
> 　　　　超出数组范围的值将会被清除掉，错开后的空白区域用第二参数指定的值填充
> 　　　　使用可省略的第4和第5自变量,也可以通过使用他们来只移开一部分范围变量

只能用于一维数组和数组型角色变量。不能用于DITEMTYPE和TA等

###### 示例
	LOCAL:0 = 0
	LOCAL:1 = 1
	LOCAL:2 = 2
	LOCAL:3 = 3
	LOCAL:4 = 4
	LOCAL:5 = 5
	LOCAL:6 = 6
	LOCAL:7 = 7
	LOCAL:8 = 8
	LOCAL:9 = 9
	ARRAYSHIFT LOCAL, 1, 495, 2, 4
	FOR INDEX, 0, 10
		PRINTFORML LOCAL:{INDEX} = {LOCAL:INDEX}
	NEXT
结果
	LOCAL:0 = 0
	LOCAL:1 = 1
	LOCAL:2 = 495
	LOCAL:3 = 2
	LOCAL:4 = 3
	LOCAL:5 = 4
	LOCAL:6 = 6
	LOCAL:7 = 7
	LOCAL:8 = 8
	LOCAL:9 = 9

<br/>
<h4 id="6.28"><font color=MediumBlue>6.28 ARRAYREMOVE <对象变量>, <整形 起始位置>, <整形 删除个数></font></h4>

以下摘自私家改造版的说明

> 实现了删除部分数组元素的命令ARRAYREMOVE
> 　格式:ARRAYREMOVE <对象变量>, <起始位置>, <删除个数>
> 　内容:从指定了数组变量的初始值中只删除要素数分,并用后面的值填补
> 　　　　如果你把要删除的元素数设为0或更少,那么从初始值到后面的所有元素都将被删除

只能用于一维数组和数组型角色变量。不能用于DITEMTYPE和TA等

###### 示例

	LOCAL:0 = 0
	LOCAL:1 = 1
	LOCAL:2 = 2
	LOCAL:3 = 3
	LOCAL:4 = 4
	LOCAL:5 = 5
	LOCAL:6 = 6
	LOCAL:7 = 7
	LOCAL:8 = 8
	LOCAL:9 = 9
	ARRAYREMOVE LOCAL, 2, 4
	FOR INDEX, 0, 10
		PRINTFORML LOCAL:{INDEX} = {LOCAL:INDEX}
	NEXT
结果

	LOCAL:0 = 0
	LOCAL:1 = 1
	LOCAL:2 = 6
	LOCAL:3 = 7
	LOCAL:4 = 8
	LOCAL:5 = 9
	LOCAL:6 = 0
	LOCAL:7 = 0
	LOCAL:8 = 0
	LOCAL:9 = 0

<br/>
<h4 id="6.29"><font color=MediumBlue>6.29 ARRAYSORT <对象变量>{, <排序方式(FORWARD or BACK)>, <起始索引>, <整形 对象元素数>}</font></h4>

以下摘自私家改造版的说明

> 实现了数组变量排序的命令ARRAYSORT
> 　格式:ARRAYSORT[对象变量](,[排序方式(FORWARD or BACK)]，[起始索引]，[对象元素数])
> 　内容:从起始索引范围内的元素进行重排序
> 　　　 FORWARD为升序，BACK为降序

<br/>
<h4 id="6.30"><font color=MediumBlue>6.30 ARRAYCOPY <字符串表达式 原始变量名>, <字符串表达式 目标变量名></font></h4>

以下摘自私家改造版的说明

> 实现复制任意数组的命令ARRAYCOPY
> 　格式:ARRAYCOPY <原始变量名>，<目标变量名>
> 　内容:将复制原变量的值复制到复制目标变量
> 　　　 类型变量需要类型相同，维度相同
> 　　　 另外,角色变量不对应(译者不知道啥意思)
> 　　　 元素数量不同的情况下,只复制能复制部分元素

格式示例：ARRAYCOPY "A", "B"

<br/>
<h4 id="6.31"><font color=MediumBlue>6.31 ARRAYMSORT <数组1>{, <数组2>...}</font></h4>

ARRAYMSORT根据array1对所有数组进行升序排序
array1必须是一维排列,但array2可以是多维数组
当array1中有0或空符号串的元素时,将其视为阵列的末端,之后的元素将不再进行排序。
如果array2之后的数组的元素数少于array1的排序元素数,则中断指令,将返回0到RESULT:0中
如果你成功排序了所有阵列,将返回非0的数到RESULT:0中

> @TEST
> #DIM ARRAY1,4
> #DIM ARRAY2,4
> #DIM ARRAY3,4,3
> ARRAY1 = 3,1,2,0
> ARRAY2 = 1001,1002,1003,0
> ARRAY3:0:0 = 1, 101, 2763
> ARRAY3:1:0 = 2, 102, 9615
> ARRAY3:2:0 = 3, 103, 7035
> 
> ARRAYMSORT ARRAY1,ARRAY2,ARRAY3
> PRINTFORML > ARRAY1 == {ARRAY1:0},{ARRAY1:1},{ARRAY1:2},{ARRAY1:3}
> PRINTFORML > ARRAY2 == {ARRAY2:0},{ARRAY2:1},{ARRAY2:2},{ARRAY2:3}
> FOR I,0,3
> 	PRINTFORML > ARRAY3:{I}:0 == {ARRAY3:I:0},{ARRAY3:I:1},{ARRAY3:I:2}
> NEXT
> 
> ;;;结果
> > ARRAY1 == 1,2,3,0
> > ARRAY2 == 1002,1003,1001,0
> > ARRAY3:0:0 == 2,102,9615
> > ARRAY3:1:0 == 3,103,7035
> > ARRAY3:2:0 == 1,101,2763

<br/>
<h4 id="6.32"><font color=MediumBlue>6.32 CUPCHECK <整形 登录角色的编号></font></h4>

以下摘自私家改造版的说明

> CUP、CDOWN对应的UPCHECK即CUPCHECK追加
> 　格式:CUPCHECK <登录角色的编号>
> 　内容:对自变量指定的角色进行UPCHECK，仅此而已

当然UP,DOWN没有影响。另外，虽然UPCHECK显示了结果，但是CUPCHECK的结果不会显示
(译者也不知道怎么用的,所以这个指令就是纯机翻啦)
<br/>

<h3 id="7"><font color=MidNightBlue>7 读写操作</font></h3>
<h4 id="7.1"><font color=MediumBlue>7.1 SAVEDATA <整形 存档编号>, <字符串表达式 备注信息></font></h4>

将当前数据保存在指定编号的存档中
将当前状态保存在第一个参数指定编号的文件中
因为SAVEDATA指令不能调用@SAVEINFO,所以不能用PUTFORM添加存档备注信息
取而代之,用第二个参数来添加存档备注信息
(从1.704开始，你可以使用字符串表达式，而不仅仅是字符串)下面是一个例子

###### 示例
	GETTIME
	STR:0 = %RESULTS:0% {DAY+1}日目
	SAVEDATA 14, STR:0
	SAVEDATA 15, RESULTS:0 + " " + @"{DAY+1}日目"
结果

	[13] ----
	[14] 2009年03月28日 00:31:27 1日目
	[15] 2009年03月28日 00:31:27 1日目
	[17] ----

因为不进行覆写确认等,必要的话请做好备份
你可以通过[CHKDATA](#7.4)指令查询是否已经有数据
SAVEDATA(与SAVEGAME指令不同)可以在脚本的任何位置调用

<br/>
<h4 id="7.2"><font color=MediumBlue>7.2 LOADDATA <整形 存档编号></font></h4>
加载第一个参数指定编号的存档
加载失败的话,会报错
请一定用CHKDATA指令检查是否可以加载后再执行
LOADDATA(与LOADGAME指令不同)可以在脚本的任何位置调用

<br/>
<h4 id="7.3"><font color=MediumBlue>7.3 DELDATA <整形 存档编号></font></h4>
删除指定编号的存档
即使文件不存在也不会出错

<br/>
<h4 id="7.4"><font color=MediumBlue>7.4 CHKDATA <整形 存档编号></font></h4>
获取指定编号存档的数据,并将结果返回到RESULT:0和RESULT:1中
RESULT:0有一下情况,值为0的时候可以读取
0 - 这个存档可以加载
1 - 没有该存档文件
2 - 游戏的代码不同(与gamebase.csv的"コード"值不同的存档,一般是其它游戏的存档)
3 - 版本不同。(gamebase.csv的"版本"值不同)
4 - 有上述以外问题的文件
当RESULT:0为0时,存档的备注信息会被返回到RESULTS:0中,例如:@SAVEINFO的PUTFORM输入的字码串,SAVEDATA的第二参数
当RESULT:0不是0时,会返回错误消息到RESULTS:0中,例如"保留数据的缓冲不同"

<br/>
<h4 id="7.5"><font color=MediumBlue>7.5 SAVENOS <整形></font></h4>

将emuera中玩家设置的"使用するセーブデータ数"(emuera1824中文版中为"使用存档数量")值返回到RESULT:0中,默认是20
INT变量是不能省略的

<br/>
<h4 id="7.7.><font color=MediumBlue>7.7.SAVEGLOBAL</font></h4>

保存变量GLOBAL和GLOBALS.保存到"glover.sav"中
如果在ERH文件中定义了具有GLOBAL和SAVEDATA标志的变量,也会保存他们

<br/>
<h4 id="7.7"><font color=MediumBlue>7.7 LOADGLOBAL</font></h4>

从"glover.sav"中加载GLOBAL和GLOBALS
即使读取失败也不会造成错误
读取成功时返回1,失败时返回0
和通常的保存数据一样,gamebase.csv设定的代码,版本不合适的文件不建议加载

<br/>
<h4 id="7.8"><font color=MediumBlue>7.8 OUTPUTLOG</font></h4>

以下摘自私家改造版的说明

> 实现了日志输出指令OUTPUTLOG
> 　　过度使用会缩短磁盘的寿命,所以要适可而止(译者:现在都什么年代了...)

另外，日志的编码格式是Unicode

<br/>
<h4 id="7.9"><font color=MediumBlue>7.9 SAVECHARA <字符串表达式 文件名>, <字符串表达式 备注信息>, <整形 角色1登录编号>{, <整形 角色2登录编号>, ...}</font></h4>

这是将指定的角色数据保存到文件中的命令
第一个参数指定保存数据的文件名(的一部分)。实际的文件名是"chara_*.dat"
第二个参数是数据的备注信息。之后可以通过[CHKCHARADATA](#7.11)函数来阅读
第三自参数是角色的登录编号,可以同时保存多个角色,但不能同时多次保存一个角色
如果不存在dat文件夹,会尝试创建文件夹,创建失败的话会报错
另外,第一个参数是空字串或者包含文件名中不能使用的字符会报错

<br/>
<h4 id="7.10"><font color=MediumBlue>7.10 LOADCHARA <字符串表达式 文件名></font></h4>

加载第一个参数指定的数据文件。实际的文件名是"chara_*.dat"
读取成功返回1,失败返回0
在加载之前,你应该通过[CHKCHARADATA](#7.11)函数来确认该文件是否可以加载
LOADCHARA是根据被SAVE的角色的数量注册新的角色
因此对现有的登录角色没有影响
要知道追加了多少名角色请比较加载前后的CHARANUM

<br/>
<h4 id="7.11"><font color=MediumBlue>7.11 CHKCHARADATA <字符串表达式 文件名></font></h4>

返回第一个参数指定的数据文件的文件信息。实际的文件名是"chara_*.dat"
可以加载的时候返回0,由于某种原因不可能加载的时候返回其他值
另外,在可以加载的情况下,将保存数据的备注信息返回到RESULTS:0,在不可能加载的情况下,将其理由返回的RESULTS:0

<br/>
<h4 id="7.12"><font color=MediumBlue>7.12 FIND_CHARADATA <字符串表达式 文件名></font></h4>

在dat文件夹中搜索可能成为LOADCHARA对象的文件，并将文件名(chara_*.dat的*部分)返回到RESULTS
会将hit数(发现的文件数)返回到RESULT中
参数可以指定chara_*.dat的*的部分。
例如执行FIND_CHARADATA("\*你\*")时,会查找chara_\*你\*.dat。chara_001你.dat或chara_你ABC.dat会被选中
省略参数时，指定"\*",查找chara_\*.dat。
另外,chara_.dat(\*为空字符串)不能被LOADCHARA指定,所以不会被选中
hit数超过RESULTS要元素个数的情况不会出错,但是超过的部分的文件名不会被返回

<br/>
<h4 id="7.13"><font color=MediumBlue>7.13 SAVETEXT <字符串表达式 文本内容>, <整形 文件编号>{, <整形 保存在sav文件夹>, <整形 用UTF-8编码>}</font></h4>

将在第一个参数的文本保存到textxxx.txt中(例如，如果fileNo是2，则为text02.txt)。
这个命令不会给文本添加或更改标题等,而是直接保存字符串
这条指令通常会受到选项设置的影响,如在sav文件夹中创建,或以UTF-8编码格式保存
如果将第三参数指定为非0,则可以无视该选项并将其强制保存在sav文件夹中。sav文件夹是根据需要创建的。
在第4参数中指定非0时,无视选项并强制保存为UTF-8编码
成功时RESULT:0中返回非0值,失败时返回0。
在短时间内重复写入同一文件的情况下,可能会被杀软误判导致失败,所以成败的检查很重要

<br/>
<h4 id="7.14"><font color=MediumBlue>7.14 LOADTEXT <整形 文件编号>{, <整形 保存在sav文件夹>, <整形 用UTF-8编码>}</font></h4>

会读取textxxx.sav的文本,并将结果返回到RESULTS:0
如果你将第二个参数指定为非0,无论选项如何,都会在sav文件夹中寻找文件
在第三参数中指定非0时,会以UTF-8编码格式读取
如果失败,会返回空字符串
若读取结果也有同名的式中函数,读取结果或空字串将替代返回值存入RESULTS:0中(译者尝试时并没有发现结果会格式化字符串)

<br/>

<h3 id="8"><font color=MidNightBlue>8 日期・时间取得</font></h3>
<h4 id="8.1"><font color=MediumBlue>8.1 GETTIME</font></h4>

将电脑中当前时刻返回到RESULT:0和RESULTS:0中
如果现在的时间是2009年3月28日13时5分23秒678毫秒
则将20090328130523678返回到RESULT:0
将"2009年03月28日13:05:23"返回到RESULT:0
RESULTS:0基本上用于保存数据的备注信息使用
想单独保存年月日的可以把RESULTS:0分离
另外,RESULT:0的精度根据执行的环境不同,会有十几到几十毫秒的误差
(如果只过了几毫秒,可能会返回相同的值)
如果用来测试代码性能,需要注意

<br/>
<h4 id="8.2"><font color=MediumBlue>8.2 GETMILLISECOND</font></h4>

从公元0001年1月1日开始的时间以毫秒为单位计时,结果返回到RESULT:0
因为可以直接进行加减运算，所以比GETTIME更适合调查过程耗时
另外,RESULT:0的精度根据执行的环境不同,会有十几到几十毫秒的误差
(如果只过了几毫秒,可能会返回相同的值)
如果用来测试代码性能,需要注意

<br/>
<h4 id="8.3"><font color=MediumBlue>8.3 GETSECOND</font></h4>

从公元0001年1月1日开始的时间以秒为单位计时,结果返回到RESULT:0
因为可以直接进行加减运算，所以比GETTIME更适合调查过程耗时
<br/>

<h3 id="9"><font color=MidNightBlue>9 输入・WAIT</font></h3>
<h4 id="9.1"><font color=MediumBlue>9.1 FORCEWAIT</font></h4>

右键、宏跳过不能跳过的WAIT命令
达到这个命令的时候将解除跳过状态

<br/>
<h4 id="9.2"><font color=MediumBlue>9.2 INPUT {<整形 默认值>}</font></h4>
<h4 id="9.3"><font color=MediumBlue>9.3 INPUTS {< 字符串 默认值>}</font></h4>

与eramaker相同的指令,通过参数可以设定输入为空时的字符串
省略参数且输入为空的情况下,和以前一样INPUT重新输入,INPUTS的空字串被代入RESULTS进入下一个处理

<br/>
<h4 id="9.4"><font color=MediumBlue>9.4 TINPUT <整形 时间(ms)>, <整形 超时返回值>{, <整形 显示剩余时间> = 1, <字符串表达式 超时文本>}</font></h4>
<h4 id="9.5"><font color=MediumBlue>9.5 TINPUTS <整形 时间(ms)>, <字符串表达式 超时返回值>{, <整形 显示剩余时间> = 1, <字符串表达式 超时文本>}</font></h4>

是有时间限制的输入命令。第一个参数是时间限制(ms),不过,即使设定比100ms更细小的值可能达不到效果
第二个参数是时间到期时的默认返回值
第三个参数显示剩余时间,如果是0就不显示,其他的表示。省略的情况是1(表示)
第四个参数是时间到期时显示的字符串。空字符串的情况消除计时器表示转移到下一个处理
另外,设定第四个参数时,不能省略第三个参数
在TINPUTS中,和INPUTS一样可以使用宏公式
当使用()作为字符串时,请进行转义

<br/>
<h4 id="9.6"><font color=MediumBlue>9.6 TWAIT <整形 时间(ms)>, <整形 接受输入标志></font></h4>

第一个参数是时间限制,第二个参数是输入接受标志。
一直听到倒计时结束
实际行为会随着输入接受标记的指定而变化

* 接受输入标志 = 0:接受输入,输入完成后,即使在限制时间结束前也会继续
* 接受输入标志 ≠ 0:不接受输入(可以强制等待到限制时间结束)

<br/>
<h4 id="9.7"><font color=MediumBlue>9.7 ONEINPUT {<整形 默认值>}</font></h4>
<h4 id="9.8"><font color=MediumBlue>9.8 ONEINPUTS {<字符串表达式 默认值>}</font></h4>

以下摘自私家改造版的说明

> 实现了只能输入一个字符的输入命令ONEINPUT、ONEINPUTS
> 　格式:ONEINPUT or ONEINPUTS
> 　内容:只接受输入一个字符,输入后自动进入下一处理

使用粘贴等一次性粘贴多位数字(多个文字)时,只输入第一位数字(文字)。
和INPUT和INPUTS一样，通过参数可以设定输入空字串时的默认输入值。
但是,在ONEINPUT中指定负值的情况下,或者在ONEINPUTS中指定空字串的情况下,参数无效,行为与没有参数时相同。
另外,将多位数(多个字符)作为默认值时,只有第一位字符是默认输入值
省略参数输入为空的情况下,ONEINPUT和通常一样,需要重新输入
而ONEINPUTS则将空字符串返回,进行下一步处理
另外,这些指令是可以使用Emuera的CONFIG设定的宏命令
不过可能会出问题
在ONEINPUTS中,可以和INPUTS一样使用宏式
当使用()作为字符串时,请进行转义

<br/>
<h4 id="9.9"><font color=MediumBlue>9.9 TONEINPUT <整形 时间(ms)>, <整形 超时返回值>{, <整形 显示剩余时间> = 1, <字符串表达式 超时文本>}</font></h4>
<h4 id="9.10"><font color=MediumBlue>9.10 TONEINPUTS <整形 时间(ms)>, <字符串表达式 超时返回值>{, <整形 显示剩余时间> = 1, <字符串表达式 超时文本>}</font></h4>

参数分别与[TINPUT](#9.4)和[TINPUTS](#9.5)相同
分别具有[ONEINPUT](#9.7)和[TINPUT](#9.4)、ONEINPUTS和[TINPUTS](#9.5)性质的输入接受命令
另外,这些指令是可以使用Emuera的CONFIG设定的宏命令
不过可能会出问题
在TONEINPUTS中,可以和[TINPUTS](#9.5)一样使用宏式
当使用()作为字符串时,请进行转义

<br/>
<h4 id="9.11"><font color=MediumBlue>9.11 WAITANYKEY</font></h4>

等待输入任何一个键,或者鼠标点击的指令
也可以说是WAIT的ONEINPUT版

<br/>
<h4 id="9.12"><font color=MediumBlue>9.12 INPUTMOUSEKEY {<整形 时间(ms)>}</font></h4>

INPUTMOUSEKEY命令是直接识别鼠标和键盘输入的命令。
参数用毫秒来表示TINPUT这种超时处理的时间。
省略参数或指定0以下时不进行超时处理。
这个指令中,[ONEINPUT](#9.7)等捕捉不到的功能键、方向键、PageUp键等也能识别为输入。
另一方面，根据这个命令的输入的接受等待中ESC键和右键的跳过功能,宏功能,其他的功能均不能使用,ESC键右键等被按下也会被它接收
在第二参数中以毫秒为单位指定数值，进行超时处理。INPUTMOUSEKEY的返值最多为5，分别代入RESULT:0, RESULT:1, RESULT:2, RESULT:3, RESULT:4。

> RESULT:0 == 1;检测到鼠标按压。
> > RESULT:1;鼠标按钮-左键0x100000，右键0x200000，中键0x400000。为C# system.windows.forms.mousebuttons列举体整数的值
> > RESULT:2;鼠标X坐标解释器区域的左下为基准。总是正值。
> > RESULT:3;鼠标Y坐标解释器区域的左下为基准。总是负值。
> > RESULT:4;当正在执行CBGSETBMAP并且点击坐标正下方的颜色的不透明度为0xff时，返回颜色的0xrrggbb。不符合的情况下-1。
> RESULT:0 == 2;检测到鼠标滚轮的旋转。
> > RESULT:1;滚动量
> > RESULT:2;鼠标X坐标
> > RESULT:3;鼠标Y坐标
> RESULT:0 == 3;检测到键盘按压
> > RESULT:1;按下的键线。不含修饰代码(Alt,Ctrl,Shift)。KeyCode相当。为C# system.windows.forms.keys列举体整数的值
> > RESULT:2;按下的键线。包含修饰代码。KeyData相当
> RESULT:0 == 4;因超时而结束了

鼠标按钮请参考_virtualkey.erh中的mb_left ~ mb_middle关键代码请参考_virtualkey.erh中的vk_~
关键代码与GETKEY函数相同
请注意鼠标轮的轮量不是1或-1，而是+-120
另外,光标在Emuera画面外能否被检测到鼠标滚轮转动取决于Windows的设定,Emuera无法更改。
初始设置在Windows8.1之前会检测到,但是在Windows10中似乎不会检测到屏幕外的鼠标滚轮
<br/>

<h3 id="10"><font color=MidNightBlue>10 循环</font></h3>
<h4 id="10.1"><font color=MediumBlue>10.1 FOR <整形变量>, <整形 起始>, <整形 中止>{, <整形 步长> = 1}</font></h4>
<h4 id="10.2"><font color=MediumBlue>10.2 NEXT</font></h4>

FOR～NEXT是REPEAT～REND的升级版
１. 该参数指定的变量将被拥有统计轮数,类似REPEAT的COUNT
２. 第一个参数指定的变量将被初始化为这个值（REPEAT总是初始化为0）.
３. 第一个参数指定的变量将在大于等于这个数时结束循环（等同于REPEAT的参数）.
４. 第一个参数指定的变量每轮会增加多少（REPEAT总是1）.

	FOR COUNT, 0, X
		～～
	NEXT
	REPEAT X
		～～
	REND

这两个循环基本上做了同一件事
二者都进行了X轮可被BREAK的循环,循环中BREAK,CONTINUE命令是可以使用的
不同的是FOR～NEXT有初始值和步长
FOR～NEXT是可以用于递归调用的

	FOR Y, 0, 100
		FOR X, 0, 100
			～～
		NEXT
	NEXT

<整形变量>必须不同于这个循环中的其他变量(否则可能导致死循环)
第四个参数<整形 步长>若为被指定,则按1处理
当<整形 步长>为正值时,<整形变量>将在每次循环时都将增肌该值,直至大于等于<整形 中止>时跳出循环
当<整形 步长>为负值时,<整形变量>将在每次循环时都将减去该值,直至小于等于<整形 中止>时跳出循环
如果<整形 步长>为0,则会是一个死循环.将会使用BREAK跳出循环,而非开始循环
<整形 中止>与<整形 步长>在循环中是固定的,中途不能改变
这又2个结果相同的循环例子

	;１
	X = 10
	FOR COUNT:X, 0, X, X/10
		X = 10000
	NEXT
	;２
	FOR COUNT:10, 0, 10, 10/10
		X = 10000
	NEXT

如果通过GOTO或其他指令进入FOR～NEXT,他将无视NEXT继续下一行代码

<br/>
<h4 id="10.3"><font color=MediumBlue>10.3 WHILE <条件></font></h4>
<h4 id="10.4"><font color=MediumBlue>10.4 WEND</font></h4>

REPEAT～REND是类似的[FOR～NEXT](#10.1)一种循化
WHILE <条件>是0时将跳出循环
当条件一直满足时,它会成为死循环,当然,你可以通过BREAK命令跳出循环
如果你的循化次数太多了,EmuEra会给予警告
如果你用GOTO命令跳转进去,当他运行到WEND时会和往常一样跳转到WHILE

<br/>
<h4 id="10.5"><font color=MediumBlue>10.5 DO</font></h4>
<h4 id="10.6"><font color=MediumBlue>10.6 LOOP <条件></font></h4>

和do～while类似, 只有<条件>不为0,do～loop循化就会继续进行
与[WHILE～WEND](#10.3)不同,它至少会被执行一次
如果你用GOTO命令跳转进去,当他运行到LOOP时会和往常一样进行判断并跳转到DO

<br/>
<h4 id="10.7"><font color=MediumBlue>10.7 SELECTCASE <变量></font></h4>
<h4 id="10.8"><font color=MediumBlue>10.8 CASE < CASE 判定条件>{, < CASE 判定条件>, < CASE 判定条件> ……} <条件></font></h4>
<h4 id="10.9"><font color=MediumBlue>10.9 CASEELSE <条件></font></h4>
<h4 id="10.10"><font color=MediumBlue>10.10 ENDSELECT <条件></font></h4>

分支语句,和VB类似
类似于IF的语句:SELECTCASE,可以分出多条分支
SELECTCASE的分支依赖于单个参数值。实践表明,SELECTCASE是EraDev中最常见的分支函数,最简单的用法如下所示

	SELECTCASE X
		CASE 1
			PRINTL X是1.
		CASE 3
			PRINTL X是3.
		CASEELSE
			PRINTL X不是1或3
	ENDSELECT

脚本的分支取决于X的值
若果满足X等于1后,将会运行CASE 1和下一个CASE或CASELESS之间的语句,之后将跳转至ENDSELECT.不满足的话将去判定"CASE 3"
若果没有满足条件的CASE,那么将在运行ENDSELECT之前运行CASELESS
与switch不同,它不会继续运行CASE之外的东西
而且不能通过BREAK跳转到ENDSELECT
如果使用GOTO跳转到SELECTCASE~CASE~CASEELSE~ENDSELECT分支的中,它会像If ~ELSEIF~ELSE~ ENDSELECT一样运行
代码将正常运行,直到遇到CASE,CASEELSE或ENDSELECT。然后代码将跳转到ENDSELECT

CASE条件有以下三种格式
1:向上方示例一样使用单独一个值
2:满足从< 初始值>到< 终止值>的数组
3 一列条件: <条件1>, <条件2>.
可以使用"IS <运算符> <整形>"进行判定,例如"IS <= 30",则X满足小于等于30,将会执行
在“<整形> TO <整形>”的情况下，例如“10 TO 20”，X大于等于10,小于等于20，将会执行
另外,在CASE中可以将多个条件式用","隔开

###### 示例
	SELECTCASE X
		CASE 1
			PRINTL X是1.
		CASE 2,3
			PRINTL X不是1.
			PRINTL X是2或3.
		CASE 10 TO 20
			PRINTL X既不是1也不是2或3
			PRINTL X在10以上20以下。
		CASE IS <= 30
			PRINTL X不是1,2,3及10以上20以下的数
			PRINTL X是30及以下的数
		CASE 40, 5 * 10 TO 6 * 10, IS >= 10 * 10
			PRINTL X大于30
			PRINTL X是40,或50以上60以下,或者100及以上的数
		CASEELSE
			PRINTL X不是30以下,40,或50以上60以下,或者100以上的数
	ENDSELECT

IS和TO必须以"IS <运算符> <整形>"、"<整形> TO <整形>"的形式使用
不能写成"30 < IS"或" (10 TO 20) || (30 TO 40)"
另外,"<整形> TO <整形>"变量在大于等于左边,小于等于时为真
如果右边比左边小的话不会被执行

请注意,在存在多个条件时.会发生逻辑短路
从左到右依次检查条件,如果发现为真的条件,之后的条件将不被判断

你也可以使用STR作为SELECTCASE的参数
在SELECTCASE中指定了STR变量的情况下,CASE的条件式也需要是STR
<br/>

<h3 id="11"><font color=MidNightBlue>11 随机数生成</font></h3>
<h4 id="11.1"><font color=MediumBlue>11.1 RANDOMIZE <整形></font></h4>
<h4 id="11.2"><font color=MediumBlue>11.2 DUMPRAND</font></h4>
<h4 id="11.3"><font color=MediumBlue>11.3 INITRAND</font></h4>

RAND:X是用得到在[0,X)间的随机数的命令

RANDOMIZE是用来初始化随机数的命令
如果初始化的值相同，RAND一定会返回相同的结果

DUMPRAND将当前随机数的状态保存在RANDDATA变量中
INITRAND会读取存储在RANDDATA变量中的数据
请注意,在进行DUMPRAND之前,不要执行INITRAND
如果RANDDATA的值不合适,RAND就不能正常工作

###### 示例
	PRINTFORML {RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}
	RANDOMIZE 23478612
	PRINTFORML {RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}
	RANDOMIZE 23478612
	PRINTFORML {RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}
	DUMPRAND
	PRINTFORML {RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}
	INITRAND
	PRINTFORML {RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}
	INITRAND
	PRINTFORML {RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}/{RAND:100000}
结果

	92539/49469/48337/15839/48368/1604
	34536/91889/81167/22434/87922/95565
	34536/91889/81167/22434/87922/95565
	68286/10690/68868/82610/90769/60789
	68286/10690/68868/82610/90769/60789
	68286/10690/68868/82610/90769/60789

上述结果中,第一行的结果是不确定的。每次执行的结果都不一样
第二行和第三行因为RANDOMIZE的值相同,所以结果是一定的
在第四行之前执行了DUMPRAND指令
在第五行之前使用INITRAND指令,将RAND状态恢复到DUMPRAND指令保存的状态
因此第四行和第五行的结果是一样的
在第六行中再次使用了INITRAND指令,再次得到了相同的结果

RANDDATA变量是存档变量,所以存档前进行DUMPRAND,读档后立即进行INITRAND,这样就可以得到相同的随机数状态
<br/>

<h3 id="12"><font color=MidNightBlue>12 流程控制・调试辅助</font></h3>
<h4 id="12.1"><font color=MediumBlue>12.1 BEGIN <关键字></font></h4>

BEGIN是eramaker时代就存在的命令,但是eumera新增了关键字FIRST和TITLE
BEGIN FIRST,与在标题画面中选择{{{"[0]最初からはじめる"}}}时的效果相同,会执行事件函数@EVENTFIRST。
BEGIN TITLE返回标题画面
两者都不进行变量初始化,请适当配合RESETDATA命令使用

<br/>
<h4 id="12.2"><font color=MediumBlue>12.2 CALLTRAIN <整形 COM编号></font></h4>

是连续命令执行命令。
预先在SELECTCOM:(1 ~)中代入命令号,将要执行的命令的数量作为自变量来执行。

　　SELECTCOM:1 = XXX
　　SELECTCOM:2 = YYY
　　　　　・
　　　　　・
　　　　　・
　　SELECTCOM:N = ZZZ

　　CALLTRAIN N(运行的命令数量)

和正常的命令执行一样,会调用SHOW_STATUS和SHOW_USERCOM,但是不会显示TRAIN命令及USERCOM
如果一定要显示USERCOM的话,可以使用NOSKIP ~ ENDNOSKIP
CALLTRAIN自动执行结束后,会调用系统函数@CALLTRAINEND
但是,请注意@CALLTRAINEND不是事件函数,所以不能被重复定义。
另外,命令的指定使用的命令号不是游戏中的值,而是TRAIN.CSV指定的值。

<br/>
<h4 id="12.3"><font color=MediumBlue>12.3 DOTRAIN <整形></font></h4>

是强制执行TRAIN的命令
只能在@EVENTTRAIN、@SHOW_STATUS、@SHOW_USERCOM、@USERCOM、@EVENTCOMEND以及由此调用的函数中使用
参数中指定的值必须与train.csv中定义的号码相对应
操作与选择命令时相同,初始化UP、DOWN等变量,再将参数赋值给SELECTCOM,然后调用@EVENTCOM,调用@COM{SELECTCOM}……等流程

如果参数小于0,或者值大于TRAINNAME的要素数,则报错,除此之外不再进行判定
即使参数不是train.csv中定义的数字也会强制执行
另外,不调用@COM_ABLE,强制执行
如果有必要,请在DOTRAIN前进行判定

	SIF ( X < 0 || X >= VARSIZE("TRAINNAME") || TRAINNAME:X == "" )
		RETURN
	RESULT = 1
	TRYCALLFORM COM_ABLE{X}
	SIF RESULT == 0
		RETURN
	DOTRAIN X

相反,你也可以使用DOTRAIN来独立实现TRAIN命令。
例如,不使用train.csv,用@SHOW_USERCOM单独打印命令,然后在@USERCOM进行DOTRAIN。
或者也可以让所有的@COM_ABLE都返回0来代替清空train.csv
你也可以选择删除所有的@com_able,并将[replace _replace.csv]的"COM_ABLE初期値"设为0来代替更改@COM_ABLE

另外,如果在[CALLTRAIN](#12.2)的处理过程中进行了DOTRAIN,剩余的[CALLTRAIN](#12.2)就会失效

<br/>
<h4 id="12.4"><font color=MediumBlue>12.4 THROW <格式字符串></font></h4>

是强制性报错,并将第一个参数的内容作为错误信息的命令
<br/>

<h3 id="13"><font color=MidNightBlue>13 CALL・JUMP・GOTO系</font></h3>
<h4 id="13.1"><font color=MediumBlue>13.1 TRYJUMP <字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="13.2"><font color=MediumBlue>13.2 TRYCALL <字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="13.3"><font color=MediumBlue>13.3 TRYGOTO <字符串 函数名></font></h4>

和JUMP、CALL、GOTO一样,但即使指定的函数不存在也不会出错
指定的函数不存在的话什么都不做
TRYJUMP和TRYCALL可以指定参数。详细内容请参考[exfunc函数](https://osdn.net/projects/emuera/wiki/exfunc)中的"自定义函数中的参数指定"一项(译者:和JUMP,CALL一样,函数要啥就给啥,没必要看内容参考)
另外，用TRYGOTO直接进入IF ~ ELSEIF ~ ELSE ~ ENDIF的情况下,像往常一样执行,直至遇到ELSEIF、ELSE、ENDIF,然后跳到ENDIF的下一行
另外，直接进入REPEAT ~ REND的情况下，到REND之前正常运行,然后无视REND,从下一行继续处理
这些处理与GOTO和其他GOTO系统指令是同样的处理。关于其他Emuera中追加的循环分支语法，请参照本页的"[循环分支语法](#10)""[TRYC系统](#14)"

<br/>
<h4 id="13.4"><font color=MediumBlue>13.4 JUMPFORM <格式化字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="13.5"><font color=MediumBlue>13.5 CALLFORM <格式化字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="13.6"><font color=MediumBlue>13.6 GOTOFORM <格式化字符串 函数名></font></h4>

与JUMP、CALL、GOTO相同,可以用格式化字符串指定函数名

###### 示例
	CALLFORM KOJO_{NO:TARGET}_{SELECTCOM}

可以这样使用。JUMPFORM和CALLFORM可以指定参数。详细内容请参考[exfunc函数](https://osdn.net/projects/emuera/wiki/exfunc)中的"自定义函数中的参数指定"一项(译者:和JUMP,CALL一样,函数要啥就给啥,没必要看内容参考)
另外，如果用GOTOFORM直接进入循环分支语句,请参考"[TRYGOTO](#13.3)"或本页的"[循环分支语法](#10)""[TRYC系统](#14)"

<br/>
<h4 id="13.7"><font color=MediumBlue>13.7 TRYJUMPFORM <格式化字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="13.8"><font color=MediumBlue>13.8 TRYCALLFORM <格式化字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="13.9"><font color=MediumBlue>13.9 TRYGOTOFORM <格式化字符串 函数名></font></h4>

与JUMP、CALL、GOTO相同,可以用格式化字符串指定函数名,即调用的函数不存在也不会出错。
TRYJUMPFORM和TRYCALLFORM可以指定参数。详细内容请参考[exfunc函数](https://osdn.net/projects/emuera/wiki/exfunc)中的"自定义函数中的参数指定"一项(译者:和JUMP,CALL一样,函数要啥就给啥,没必要看内容参考)
另外，如果用TRYGOTOFORM直接进入循环分支语句，请参考"[TRYGOTO](#13.3)"或本页的"[循环分支语法](#10)""[TRYC系统](#14)"


<br/>
<h4 id="13.10"><font color=MediumBlue>13.10 CALLF <字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="13.11"><font color=MediumBlue>13.11 CALLFORMF <字符串 函数名> {, <参数1>, <参数2>……}</font></h4>

以下摘自私家改造版的说明

实现了调用式中函数并忽略返回值的指令CALLF,CALLFORMF
　格式:CALLF 函数名, 参数1, ....
　　　　（虽然是式中函数,但可以用普通函数的参数格式调用）
　内容：把式中函数当作普通的函数来调用,并忽略返回值
　　我想做个疑似SETTER，现在我在反省。(译者:感觉这句和命令说明无关,不润色了)

当然，RESULT和RESULTS只要不在调用的式中函数内操作，是不会变化的。

<br/>
<h4 id="13.12"><font color=MediumBlue>13.12 CALLEVENT <字符串 函数名></font></h4>

调用事件函数
不能给出自变量
也不能在事件函数中和从事件函数被调用的函数中使用
<br/>

<h3 id="14"><font color=MidNightBlue>14 CALL・JUMP・GOTO系2 (TRYC-CATCH-ENDCATCH)</font></h3>
<h4 id="14.1"><font color=MediumBlue>14.1 TRYCJUMP <字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="14.2"><font color=MediumBlue>14.2 TRYCCALL <字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="14.3"><font color=MediumBlue>14.3 TRYCGOTO <字符串 函数名></font></h4>
<h4 id="14.4"><font color=MediumBlue>14.4 TRYCJUMPFORM <格式字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="14.5"><font color=MediumBlue>14.5 TRYCCALLFORM <格式字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="14.6"><font color=MediumBlue>14.6 TRYCGOTOFORM <格式字符串 函数名></font></h4>
<h4 id="14.7"><font color=MediumBlue>14.7 CATCH</font></h4>
<h4 id="14.8"><font color=MediumBlue>14.8 ENDCATCH</font></h4>

格式:TRYC系统函数调用~ CATCH ~ ENDCATCH
(TRYC系统有和TRY系统在调用函数时一样)
内容:TRYC系统的函数调用时有没有找到函数的流程分支
语法上和IF ~ ELSE ~ ENDIF一样(不同的是不需要处理有函数的情况)
因此，在通过GOTO等命令直接进入TRYC系统~ CATCH ~ ENDCATCH内的情况下,与IF ~ ELSEIF ~ ELSE ~ ENDIF相同
按照常规执行到CATCH、ENDCATCH,然后跳到ENDCATCH的下一行继续运行
另外,如果用TRYCGOTO直接进入循环分支语句，请参考"[TRYGOTO](#13.3)"或本页的"[循环分支语法](#10)""[TRYC系统](#14)"

	TRYCCALL UNKNOWN_FUNC ;不存在的函数
		有函数时,函数处理后进行的处理(如果没有就省略,直接进入CATCH)
	CATCH
		没有函数时进行的处理
	ENDCATCH

另外,支持嵌套

<br/>
<h4 id="14.9"><font color=MediumBlue>14.9 TRYCALLLIST</font></h4>
<h4 id="14.10"><font color=MediumBlue>14.10 TRYJUMPLIST</font></h4>
<h4 id="14.11"><font color=MediumBlue>14.11 TRYGOTOLIST</font></h4>
<h4 id="14.12"><font color=MediumBlue>14.12 FUNC <字符串 函数名> {, <参数1>, <参数2>……}</font></h4>
<h4 id="14.13"><font color=MediumBlue>14.13 ENDFUNC</font></h4>

该语法用于尝试调用多个函数,并调用第一个发现的函数
TRYLIST ~ ENDFUNC系内不能使用上述以外的语法
另外,在TRYGOTOLIST直接进入循环分支语句，请参考"[TRYGOTO](#13.3)"或本页的"[循环分支语法](#10)""[TRYC系统](#14)"

	TRYCALLLIST
		FUNC 函数1
		FUNC 函数2
	ENDFUNC

依次尝试调用FUNC中指定的函数,如果成功,调用后转到ENDFUNC;如果失败,转到下一行的FUNC(或ENDFUNC)
作用和下面的代码相同

	TRYCCALL 函数1
	CATCH
		TRYCCALL 函数2
		CATCH
		ENDCATCH
	ENDCATCH
<br/>

<h3 id="15"><font color=MidNightBlue>15 RETURN系</font></h3>
<h4 id="15.1"><font color=MediumBlue>15.1 RETURN <整形>{, <整形>, <整形>, ...}</font></h4>

来自eramaker的一个命令,在返值中也可以指定不定量的整形变量和整形表达式
另外,还可以有多个返值。
当指定多个返值时,将依次赋值给RESULT:0、RESULT:1…

<br/>
<h4 id="15.2"><font color=MediumBlue>15.2 RETURNFORM <格式字符串>{，<格式字符串>，<格式字符串>，…}</font></h4>

是RETURN的亚种。
将参数中指定的格式化字符串进行解析,并进行返回
例如，你可以这样做

###### 示例
	A = 100
	CALL TEST
	PRINTFORMW RESULT == {RESULT}

	@TEST
		STR = A * 10
		RETURNFORM %STR%

请注意,与RETURN不同,"%"不被是为余数运算符,而是字串式的开始
###### 示例
	;OK,可以返回A的后两位
	RETURN A % 100

	;错误,因为把"%"之后的内容作为字符串来解读
	RETURNFORM A % 100

另外,还可以有多个返值
当指定多个返值时,将依次赋值给RESULT:0、RESULT:1…

<br/>
<h4 id="15.3"><font color=MediumBlue>15.3 RETURNF <表达式></font></h4>

`是具有#FUNCTION或#FUNCTIONS属性的函数专用命令`
详细请参考[UserMeth ユーザー定義の式中関数](https://osdn.net/projects/emuera/wiki/UserMeth)
不能有多个返值
(译者:简单来说,#FUNCTION的填整形表达式,#FUNCTIONS的填字符串表达式)
<br/>

<h3 id="16"><font color=MidNightBlue>16 DEBUG系</font></h3>

DEBUG类指令只在启动调试模式时运行
非调试模式时不会运行
因为非调试模式时不进行自变量的解析,即使<格式化字符串>有问题也不会出错。

<h4 id="16.1"><font color=MediumBlue>16.1 DEBUGPRINT <字符串></font></h4>
<h4 id="16.2"><font color=MediumBlue>16.2 DEBUGPRINTL <字符串></font></h4>
<h4 id="16.3"><font color=MediumBlue>16.3 DEBUGPRINTFORM <格式化字符串></font></h4>
<h4 id="16.4"><font color=MediumBlue>16.4 DEBUGPRINTFORML <格式化字符串></font></h4>

它们的操作与PRINT指令和PRINTL相似。
不同之处在于输出目的地不是主控台而是调试台
也不受SKIPDISP指令的影响,不能使用n(TODO译者也不知道n是什么)

<br/>
<h4 id="16.5"><font color=MediumBlue>16.5 DEBUGCLEAR</font></h4>

删除调试控制台中所有打印内容

<br/>
<h4 id="16.6"><font color=MediumBlue>16.6 ASSERT <整形></font></h4>

自变量为真(非0)时什么都不做
当自变量为假(0)时,输出错误并停止执行脚本
<br/>

<h3 id="17"><font color=MidNightBlue>17 提示工具系</font></h3>

通过将鼠标光标放在按钮上来控制提示工具的指令。
提示工具的设置方法请参考[exhtml HTML_PRINT関連](https://osdn.net/projects/emuera/wiki/exhtml)
[推荐个中文版的教程](https://miswanting.gitee.io/ecd/translation/HTML_PRINT.html#html-print)
这个译者不怎么会,所以这里基本上都是机翻

<h4 id="17.1"><font color=MediumBlue>17.1 TOOLTIP_SETCOLOR <整形>, <整形></font></h4>

将提示工具的前景和背景色设定为0xrrggbb形式的数值。
指定使用R、G、B值或字符串时请使用COLOR_FROMRGB或COLOR_FROMNAME函数。

<br/>
<h4 id="17.2"><font color=MediumBlue>17.2 TOOLTIP_SETDELAY <整形></font></h4>

设定显示提示工具所需停留时间,以毫秒为单位
误差是500(毫秒),最大值是32767

<br/>
<h4 id="17.3"><font color=MediumBlue>17.3 TOOLTIP_SETDURATION <整形 显示时间></font></h4>

以下摘自私家改造版的说明

　〇添加设置提示工具显示时间的指令TOOLTIP_SETDURATION
　　　格式：TOOLTIP_SETDURATION [显示时间(ms)]
　　　内容：将提示工具的最大显示时间设定为[显示时间(ms)]
　　　引数：[显示时间(ms)]: 0以上的整数值为,若为0的情况下则为默认的行为,由于计时器的特性,在极短的时间内可能不会达到预期的效果
<br/>

<h3 id="18"><font color=MidNightBlue>18 HTML系</font></h3>

利用类似HTML语法的标签进行打印的命令·函数群
详细请参考[exhtml HTML_PRINT関連](https://osdn.net/projects/emuera/wiki/exhtml)

<h4 id="18.1"><font color=MediumBlue>18.1 HTML_PRINT <字符串表达式></font></h4>

使用类似HTML标签的打印指令。
参数不是像PRINT那样的字符串,而是和PRINTS一样的字符串表达式,支持自动换行,所以实际上和PRINTSL的行为很接近。
使用HTML_PRINT绘图不受ALIGNMENT, SETFONT, COLOR, FONTSTYLE指令及其类似指令的影响。
为了得到这些效果全部需要用标签指定

<br/>
<h4 id="18.2"><font color=MediumBlue>18.2 HTML_TAGSPLIT <字符串表达式>{, <整形变量>, <字符串变量>}</font></h4>

将对象字符串解释为HTML字符串,分割成标签和明文,将分割后结果数量返回的RESULT,将分割后的字符串依次返回到RESULTS中
如果指定了第二、第三变量,将返回到指定变量而非RESULT、RESULTS中
如果在分割过程中出现错误,将返回-1到RESULT中
HTML_TAGSPLIT不能验证标签的内容和对应关系是否挣钱
分割数超过RESULTS的数组大小时,超过的部分不会被存入RESULTS。

###### 示例
INPUT_STR内容

	<body>
		测试内容
		<div class="tooltip">Hover over me
			<span class="tooltiptext">Tooltip text</span>
		</div>
	</body>

代码
	#DIM HTML_NUM
	#DIMS HTML_STR, 20
	#DIMS INPUT_STR
	HTML_TAGSPLIT  INPUT_STR, HTML_STR, HTML_NUM
	PRINTFORML HTML_NUM = {HTML_NUM}
	FOR i, 0, HTML_NUM
		PRINTFORML HTML_STR:{i} = %HTML_STR:i%
	NEXT
结果

	HTML_NUM = 9
	HTML_STR:0 = <body>
	HTML_STR:1 = 测试内容
	HTML_STR:2 = <div class="tooltip">
	HTML_STR:3 = Hover over me
	HTML_STR:4 = <span class="tooltiptext">
	HTML_STR:5 = Tooltip text
	HTML_STR:6 = </span>
	HTML_STR:7 = </div>
	HTML_STR:8 = </body>
<br/>

<h3 id="19"><font color=MidNightBlue>19 AWAIT相关</font></h3>

是不经过文本框进行输入的命令、函数群

<h4 id="19.1"><font color=MediumBlue>19.1 AWAIT {<整形 等待时间(ms)>}</font></h4>

暂停ERB的运行,进行Windows的处理。
指定参数,则需等待指定的时间
AWAIT命令会中断Emuera的无限循环警告,防止Emuera进程变成“无响应”。
请在进行需要时间的处理时使用
但是,因为AWAIT命令本身需要一定的执行时间,所以过于频繁的程序运行会很慢
另外,为了不让用户感到不安,建议按照以下顺序显示工作进度

	REDRAW 0
	FOR LCNT, 0, 100
		PRINTSL "工作中・・・ " + TOSTR(LCNT) + "％"
		AWAIT
		CLEARLINE 1
		;花费时间的处理
	NEXT

<br/>
<h4 id="19.2"><font color=MediumBlue>19.2 GETKEY <整形 按键代码></font></h4>

返回键盘和鼠标按钮的状态
如果按下了参数中指定的键,则返回1,如果没有按下则返回0
这个函数只在Emuera的窗口激活时返回1，如果不是激活状态则不管键状态如何都返回0。
关于关键代码的数值和实际的关键的对应,请参考微软公司提供的MSDN的[虚拟键代码](https://learn.microsoft.com/zh-cn/windows/win32/inputdev/virtual-key-codes)

<br/>
<h4 id="19.3"><font color=MediumBlue>19.3 GETKEYTRIGGERED <整形 按键代码></font></h4>

类似于GETKEY(#19.2)返回键盘和鼠标按钮状态。
[GETKEY](#19.2)获取当前是否被按下,而GETKEYTRIGGERED只在被按下时返回1。
也就是说,如果你一直按下去,GETKEY会一直返回1，而GETKEYTRIGGERD只在按下第一次返回1,之后返回0
这个函数只在Emuera的窗口激活时返回1,如果不是激活状态则不管键状态如何都返回0
关于关键代码的数值和实际的关键的对应,请参考微软公司提供的MSDN的[虚拟键代码](https://learn.microsoft.com/zh-cn/windows/win32/inputdev/virtual-key-codes)

<br/>
<h4 id="19.4"><font color=MediumBlue>19.4 MOUSEX</font></h4>
<h4 id="19.5"><font color=MediumBlue>19.5 MOUSEY</font></h4>

获取鼠标光标的当前X坐标或Y坐标。
坐标是以解释器区域的左下位置为(0,0)的相对位置，右侧是x轴的正方向，下方是y轴的正方向。
注意,如果光标在解释器区域内,MOUSEY将返回负值。
解释器区域的宽度可以通过CLIENTWIDTH、CLIENTHEIGHT函数获取
(如果需要以解释器区域左上方为基准的Y坐标，可以通过MOUSEY()+CLIENTHEIGHT()获取)
这个函数即使Emuera的窗口不激活,或者鼠标光标在窗口外也能正常工作

<br/>
<h4 id="19.6"><font color=MediumBlue>19.6 ISACTIVE</font></h4>

返回Emuera的窗口状态。
如果激活,就返回1,如果不激活,就返回0。
<br/>

<h3 id="20"><font color=MidNightBlue>20 图像处理相关</font></h3>

图像处理相关的命令
以G开始的Graphics系命令是用于操作可变更的绘图区域
使用G系指令需要指定绘图方式为GRAPHICS或TEXTRENDERER。
在绘图方式WINAPI被指定的情况下,G系命令不能使用
以SPRITE开头的SPRITE系命令是关于雪碧的命令。
雪碧和resources文件夹中声明的资源一样,也可以用[PRINT_IMG](#1.11)命令进行显示
以CBG开始的是ClientBackground系指令是与解释器区域和背景图像相关的指令

请注意图像处理系统的命令中的颜色指定不是RGB，而是包含α值(不透明度)的ARGB格式
ARGB型用16进制的0xAARRGGBB来表示

图像处理系统的命令的大半都可以作为行内函数调用
作为行内函数调用的情况下,返回值不会存入RESULT中,而是替代自身原本位置
*注:绘图方式在emuera解释器的设置中修改*
(译者:大部分命令不都是这样)

<h4 id="20.1"><font color=MediumBlue>20.1 GCREATE <整形 ID>, <整形 宽>, <整形 高></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
在指定的ID创建指定大小的G图像
G图像的ID必须是0及以上的整数,宽和高必须是1及以上8192几以下之间的整数值
若参数不在这个范围内会报错
如果创建成功,则返回非0值
如果已经创建了指定ID的G图像,则返回0
如果你要重新创建一个新的图像,请使用[GDISPOSE](#20.3)指令来丢弃现有的G图像

这只是个没内容的空白G图像

<br/>
<h4 id="20.2"><font color=MediumBlue>20.2 GCREATEFROMFILE <整形 ID>, <字符串表达式 文件位置></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
用相对路径指定resources文件夹中的图像文件,打开该图像并创建G图像
与在resources文件夹中的csv文件中声明资源时不同,图像文件不会被锁定
如果创建成功,则返回非0值
如果已经创建了指定ID的G图像,则G图像创建失败,该指令将返回0并结束
文件不存在、无法识别为图像、文件尺寸过大等失败的情况也返回0

G图像处理后并不会显示,要想显示需要配合[SPRITECREATE](#20.23)及[PRINT_IMG](#1.11)使用

<br/>
<h4 id="20.3"><font color=MediumBlue>20.3 GDISPOSE <整形 ID></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
丢弃指定ID的G图像
如果废弃成功的话,返回非0值
如果指定ID的G图像未被创建(或已经已废弃的图像),则返回0

<br/>
<h4 id="20.4"><font color=MediumBlue>20.4 GCLEAR <整形 ID>, <整形 cARGB></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
用指定的颜色替换指定ID的G图像内全部内容
如果处理成功,则返回非0
ID或颜色指定不合适的情况下会报错

G图像处理后并不会显示,要想显示需要配合[SPRITECREATE](#20.23)及[PRINT_IMG](#1.11)使用

<br/>
<h4 id="20.5"><font color=MediumBlue>20.5 GFILLRECTANGLE <整形 ID>, <整形 x>, <整形 y>, <整形 宽>, <整形 高></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
在指定ID的G图像中，用(x, y, 宽, 高)绘制指定的四边形。
如果处理成功，则返回非0。
绘制的颜色如果没有通过GSETBRUSH命令预先指定,则以Emuera图标的文字颜色绘制

G图像处理后并不会显示,要想显示需要配合[SPRITECREATE](#20.23)及[PRINT_IMG](#1.11)使用

<br/>
<h4 id="20.6"><font color=MediumBlue>20.6 GDRAWG <整形 桌面ID>, <整形 源图像ID>, <整形 桌面X>, <整形 桌面Y>, <整形 桌面宽>, <整形 桌面高>, <整形 源图像X>, <整形 源图像Y>, <整形 源图像宽>, <整形 源图像高></font></h4>
<h4 id="20.7"><font color=MediumBlue>20.7 GDRAWG <整形 桌面ID>, <整形 源图像ID>, <整形 桌面X>, <整形 桌面Y>, <整形 桌面宽>, <整形 桌面高>, <整形 源图像X>, <整形 源图像Y>, <整形 源图像宽>, <整形 源图像高>, <整形 颜色矩阵></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
将第一个参数指定ID的G图像作为桌面,第二个参数指定ID的G图像作为源图像,然后将源图像粘贴到桌面上
用4个参数指定桌面上要被粘贴的区域大小与位置,用4个参数指定源图像上要用于粘贴的区域与大小
另外,可以将5x5的二维数值排列指定为[颜色矩阵(Color Matrix缩写CM)](https://learn.microsoft.com/zh-cn/dotnet/desktop/winforms/advanced/how-to-use-a-color-matrix-to-transform-a-single-color?view=netframeworkdesktop-4.8),应用该颜色矩阵来绘制
该ColorMatrix的值为256时与Net Framework的ColorMatrix的1相同。也就是说,对角都是256的5x5矩阵就是单位矩阵
如果处理成功,则返回非0值
如果桌面ID或源图像ID指定的G图像不存在,则返回0
即使桌面ID与图像ID相同也可以执行

G图像处理后并不会显示,要想显示需要配合[SPRITECREATE](#20.23)及[PRINT_IMG](#1.11)使用

<br/>
<h4 id="20.8"><font color=MediumBlue>20.8 GDRAWGWITHMASK <整形 桌面ID>, <整形 源图像ID>, <整形 蒙版ID>, <整形 桌面X>, <整形 桌面Y></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
将第一个参数指定ID的G图像作为桌面,第二个参数指定ID的G图像作为源图像,第三个ID指定G图像作为蒙版,然后将源图像与蒙版粘贴到桌面上
通过<整形 桌面X>,<整形 桌面Y>来指定粘贴到桌面的位置
如果处理成功,则返回非0
源图像和蒙版的宽度和高度需要完全一致,而其绘制区域在桌面图像范围内才能成功
具体来说,就是将蒙版的蓝色值作为不透明度应用到源图像上
例如,如果蒙版图像是全白的(也就是说，所有地方的蓝色都是MAX),那么源图像将会像没有蒙版时被绘制
如果蒙版图像是全黑的(即所有地方的蓝色为0),源图像将被视为全透明的,绘制与不绘制没有区别
该指令是由CPU单线程处理的,速度可想而知

图像处理后并不会显示,要想显示需要配合[SPRITECREATE](#20.23)及[PRINT_IMG](#1.11)使用

<br/>
<h4 id="20.9"><font color=MediumBlue>20.9 GDRAWSPRITE <整形 桌面ID>, <字符串表达式 雪碧图></font></h4>
<h4 id="20.10"><font color=MediumBlue>20.10 GDRAWSPRITE <整形 桌面ID>, <字符串表达式 雪碧图>, <整形 桌面X>, <整形 桌面Y></font></h4>
<h4 id="20.11"><font color=MediumBlue>20.11 GDRAWSPRITE <整形 桌面ID>, <字符串表达式 雪碧图>, <整形 桌面X>, <整形 桌面Y>, <整形 桌面宽>, <整形 桌面高></font></h4>
<h4 id="20.12"><font color=MediumBlue>20.12 GDRAWSPRITE <整形 桌面ID>, <字符串表达式 雪碧图>, <整形 桌面X>, <整形 桌面Y>, <整形 桌面宽>, <整形 桌面高>, <整形 颜色矩阵></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
将指定ID的G图片作为桌面,往上绘制指定的雪碧图
可用可选参数,在桌面上指定的XY坐标绘制雪碧图
另外,可用<整形 桌面宽>,<整形 桌面高>指定绘制区域的宽高来拉缩雪碧图
另外,可将5x5的二维数值排列指定为[颜色矩阵(Color Matrix缩写CM)](https://learn.microsoft.com/zh-cn/dotnet/desktop/winforms/advanced/how-to-use-a-color-matrix-to-transform-a-single-color?view=netframeworkdesktop-4.8),应用该颜色矩阵来绘制
该ColorMatrix的值为256时与Net Framework的ColorMatrix的1相同。也就是说,对角都是256的5x5矩阵就是单位矩阵
雪碧图的大小可以通过[SPRITEWIDTH(<字符串表达式 图像名>)](#20.30)和[SPRITEHEIGHT(<字符串表达式 图像名>)](#20.31)函数来获取
如果处理成功,则返回非0值

如果指定了动画雪碧图,只会绘制运行时的一帧

<br/>
<h4 id="20.13"><font color=MediumBlue>20.13 GSETCOLOR <整形 ID>, <整形 cARGB>, <整形 X>, <整形 y></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
将指定ID的G图像的指定位置的像素替换成指定的颜色
如果处理成功，则返回非0
这个命令速度不怎么快
结合[GGETCOLOR](#20.20)命令尝试在大图像中画画会花费很长时间

<br/>
<h4 id="20.14"><font color=MediumBlue>20.14 GSETBRUSH <整形 ID>, <整形 cARGB></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
在指定ID的G图像中设置指定颜色的笔刷
该笔刷会被储存,直到通过[GDISPOSE](#20.3)指令丢弃该G图像
如果处理成功,则返回非0。
可通过GFILLRECTANGLE指令来更改颜色

<br/>
<h4 id="20.15"><font color=MediumBlue>20.15 GSETFONT <整形 ID>, <字符串表达式 字体名>, <整形 字体大小></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
在指定ID的G图像中设置指定大小和名称的字体
该字体会被储存,直到通过[GDISPOSE](#20.3)指令丢弃该G图像
如果处理成功,则返回非0。
但在1.824中没有设置字体的命令与函数

<br/>
<h4 id="20.16"><font color=MediumBlue>20.16 GSETPEN <整形 ID>, <整形 cARGB>, <整形 宽度></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
在指定ID的G图像中设置指定颜色和宽度的画笔
该画笔会被储存,直到通过[GDISPOSE](#20.3)指令丢弃该G	图像
如果处理成功,则返回非0值
但在1.824中没有利用该画笔的命令与函数

<br/>
<h4 id="20.17"><font color=MediumBlue>20.17 GCREATED <整形 ID></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
如果指定ID的G图像存在,则返回1,如果未创建(包括已丢弃的),则返回0。

<br/>
<h4 id="20.18"><font color=MediumBlue>20.18 GWIDTH <整形 ID></font></h4>
<h4 id="20.19"><font color=MediumBlue>20.19 GHEIGHT <整形 ID></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
获取指定ID的G图像宽度或高度
如果G图像还未创建(包括已丢弃的),则返回0。

<br/>
<h4 id="20.20"><font color=MediumBlue>20.20 GGETCOLOR <整形 ID>, <整形 X>, <整形 Y></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
以0xaarrggbb格式的整数值获取指定ID的G图像的指定位置的颜色。
如果G图像还未创建(包括已丢弃的),或者XY不在图像之内,则返回0。

请注意,只有这个指令在失败时返回-1而不是0。
如果获得黑色和全透明位置的颜色,该命令都返回0。

<br/>
<h4 id="20.21"><font color=MediumBlue>20.21 GSAVE <整形 ID>, <整形 文件编号></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
将指定ID的G图像以png格式输出并保存,文件名为fileNo编号
如果处理成功,则返回非0值
例如

	GSAVE 2, 495
	GSAVE 2, 495495
会在sav里创建img0495.png与img495495.png两张图片

<br/>
<h4 id="20.22"><font color=MediumBlue>20.22 GLOAD <整形 ID>, <整形 文件编号></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
打开文件编号为fileNo的图像,并创建G图像
它的行为和[GCREATEFROMFILE](#20.2)命令几乎一样,不同之处在于它不是根据resouces文件夹中的图像,而是根据GSAVE命令保存的图像进行绘制
如果处理成功,则返回非0值
如果已经创建了指定ID的图像,则图像创建失败,该命令将返回0并结束

<br/>
<h4 id="20.23"><font color=MediumBlue>20.23 SPRITECREATE <字符串表达式 雪碧图名>, <整形 ID></font></h4>
<h4 id="20.24"><font color=MediumBlue>20.24 SPRITECREATE <字符串表达式 雪碧图名>, <整形 ID>, <整形 X>, <整形 Y>, <整形 宽>, <整形 高></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
以指定的ID的G图像的全部或一部分创建具有指定资源名的雪碧图资源
通过指定(X,Y,宽,高),可以将G图像进行裁剪
如果创建成功,则返回非0值
如果相同资源名的雪碧已经存在等问题导致失败时,返回0。
因为该雪碧图只存储父G图像的ID和剪切位置,所以如果父G图像发生变化,雪碧图也会发生变化
另外,父G图像被丢弃的话,雪碧图也会被丢弃处理
你可以用resouces文件夹中的csv声明资源来处理你制作的雪碧图
可通过PRINT_IMG命令和HTML_print的IMG标签来绘制雪碧图

<br/>
<h4 id="20.25"><font color=MediumBlue>20.25 SPRITEANIMECREATE <字符串表达式 雪碧图名>, <整形 宽>, <整形 高></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
创建具有指定资源名,宽和高的动画雪碧图。如果创建成功,则返回非0值
相同资源名的雪碧已经存在等问题导致失败时,返回0。
关于动画,你需要根据[SPRITEANIMEADDFRAME](#20.26)命令来添加帧
关于动画雪碧的要点,请参考[resouces](https://osdn.net/projects/emuera/wiki/resources)

<br/>
<h4 id="20.26"><font color=MediumBlue>20.26 SPRITEANIMEADDFRAME <字符串表达式 雪碧图名>, <整形 ID>, <整形 X>, <整形 Y>, <整形 宽>, <整形 高>, <整形 雪碧图X>, <整形 雪碧图Y>, <整形 时间(ms)></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
向指定资源名的雪碧图中添加帧
将指定ID的G图像X,Y,宽,高对应的区域,粘贴到雪碧图指定的XY位置
超出制作动画雪碧时设定的尺寸范围的部分不会被绘制。
在delay中指定显示这个帧的时间,毫秒为单位
如果指定的资源名不存在,或者不是动画雪碧,这个指令失败,什么都不做
成功添加空格时返回1，失败时返回0。

<br/>
<h4 id="20.27"><font color=MediumBlue>20.27 SPRITEDISPOSE <字符串表达式 雪碧图名></font></h4>

丢弃指定的资源名称的雪碧图
如果丢弃成功的话,返回非0值
这个命令不会影响雪碧图的父G图像
可以通过[GDISPOSE](#20.3)指令来释放分配给G图像的内存

<br/>
<h4 id="20.28"><font color=MediumBlue>20.28 SPRITEGETCOLOR <字符串表达式 雪碧图名>, <整形 X>, <整形 Y></font></h4>

以0xaarrggbb形式的整数值获取具有指定的资源名的雪碧图的指定位置的颜色。
如果该雪碧图未创建或已经丢弃的,或者X,Y是图像外的位置,则返回-1。

请注意,这个指令在失败时返回-1而不是0。
如果获得黑色和全透明位置的颜色,该指令返回0。

<br/>
<h4 id="20.29"><font color=MediumBlue>20.29 SPRITECREATED <字符串表达式 雪碧图名></font></h4>

如果已经创建了指定名称的雪碧图,则返回1,如果还没有创建或者已经废弃,则返回0。

<br/>
<h4 id="20.30"><font color=MediumBlue>20.30 SPRITEWIDTH <字符串表达式 雪碧图名></font></h4>
<h4 id="20.31"><font color=MediumBlue>20.31 SPRITEHEIGHT <字符串表达式 雪碧图名></font></h4>


获得指定名称的雪碧图的宽度或高度。
如果该雪碧图没有创建或者已经废弃,则返回0。

<br/>
<h4 id="20.32"><font color=MediumBlue>20.32 SPRITEPOSX <字符串表达式 雪碧图名></font></h4>
<h4 id="20.33"><font color=MediumBlue>20.33 SPRITEPOSY <字符串表达式 雪碧图名></font></h4>

取得指定名称雪碧的相对位置X、Y
如果该雪碧图没有创建或者已经废弃,则返回0。
为了区分相对位置的X、Y是0还是未制作或已废弃,请配合[SPRITECREATED](#20.29)使用

<br/>
<h4 id="20.34"><font color=MediumBlue>20.34 SPRITESETPOS <字符串表达式 雪碧图名>, <整形 X>, <整形 Y></font></h4>

设定指定名称的雪碧的相对位置X, Y。

<br/>
<h4 id="20.35"><font color=MediumBlue>20.35 SPRITEMOVE <字符串表达式 雪碧图名>, <整形 X>, <整形 Y></font></h4>

将指定名称的雪碧的相对位置的X、Y加上指定值
与一下代码效果相同

	SPRITESETPOS spriteName, SPRITEPOSX(spriteName) + movex, SPRITEPOSY(spriteName) + movey

<br/>
<h4 id="20.36"><font color=MediumBlue>20.36 CBGSETG <整形 ID>, <整形 X>, <整形 Y>, <整形 Z></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
将指定ID的G图像显示在解释器固定位置显示(不会随文字滚动)
解释器和G图像的原点均为左下角
x的右侧方向是正的,y的下方方向是正的,画面深处为Z的正方向
Z只能指定0以外的数字。通常文字深度为0,Z为负值的话图像将显示到文字上方

<br/>
<h4 id="20.37"><font color=MediumBlue>20.37 CBGSETSPRITE <字符串表达式 雪碧图名>, <整形 X>, <整形 Y>, <整形 Z></font></h4>

将指定资源名的雪碧图显示在解释器固定位置显示(不会随文字滚动)
解释器和G图像的原点均为左下角
x的右侧方向是正的,y的下方方向是正的,画面深处为Z的正方向
Z只能指定0以外的数字。通常文字深度为0,Z为负值的话图像将显示到文字上方

<br/>
<h4 id="20.38"><font color=MediumBlue>20.38 CBGCLEAR</font></h4>

解除首字母为CBG的各种CBG系命令设定的图像设置

<br/>
<h4 id="20.39"><font color=MediumBlue>20.39 CBGCLEARBUTTON</font></h4>

解除[CBGSETBUTTONSPRITE](#20.43)命令中设置的按钮设置

<br/>
<h4 id="20.40"><font color=MediumBlue>20.40 CBGREMOVERANGE <整形 Zmin>, <整形 Zmax></font></h4>

解除设置Z深度大于等于Zmin小于等于Zmax,由[CBGSETG](#20.36)、[CBGSETSPRITE](#20.37)、[CBGSETBUTTONSPRITE](#20.43)命令设定的图像

<br/>
<h4 id="20.41"><font color=MediumBlue>20.41 CBGREMOVEBMAP</font></h4>

取消[CBGSETBMAPG](#20.34)指令中设置的按钮映射

<br/>
<h4 id="20.42"><font color=MediumBlue>20.42 CBGSETBMAPG <整形 ID></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
将指定ID的G图像设置为解释器固定区域的按钮映射图像
这里设置的按钮映射图像会影响[CBGSETBUTTONSPRITE](#20.43)和[INPUTMOUSEKEY](#9.12)命令
按钮映射图像不会被显示,但是和[CBGSETG](#20.36)命令设定的图像一样,屏幕左下方和图像左下方为原点
鼠标光标正下方的按钮映射图像的颜色会被识别为按钮的值
但是,如果颜色的α值不是255(不透明),就不会被认为是按钮的值
译者:这个按钮映射图像好像只能在屏幕左下角啊

<br/>
<h4 id="20.43"><font color=MediumBlue>20.43 CBGSETBUTTONSPRITE <整形 按钮值>, <字符串表达式 雪碧图名A>, <字符串表达式 雪碧图名B>, <整形 X>, <整形 Y>, <整形 Z></font></h4>
<h4 id="20.44"><font color=MediumBlue>20.44 CBGSETBUTTONSPRITE <整形 按钮值>, <字符串表达式 雪碧图名A>, <字符串表达式 雪碧图名B>, <整形 X>, <整形 Y>, <整形 Z>, <格式化字符串 提示工具></font></h4>

(※仅在绘图方法为GRAPHICS或TEXTRENDERER时可使用)
与[CBGSETBMAPG](#20.42)指令中设定的按钮映射图像联动,设定可选择的按钮。
当鼠标下方的按钮映射图像颜色的0xrrggbb为参数button时显示的雪碧图为雪碧图名B,否则显示的雪碧为雪碧图名A

<雪碧图名A>或<雪碧图名B>可以指定空符号串,在这种情况下不显示任何非选择或选择贴图
关于XYZ的含义和[CBGSETSPRITE](#20.37)相同
可以用<提示工具>指定在选择该按钮的选项中显示的提示工具
你可以为同一个<按钮值>分配多个CBGSETBUTTONSPRITE值,并且不需要匹配按钮的位置
在这种情况下,与图像的xy位置无关,优先显示Z最大的图像的提示工具
在客户端固定区域显示<雪碧图名A>中指定的资源名称的雪碧。
解释器和G图像的原点均为左下角
x的右侧方向是正的,y的下方方向是正的,画面深处为Z的正方向
Z只能指定0以外的数字。通常文字深度为0,Z为负值的话图像将显示到文字上方

<br/>
<h4 id="20.45"><font color=MediumBlue>20.45 SETANIMETIMER <整形 时间(ms)></font></h4>

为动画雪碧指定以毫秒为单位的刷新间隔。
Emuera通常不会在WAIT/INPUT等的时候进行刷新
在等待输入INPUT等信息的时候，你可以通过设置刷新间隔来使动画正常播放
另外,在[TINPUT](#9.4)等有时间限制的命令中不会进行刷新
实际的刷新间隔根据电脑的状态,比指定的时间稍微慢一些
因此,如果绘图间隔与动画的每帧时间值相同,就会频繁地丢帧
请指定比每帧时间足够短的间隔。

这个命令和"每秒帧"的词组无关。
另外,不受[REDRAW](#2.25)命令的刷新抑制的效果
<br/>

<h3 id="21"><font color=MidNightBlue>21 未整理項目</font></h3>
<h4 id="21.1"><font color=MediumBlue>21.1 CLEARTEXTBOX</font></h4>

以下摘自私家改造版的说明

> 〇添加了清空输入栏的命令CLEARTEXTBOX
> 　　　格式:CLEARTEXTBOX
> 　　　内容:删除最底部输入栏的全部文本

译者没有研究明白怎么用

<br/>
<h4 id="21.2"><font color=MediumBlue>21.2 STRDATA</font></h4>

以下摘自私家改造版的说明

> 〇添加了隐藏[PRINTDATA](#1.4),并将结果返回的命令STRDATA
> 　　　格式:STRDATA <存放结果的变量(默认RESULTS)>
> 　　　　　 DATA, DATAFORM, DATALIST ~ ENDATA
> 　　　　　 ENDDATA
> 　　　内容:从用DATA语法指定的字串中随机返回一个。
> 　　　　　 DATALIST语法中的数据系统被换行字符连接并返回。
###### 示例
	STRDATA
	PRINTDATA LOCAL
		DATA (字符串)
		DATAFORM (格式化字符串)
		ENDLIST
	ENDDATA
	PRINTFORML STRDATA的结果: %RESULTS%
	PRINTDATA LOCAL
		DATA (字符串)
		DATAFORM (格式化字符串)
		ENDLIST
	ENDDATA
结果

	STRDATA的结果: (格式化字符串)
	(格式化字符串)

<br/>
<h4 id="21.1"><font color=MediumBlue>21.3 STOPCALLTRAIN</font></h4>

以下摘自私家改造版的说明

> 〇添加了强制终止[CALLTRAIN](#12.2)的指令STOPCALLTRAIN
> 　　格式:STOPCALLTRAIN
> 　　内容:在[CALLTRAIN](#12.2)指令运行的时候被调用的话,结束对[CALLTRAIN](#12.2)
> 　　　　　除此之外什么都不做
