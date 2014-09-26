php_variable_prefix
===================

I have been using this variables prefixes in order to better organize my codes.<br>
This helps as well when doing any kind of code analysis through an automatet script/tool

<pre>
a - array    - $aRow
b - boolean  - $bExists
o - object   - $oUser
m - mixed    - $mParam
s - string   - $sName
f - function - $fCallback
r - resource - $rFile
i - integer  - $iId
d - double   - $dPrice
</pre>

```php
<?php
$aRow      = [1, 2, 3];              // a - array 
$bExists   = true;                   // b - boolean 
$oUser     = new User();             // o - object
$sName     = 'Mathias Grimm'         // s - string 
$fCallback = function(){echo 'hi';}  // f - function 
$rFile     = fopen('file.txt', 'r'); // r - resource 
$iId       = 12312312;               // i - integer 
$dPrice    = 10.99;                  // d - double 

// m - mixed
function foo($mParam) 
{

}

foo(['name' => 'Mathias Grimm', 'site' => 'phpEmpregos.com' ]);

$oParam       = new stdClass();
$oParam->name = 'Mathias'

foo($oParam);

```