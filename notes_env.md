**Получение и установка значений настроек**

Для доступа к настройкам существует фасад Config:
```
$value = Config::get('app.timezone');
Config::set('app.timezone', 'America/Chicago');
```
Так же можно использовать функцию config:
```
$value = config('app.timezone');
```
**Получение текущей среды**
Получить текущую среду с помощью метода environment объекта Application:
```
$environment = $app->environment();
```
Так же можно использовать функцию app и фасад App:
```
$environment = app()->environment();
$environment = App::environment();
```
Можено передать аргументы в этот метод чтобы проверить, совпадает ли среда с переданным значением:
```
if ($app->environment('local'))
{
    // Среда - local
}

if ($app->environment('local', 'test'))
{
    // Среда - local ИЛИ test
}
```
