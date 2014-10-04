PHP Variable Prefix
===================

I have been using this variables prefixes in order to better organize my codes.<br>
This helps as well when doing any kind of code analysis through an automatet script/tool<br>

Once I had a really nice task (was really nice indeed) to convert an existing system from php4 to php 5.3.<br>
All was done using a combination of php and shell script with lots of regular expression.<br>
Actually this was the time when I learned regular expression.<br>

If we had followed some convetions with variables names, the task would be way easier.<br>

Some people say that just a good name is enough but in this case we had many good names that leaded to very nice problems<br>
Just to give some examples:<br>

Good Bad Names:
---------------

```php
<?php
$date = new TDate();
$date = '2014-09-27';

$today = new TDate();
$today = '2014-09-27';
?>
```


Now, this is the convetions I have been using:
----------------------------------------------


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
?>
```
