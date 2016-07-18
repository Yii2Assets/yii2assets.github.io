---
layout: post
title:  "Yii2 PDFJS"
date:   2016-07-18 23:02:40 +0700
categories: widget yii2 pdfjs
thumbnail: "pdfjs1.png"
---
Yii2 PDFJS
==========
[![Latest Stable Version](https://poser.pugx.org/yii2assets/yii2-pdfjs/v/stable)](https://packagist.org/packages/yii2assets/yii2-pdfjs) [![Total Downloads](https://poser.pugx.org/yii2assets/yii2-pdfjs/downloads)](https://packagist.org/packages/yii2assets/yii2-pdfjs) [![Latest Unstable Version](https://poser.pugx.org/yii2assets/yii2-pdfjs/v/unstable)](https://packagist.org/packages/yii2assets/yii2-pdfjs) [![License](https://poser.pugx.org/yii2assets/yii2-pdfjs/license)](https://packagist.org/packages/yii2assets/yii2-pdfjs) [![composer.lock](https://poser.pugx.org/yii2assets/yii2-pdfjs/composerlock)](https://packagist.org/packages/yii2assets/yii2-pdfjs)

Yii2 PDFJS bundle of [PDF.js](https://mozilla.github.io/pdf.js/) plugin. PDF.js Portable Document Format (PDF) viewer

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist yii2assets/yii2-pdfjs ">=1.0"
```

or add

```
"yii2assets/yii2-pdfjs": ">=1.0"
```

to the require section of your `composer.json` file.

Config
-----

```php
'modules'=>[
  'pdfjs' => [
       'class' => '\yii2assets\pdfjs\Module',
   ],
],
```

Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
use yii\helpers\Url;
<?= \yii2assets\pdfjs\PdfJs::widget([
  'url'=> Url::base().'/downloads/pdfjs.pdf'
]); ?>
```
![](https://github.com/Yii2Assets/yii2-pdfjs/blob/master/docs/images/pdfjs1.png)

use in modal

```php
use yii\bootstrap\Modal;
use yii\helpers\Url;

Modal::begin([
    'header' => '<h2>Hello world</h2>',
    'toggleButton' => ['label' => 'click me'],
]);

echo \yii2assets\pdfjs\PdfJs::widget([
  'url' => Url::base().'/downloads/manualStart_up.pdf'
]);

Modal::end();

```
![](https://github.com/Yii2Assets/yii2-pdfjs/blob/master/docs/images/pdfjs2.png)

use in fullscreen

```
http://app-url/index.php?r=pdfjs&file=download/pdfjs.pdf
```
![](https://github.com/Yii2Assets/yii2-pdfjs/blob/master/docs/images/pdfjs3.png)


Config width & height
-----
```php
use yii\helpers\Url;
<?= \yii2assets\pdfjs\PdfJs::widget([
  'width'=>'100%',
  'heith'=> '500px',
  'url'=> Url::base().'/downloads/pdfjs.pdf'
]); ?>
```
