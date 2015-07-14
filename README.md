# Wordpress
Данное руководство отображает основые шаги по на развертыванию локального проекта на Wordpress.
## Установка
Архив можно скачать с http://wordpress.org/, либо установить через консоль.
```Shell
wget http://wordpress.org/latest.tar.gz
tar -xzvf latest.tar.gz
```
## Настройка
wp-config.php
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
