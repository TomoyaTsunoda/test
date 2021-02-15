### 候補１
```sequence
WEBサーバ->DBサーバ: データ挿入
Note right of DBサーバ: DataBaseには\nユーザデータが\n格納される
DBサーバ-->WEBサーバ: データ参照
WEBサーバ->>DBサーバ: データ更新
```

### 候補２
```mermaid
sequenceDiagram
    A->B:AとBを実線
    A-->B:AとBを点線 
    A->>B:AからBへ実線矢印
    B-->>A:BからAへ点線矢印
    A -x B:AからBへ×付きの実線矢印
    B --x A:BからAへ×付きの点線矢印
    B->>B:ループ
```

### 候補３
```plantuml
@startuml

actor Entrant

Entrant -> Ticket : Attend Event Request

activate Ticket
Ticket -> Member : Create Member Request

activate Member
Member -> Member : Create Member
Ticket <-- Member : Create Member Response
deactivate Member

Ticket -> Ticket : Create Ticket
Entrant <-- Ticket : Attend Event Response
deactivate Ticket

@enduml
```