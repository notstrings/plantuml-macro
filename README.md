# PlantUMLサーバー用マクロ

## 使い方

### Gantt用

あまりの面倒くささにマクロを用意してみた

```plantuml
@startgantt
' ガント設定
language ja
projectscale daily with calendar date zoom 1
project starts 2025/01/01
saturday are closed
sunday   are closed
2025/01/01 to 2025/01/05 is closed
hide footbox

!include https://raw.githubusercontent.com/notstrings/plantuml-macro/main/gantt.puml

' ガント本体
title Test

$DefTask("Task1","1w")
$DefTask("Task2","2w")
$DefTask("Task3","1w")
$DefTask("Task4","1w")
$DefTask("Task5","1w")
[Task1]->[Task2]
[Task1]->[Task3]
$DefMile("aaa", "Task1,Task2")
$DefMile("bbb", "Task1,Task3")
$SameRow("aaa,bbb")
```
