多平台翻译、文本语言探测
---

[![Latest Stable Version](http://poser.pugx.org/mouyong/translate/v)](https://packagist.org/packages/mouyong/translate) [![Total Downloads](http://poser.pugx.org/mouyong/translate/downloads)](https://packagist.org/packages/mouyong/translate) [![Latest Unstable Version](http://poser.pugx.org/mouyong/translate/v/unstable)](https://packagist.org/packages/mouyong/translate) [![License](http://poser.pugx.org/mouyong/translate/license)](https://packagist.org/packages/mouyong/translate) [![PHP Version Require](http://poser.pugx.org/mouyong/translate/require/php)](https://packagist.org/packages/mouyong/translate)


项目自动拆分，如需跟踪源码更新情况，请前往：https://github.com/plugins-world/packages 查看 Translate 目录

# 安装

```shell
$ composer require "mouyong/translate" -vvv
```

# 使用


```php
<?php

require __DIR__ . '/vendor/autoload.php';

// jinshan
// $app = new \MouYong\Translate\Translator\Jinshan();

// baidu
// $app = new \MouYong\Translate\Translator\Baidu([
//     // @see http://api.fanyi.baidu.com/manage/developer
//     // 'app_id' => '你的百度翻译 app_id',
//     // 'app_key' => '你的百度翻译 app_key',
// ]);

// youdao
// $app = new \MouYong\Translate\Translator\Youdao([
//     // @see https://ai.youdao.com/console/
//     // 'app_id' => '你的有道智云 app_id',
//     // 'app_key' => '你的有道智云 app_key',
// ]);

// google
// $app = new \MouYong\Translate\Translator\Google\Google([
//     // 需要配置代理
//     'http' => [
//         'proxy' => [
//             'http' => 'http://10.0.30.3:7890',
//             'https' => 'http://10.0.30.3:7890',
//         ]
//     ],
// ]);

// try {
//     $result = $app->translate('测试', 'zh', 'en');
//     var_dump($result->getSrc(), $result->getDst(), $result->getOriginal());
// } catch (\Throwable $e) {
//     var_dump($e->getMessage());
// }
// die;


// 文本内容探测：检测用户输入的内容是哪个国家的语言
$languageRecognizerClient = new \MouYong\Translate\LanguageRecognizer\LanguageRecognizerClient();

$languageRecognizer = $languageRecognizerClient->detect("Словѣ́ньскъ/ⰔⰎⰑⰂⰡⰐⰠⰔⰍⰟ");
var_dump($languageRecognizer->getData());

```

## TODO

[ ] Deepl  
[ ] Bing  
[ ] Tencent  
