```uml
@startuml
|nsya|sasd|
|||
|start|start|
|:体力= 10;|:体力= 10;|
|if( 体力 <= 20 ) then (true)|if( 体力 <= 20 ) then (true)|
|:宿屋に泊まる;|:宿屋に泊まる;|
|else (false)|else (false)|
|:頑張ってレベルを上げる;|:頑張ってレベルを上げる;|
|endif|endif|
|end|end|
@enduml
```
```uml
@startuml
start
:体力= 10;
if( 体力 <= 20 ) then (true)
:宿屋に泊まる;
else (false)
:頑張ってレベルを上げる;
endif
end
@enduml
```
