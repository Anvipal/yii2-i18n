# yii2-i18n
This extension is adding all translations into their language files automaticaly.

php composer.phar require yarisrespect/yii2-i18n "dev-master"

Just configure your translation compoent like this:

    'i18n' => [
            'class' => \yarisrespect\i18n\I18N::className(),
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
