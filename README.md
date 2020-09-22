<div align="center">

## Showing Users IP on PHP Generated Picture


</div>

### Description

This is very basic script which will create a PNG picture which shows your IP. (Online demo at http://netsec.lv/hosted/code/ip.php) Vote for Me if you find this script usefull! :) P.S. You will need PHP GD library enabled in php.ini
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[BlowFly](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/blowfly.md)
**Level**          |Beginner
**User Rating**    |4.7 (14 globes from 3 users)
**Compatibility**  |PHP 3\.0, PHP 4\.0
**Category**       |[Graphics/ Sound](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/graphics-sound__8-15.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/blowfly-showing-users-ip-on-php-generated-picture__8-1454/archive/master.zip)





### Source Code

```
<?PHP
header("Content-type: image/png");
//Retrieve users IP.
$ip = $_SERVER['REMOTE_ADDR'];
//Image handler
$im = imagecreate (250, 28);
//Background Color (RGB)
$back = ImageColorAllocate ($im, 255, 255, 255);
//Text Color (RGB)
$text_color = ImageColorAllocate ($im, 0, 200, 0);
//Text to generate
$show_txt = "Your IP is: $ip";
//8 = font size. verdana = font name.
ImageTTFText ($im, 8, 0, 10, 20, $text_color, "verdana", $show_txt);
//Create Image
ImagePNG($im);
?>
```

