# == ФУНКЦИИ ==

## Математические функции

 Вызываются через модуль `Math`

### Тригонометрия

| функция | описание |
|:---------:|:--------:|
| `Math.sin(x)` | синус  |
| `Math.cos(x)` | косинус |
| `Math.tan(x)` | тангенс |

Все значения x задаются в радианах, чтобы перевести в градусы, изпольузй `Math.PI`

```coffee-script
console.log "sin(90) = #{Math.sin Math.PI/2}"
console.log "cos(45) = #{Math.cos Math.PI/4}"
```

### Математика

| функция | описание |
|:---------:|:--------:|
| `Math.floor(x)` | округление к нулю |
| `Math.round(x)` | округление к ближайшему целому |
| `Math.ceil(x)`  | округление к бесконечности |
| `Math.random()` | случайное число от `0.0` до `1.0` |
| `Math.pow(x, y)` | возвести число `x` в степень `y` |


```coffee-script
x = 4.4
console.log "pow = #{Math.pow x, 2}"
console.log "floor = #{Math.floor x}"
console.log "round = #{Math.round x}"
console.log "ceil  = #{Math.ceil x}"
```


## == ПОЛЬЗОВАТЕЛЬСКИЕ ФУНКЦИИ ==

Функция **именованная** это часть кода, которая выполняет набор операторов языка (и/или вызовов других функций.

Функция записывается в виде:

```coffee-script
имя_функции = () ->
  # код функции c отступом 
  # в 2 пробела от начала имени
```

Параметры функции задаются в `()`, например: `(x, y) ->`.

Если параметров нет, `()` можно не указывать.

Чтобы вернуть значение функции используется оператор `return`. Без оператора `return` возвращается значение, полученное в последнем операторе функции.

Фунции вызываются по имени:
```coffee-script
имя_функции() 

имя_функции X, Y
```

`()` указываются если есть параметры.

Для параметров функции можно задавать значения по умолчанию (см. пример 3)

### == ПРИМЕРЫ  ==

- Функция которая возвращает -10

```coffee-script
f = ->
  -10 # можно записать длиннее : `return -10`
console.log "f() = #{f()}" 
```


- Получить разницу между a и b

```coffee-script
delta = (a,b) ->
  a - b

x = delta 5, 10                 # x = -5
```

- Функция с параметрами по умолчанию

```coffee-script
f_defs = (k=10,x=5,b=4) ->
  k*x + b

par1 = f_defs 20           # = 104
par2 = f_defs 20, 4        # = 84
par3 = f_defs 20, 4, 7     # = 87

console_log "#{par1}, #{par2}, #{par3}"
```