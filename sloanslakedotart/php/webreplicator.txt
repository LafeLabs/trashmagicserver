<?php

$dnaurl = "http://sloanslake.art/data/dna.txt";


$baseurl = explode("data/",$dnaurl)[0];
$dnaraw = file_get_contents($dnaurl);
$dna = json_decode($dnaraw);


foreach($dna->web as $value){
    
    copy($baseurl."web/".$value,"web/".$value);
    
}
    



?>
<a href = "index.html">CLICK TO GO TO PAGE</a>
<style>
a{
    font-size:3em;
}
</style>
