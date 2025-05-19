# PlantUMLサーバー用マクロ

## 使い方

### Gantt用

あまりの面倒くささにマクロを用意してみた

インクルード

```puml
!includeurl https://raw.githubusercontent.com/notstrings/plantuml-macro/main/gantt.puml
```

タスク定義
後者は前提タスク

```puml
$DefTask("[タスクA]","10 days")
$DefTask("[タスクB]","10 days","[タスクA]")
```

マイルストーン定義
何れかのタスクの最後に張り付く

```puml
DefMile("[マイルストーン]","[タスクA],[タスクB]")
```

タスクorマイルストーンを同じ行にレイアウト

```puml
$SameLine("[要件定義暫定]","[要件定義合意]")
```

進捗値の設定

```puml
$SameLine("[タスクA]",75)
```
