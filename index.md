<h1>Sıfırdan Php ve MySQL Eğitim Notları</h1>
<div>Bu kod satırlarında hem php kodları hem ise php ile ilgili notlarım yer alacak.</div>
<div>Phpde değişkenler; </div>
  <div>$ işareti ile tanımlanırlar.</div>
  <div>Harf veya _ karakteri ile başlar.</div>
  <div>Sayı ile başlayamazlar.</div>
  <div>Türkçe karakterler içerebilir.</div>
  <div>Büyük-küçük harfe duyarlıdırlar. (case-sensitive)</div>
<div>Atama Operatörü (=)</div>
<h2>Case Sensitive Özelliği(Büyük-Küçük Harfe Duyarlı)</h2>

``` 
<?php 
$degisken="Degisken1";
$Degisken="Degisken2";
$_degisken="Degisken3"; 
echo $degisken; 
?>
Localhost:Degisken1
```
<h2>Php'de Veri Türleri</h2>
<div>Veri Türleri (Data Types)</div>
  <div>String "yazı" 'yazı"</div>
  <div>Integer 500, 200</div>
  <div>Float (Double) 5.5, 7.2</div>
  <div>Boolean (true, false)</div>
  <div>Array (Dizi)</div>
  <div>Objecy (Nesne)</div>
  <div>NULL (Hiçbir şey)</div>
 <div>gettype()Gettype fonksiyonu bize değişkenin hangi veri tipinde olduğunu gösterir.</div>   
  
```
<?php 
$string="yigithan yilmaz";
$int= 500;
$float= 5.5;
$bool= false;
$array= array();
$object= new stdClass;
$null= NULL;
echo gettype($null);
?>
Localhost:NULL
```

<h2>Php'de Sabit Değişkenler</h2>
<div>Sabit Değişkenler;</div>
  <div>define() fonksiyonu ile tanımlanır.</div>
  <div>Türkçe karakterler içerebilir.</div>
  <div>Sayı ile başlayamaz.</div>
  <div>Harf yada _ işareti ile başlar.</div>
  <div>Büyük-küçük harfe duyarlıdır.(case-sensitive)</div>
<div>Veri türlerinde;</div>
  <div>Object hariç tüm veri türlerini kapsar.</div>
  
  ```
  <?php 
$yigithan= "yigithan yilmaz1";
//echo $yigithan;
define("yigithan", "yigithan yilmaz2");
echo yigithan;
?> Localhost:yigithan yilmaz2
```

<h2>Php'de Sihirli Karakterler</h2>
<div>Sihirli Karakterler;</div>
<div> \t = Tab karakteri yerine geçer.</div>
<div> \n = Yeni satır karakteri (new line).</div>
<div> \\ = karakter bir başka sihirli karaktere denk geldiğinde örneğim “\temel\” gibi bir ifade kullanmak istedik. Bu durumda \t tab karakteri olarak algılanacağından tanımlamamış şu şekilde olmalı “\\temel\”.</div>
<div> \$ = çift tırnak içerisindeki ifadelerde değişkeleri kullanabiliyoruz. Fakat biz değişkenin değerini almak değilde kendisini görmek istersek “bu bir \$degisken” şeklinde kullanmalıyız.</div>
<div> \’ = tek tırnak ile tanımladığımız bir ifade içinde tek tırnaklı bir sözcük kullanmamız gerekirse önüne \ işareti eklemek gerekir. Örneğin $degisken = ‘Uğur dedi ki \’merhaba php\’ dedi’ </div>
<div> \” = çift tırnak içinde bir ifade yazarken çift tırnak kullanmamız gerekirse önünde \ eklememiz gerekir.</div>

```
<?php
$test= "yigithan\t\t\t\nyilmaz \\test\ ";
$ad= "Yigithan";
//echo "\$ad değişkeni $ad değerine eşittir.";
echo "Yigithan dedi ki: \"Piyasa benden sorulur\"..";
?> Localhost:Yiğithan dedi ki: "Piyasa benden sorulur"..
```

