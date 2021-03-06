# Wordpress
Данное руководство отображает основые шаги по развертыванию проекта.

## Установка

### Сохраняем

__Zip-архив__
```
https://ru.wordpress.org/latest-ru_RU.zip
```

__Linux__
```
wget https://ru.wordpress.org/latest-ru_RU.zip
```

__Mac OSX__
```
curl -O https://ru.wordpress.org/latest-ru_RU.zip
```

### Распаковываем архив
```
unzip latest-ru_RU.zip
```

### Удаляем архив
```
rm latest-ru_RU.zip
```

### Переносим CMS в рабочую директорию
```
mv wordpress/{*,.*} .; rm -fr wordpress
```

### Меняем права на проект
```
sudo chown -R www:staff .
sudo find . -type f -exec chmod 774 {} \;
sudo find . -type d -exec chmod 775 {} \;
```
## /wp-config.php
```PHP
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
Устанавливаем необходимые плагины.


### Advanced Custom Fields PRO (платный)
https://wordpress.org/plugins/advanced-custom-fields/

PRO-версию необходимо скачать с официального сайта:

http://www.advancedcustomfields.com/my-account/


### Cyr to Lat enhanced
https://wordpress.org/plugins/cyr3lat/

### Custom Upload Dir
https://wordpress.org/plugins/custom-upload-dir/

В настройках `Build a path template:` указываем `/%post_type%/%post_id%/%file_type%`


### Prime Strategy Bread Crumb
https://wordpress.org/plugins/prime-strategy-bread-crumb/


### Scripts-To-Footer
https://wordpress.org/plugins/scripts-to-footerphp/
