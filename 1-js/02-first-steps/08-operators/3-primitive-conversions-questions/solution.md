
```js no-beautify
"" + 1 + 0 = "10" // (1)
"" - 1 + 0 = -1 // (2)
true + false = 1
6 / "3" = 2
"2" * "3" = 6
4 + 5 + "px" = "9px"
"$" + 4 + 5 = "$45"
"4" - 2 = 2
"4px" - 2 = NaN
"  -9  " + 5 = "  -9  5" // (3)
"  -9  " - 5 = -14 // (4)
null + 1 = 1 // (5)
undefined + 1 = NaN // (6)
" \t \n" - 2 = -2 // (7)
```

1. الإضافة بسلسلة "" + 1` تحول `1` إلى سلسلة:` "" + 1 = "1" `، وبعد ذلك لدينا" 1 "+ 0` ، يتم تطبيق نفس القاعدة.
2. يعمل الطرح `-` (مثل معظم عمليات الرياضيات) مع الأرقام فقط ، فهو يحول سلسلة فارغة" "" إلى "0".
3. الإضافة بسلسلة تلحق الرقم `5` بالسلسلة.
4. يتحول الطرح دائمًا إلى أرقام ، لذلك يجعل "-9" `رقمًا -9` (تجاهل المسافات حوله).
5. يصبح "null" "0" بعد التحويل الرقمي.
6. يصبح "غير معرّف" "NaN" بعد التحويل الرقمي.
7. يتم قطع أحرف المسافة من بداية السلسلة ونهايتها عند تحويل سلسلة إلى رقم. تتكون السلسلة بأكملها هنا من أحرف مسافة ، مثل `\ t` و` \ n` ومسافة "عادية" بينهما. لذا ، على غرار السلسلة الفارغة ، تصبح `0`.