<h1>Php'de Operatörler</h1>
<h2>Aritmetik Operatörler</h2>
  <div>Toplama +</div>
  <div>Çıkarma -</div>
  <div>Çarpma *</div>
  <div>Bölme /</div>
  <div>Mod (Kalan) %</div>
  
  ```
  <?php
  $a=15;
  $b=4;
  //echo $a + $b;
  //echo $a - $b;
  //echo $a * $b;
  //echo $a / $b;
  //echo $a % $b;
  ?>
  ```
  
  <h2>Atama Operatörleri</h2>
    <div>Değer Atama =</div>
    <div>Arttırarak Değer Atama +=</div>
    <div>Azaltarak Değer Atama -=</div>
    <div>Bölerek Değer Atama /=<div>
    <div>Çarparak Değer Atama *=</div>
    <div>Modunu Alarak Değer Atama %=</div>
    <div>Birleştirme Operatörü .</div>
    <div>Birleştirerek Değer Atama .=</div>
  
  ``` 
 <?php
// $a  +=5; // $a = $a + 5;
// $a  -=5; // $a = $a - 5;
// $a  /=5; // $a = $a / 5; 
// $a  *=5; // $a = $a * 5; 
// $a  %=5; // $a = $a % 5;

$ad= "Yigithan";
$soyad="Yilmaz";

// echo "Yigithan" . "Yilmaz" . 24 . $ad . "yigithan" . $soyad; Localhost= YiğithanYilmaz24YigithanyigithanYilmaz

$ad .="" . $soyad; // $ad = $ad . $soyad; --->Birleştirerek Atama
echo $ad; Localhost=Yigithan Yilmaz
```

<h2>Arttırma ve Azaltma Operatörleri</h2>
  <div>$a++</div>
  <div>++$a</div>
  <div>$a--</div>
  <div>--$a</div>
  
  ```
<?php
$a = 5; 
echo **$a;
echp $a; Localhost=44
?>
 ```
 
<h2>Karşılaştırma Operatörleri</h2>
  <div>Eşittir ==</div>
  <div>Eşit Değildir !=</div>
  <div>Büyüktür > </div>
  <div>Küçüktür < </div>
  <div>Büyükse yada Eşitse >= </div>
  <div>Küçükse yada Eşitse <= </div>
  <div>Denkse === <div>
  <div>Denk Değilse !== </div>

```
<?php
$a = 5;
$b = 6;
Localhostumuza gelen değer true(1) yada false(hiçbir şey) olacaktır.Verilen sayı ve operatöre göre değişir.
echo $a !== $b;
?>
```

<h2>Mantıksal Operatörler</h2>
  <div>&& - AND - Ve</div>
  <div>|| - OR - Ya da</div> 
  <div>! - Değilse</div>
  
```
<?php
$a = 5;
$b = 5;

//echo ($a == $b) && ($a + $b == 9); Burada ilk değerimiz doğru ama ikinci değer yanlış çıktığı için localhost false .
//echo ($a != $b) || ($a + $b == 14) || ($â -$b == 0); Burada yada kullandık biri hatalı ama diğeri doğru lhost true .

echo !($a != $b); Burda eşit değilse dedik üstüne bi de değilse gelirse yeniden eşittir oldu.Lhost:True.
?>
```

<h1>Php'de Koşullu İfadeler</h1>
<h2>If-Else İfadesi</h2>
 
 ```
 <?php
if ($a > $b) {
    echo "a büyüktür b";
} elseif ($a == $b) {
    echo "a eşittir b";
} else {
    echo "a küçüktür b";
}
?>
<?php
2.Örnek
if ($a == 4) {
    echo "a değişkeninin değeri 4'tür";
} elseif ($a == 6) {
    echo "a değişkeninin değeri 6'dır";
} else {
    echo "Hiçbir koşul yerine getirilmedi.";
}
?>
```

<h2>Switch-Case İfadesi</h2>

```
<?php
$a =5;
Switch ($a){
  case 5:
    echo 'a 5'e eşit';
  break;
  case 6:
    echo 'a 6'ya eşit';
  break;
  case $a % 4 ==3:
    echo '7'yi 4'e bölünce kalan 3'tür';
  break;
  default:
    echo'Hiçbir şeye eşit değil';
  break;  
?>
```

<h2>Ternary (Üçlü Operatör Kullanımı)</h2>
  <div>Kısaca anlatayım.İf'i tek satır içinde nası kullanırız.İşte yardımımıza ternany yetişiyor.</div>
  
  ```
<?php
// Uzun Hali //
$a = 5;
if ($a == 5){
  echo "a 5'e eşit";
} else { 
  echo "a 5'e eşit değil";
}
// Ternany Sayesinde Kısa Kullanılmış Hali // 
echo $a == 5 ? "a 5'e eşit" : "a 5'e eşit değil";
?>
```

<h2>If-Else ve Switch-Case İçin Alternatif Sözdizimleri</h2>
