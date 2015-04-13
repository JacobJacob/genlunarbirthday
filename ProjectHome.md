## GenLunarBirthday ##
Generate birthday dates base on lunar birthdays for google calendar import
Can be used for notifying birthdays using google calendar

根据农历生日生成可用于谷歌日历导入的csv文件, 然后导入谷歌日历就可以每年收到所有家人的生日提醒了

Generate birthdays up to 2100

生成至2100年的生日

  * [下载](http://code.google.com/p/genlunarbirthday/downloads/list)
  * 从源文件编译: [下载安装Go](http://golang.org/doc/install#install); `go get code.google.com/p/genlunarbirthday`

用法(Windows):
  1. 编辑days.txt文件如下: (-4 代表闰四月)
```
  父亲生日: 1959.01.01
  母亲生日: 1963.-4.01
```
  1. 将days.txt拖到genlunarbirthday.exe上
  1. 或者在命令行输入genlunarbirthday.exe days.txt
  1. 应该会有一个import.csv生成
  1. 可以选择编辑这个文件, 但是要用文本编辑器打开
  1. 在谷歌日历里导入并设置提醒
  1. 每年收到邮件/短信/等等生日提醒

用法2:
  1. 打开 http://play.golang.org/p/pjHLGH_HjP
  1. 修改`const example`的内容
  1. 点击`Run`
  1. 复制粘贴结果到Excel或文本编辑器
```
Usage:
    genlunarbirthday.exe birthdays.txt
Then a import.csv will be created
Example birthday.txt:
"father's birthday": 1959.01.01
"mother's birthday": 1963.-4.01

Subject, Start Date, Start Time, End Date, End Time, Private, All Day Event, Location
"father's birthday", 1959-2-8, 8:00 AM, 1959-2-8, , FALSE, TRUE, HOME
"father's birthday", 1960-1-28, 8:00 AM, 1960-1-28, , FALSE, TRUE, HOME
"father's birthday", 1961-2-15, 8:00 AM, 1961-2-15, , FALSE, TRUE, HOME
...
"father's birthday", 2095-2-5, 8:00 AM, 2095-2-5, , FALSE, TRUE, HOME
"father's birthday", 2096-1-25, 8:00 AM, 2096-1-25, , FALSE, TRUE, HOME
"father's birthday", 2097-2-12, 8:00 AM, 2097-2-12, , FALSE, TRUE, HOME
"father's birthday", 2098-2-1, 8:00 AM, 2098-2-1, , FALSE, TRUE, HOME
"father's birthday", 2099-1-21, 8:00 AM, 2099-1-21, , FALSE, TRUE, HOME
"father's birthday", 2100-2-9, 8:00 AM, 2100-2-9, , FALSE, TRUE, HOME
...
"mother's birthday", 1963-5-23, 8:00 AM, 1963-5-23, , FALSE, TRUE, HOME
"mother's birthday", 1974-5-22, 8:00 AM, 1974-5-22, , FALSE, TRUE, HOME
...
"mother's birthday", 2088-5-21, 8:00 AM, 2088-5-21, , FALSE, TRUE, HOME
"mother's birthday", 2096-5-22, 8:00 AM, 2096-5-22, , FALSE, TRUE, HOME
```