# yii2-i18n
This extension is adding all translations into their language files automaticaly.

    php composer.phar require anvipal/yii2-i18n "*"

Just configure your translation compoent like this:

    'i18n' => [
            'class' => \anvipal\i18n\I18N::className(),
            'translations' => [
                'app*' => [
                    'class' => 'yii\i18n\PhpMessageSource',
                    'basePath' => '@app/messages',
                    'fileMap' => [
                        'app' => 'app.php',
                        'app/error' => 'error.php',
                    ],
                ],
            ],
            'autoGenerate' => YII_DEBUG,
        ],
