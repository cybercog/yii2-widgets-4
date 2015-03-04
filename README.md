Yii2 Widgets
==================================
This repository contains my widgets for the Yii2 Framework. 

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist golles/yii2-widgets "*"
```

or add

```
"golles/yii2-widgets": "*"
```

to the require section of your `composer.json` file.

Usage
-----

Once the extension is installed, simply use it in your code:

### IframeAutoHeight ###
This widget generates an iframe object in the dom that adjusts it's height automatically based on the height of the iframes content. The result is that it looks like the iframe content is normal page content, it won't look like there is an iframe at all.

Note, this only works on iframes on the same domain.
```php
echo IframeAutoHeight::widget([
    'intervalTime' => 500,
    'noIframeSupportText' => 'Your browser does not support iframes.',
    'iframeOptions' => [
        'id' => 'webalizerIframe',
        'src' => 'http://mydomain.com/iframe.html',
        'width' => '100%',
        'height' => '500px',
        'frameborder' => '0',
        'scrolling' => 'no'
                       
     ]
]);
```
