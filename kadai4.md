```uml
@startuml
start
:天気情報 = weather;
if(weather = o) then (true)
:快晴です;
elseif(weather = 1) then (true)
:曇りです;
elseif(weather = 2) then (true)
:雨です;
else (false)
:不明です;
endif
end
@enduml
```

