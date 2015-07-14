# Wordpress
Данное руководство отображает основые шаги по на развертыванию локального проекта на Wordpress.
## Установка
Архив можно скачать с http://wordpress.org/, либо установить через консоль.
```Shell
wget http://wordpress.org/latest.tar.gz
tar -xzvf latest.tar.gz
```

## Настройка
### wp-config.php
```
/**
 * Ограничиваем количество редакций.
 */
define( 'WP_POST_REVISIONS', 10 );


/**
 * Обновление без FTP.
 */
define( 'FS_METHOD', 'direct' );
```

## Плагины
### wp-content/plugins
Устанавливаем необходимые плагины.


#### Advanced Custom Fields PRO (платный)
https://wordpress.org/plugins/advanced-custom-fields/

PRO-версию необходимо скачать с официального сайта:

http://www.advancedcustomfields.com/my-account/


#### Cyr to Lat enhanced
https://wordpress.org/plugins/cyr3lat/

Для загрузки изображений "@2x" вносим изменения в файл `wp-content/plugins/cyr3lat/cyr-to-lat.php`
```
$title = preg_replace("/[^A-Za-z0-9'_\-\.]/", '-', $title);
``` 
на
```
$title = preg_replace("/[^A-Za-z0-9'_\-\.@]/", '-', $title);
```
