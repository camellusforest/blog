## JS讀書筆記30天 - Day03 函式

<!--more-->

## 函式是什麼？

函式是一個將要執行步驟寫好，包裝成呼叫就能使用的自動化程式區塊。最主要的功能是**解決人工重複性質的工作**，如此便可以省略大量的重複程式碼，讓程式碼簡潔且好維護。



## 函式的寫法

用function宣告函式，為函式命名，函式名稱後先接一個半形小括弧（`()`），緊跟著一個半形大括弧（`{}`），在大括弧中寫下要執行的程式。

要執行函式時，用函式名稱後加半形小括弧呼叫。

```javascript
function sun(){
  // 要執行的程式
}
sun(); // 呼叫函式執行
```

函式若是沒有呼叫，就不會執行。在呼叫時不可忘記函式名稱後的半形小括弧（`()`）。

另外，只要用Chrome開啟包含JavaScript的檔案，可以在Chrome中的Console裡呼叫函式，因為JavaScript在檔案執行時已經被載入。



## 帶參數的函式

寫在函式的半形小括弧（`()`）中。呼叫函式時須在半形小括弧（`()`）中帶入所需型別的參數。

```javascript
// a 為可帶入的參數，可以選擇不寫
function sun(a){
  var num = a*0.8;
  console.log(num);
}
sun(5); // 執行函式
```

目的在於做複雜的運算，或帶入值進入函式。

參數的型別不限，可為 ((5fae6b75-7a68-4465-9af8-4d7167d43755)) |數字、[字串](JS%E8%AE%80%E6%9B%B8%E7%AD%86%E8%A8%9830%E5%A4%A9%20-%20Day02%20%E8%AE%8A%E6%95%B8#%E5%AD%97%E4%B8%B2%EF%BC%88string%EF%BC%89)或[布林](JS%E8%AE%80%E6%9B%B8%E7%AD%86%E8%A8%9830%E5%A4%A9%20-%20Day02%20%E8%AE%8A%E6%95%B8.md#%E8%AE%8A%E6%95%B8%E7%9A%84%E5%9E%8B%E5%88%A5)（須按照[變數](JS%E8%AE%80%E6%9B%B8%E7%AD%86%E8%A8%9830%E5%A4%A9%20-%20Day02%20%E8%AE%8A%E6%95%B8.md)的寫法）。

```javascript
function sun(a,b){
  var num1 = a*0.8;
  var num2 = b*0.5;
  console.log(num1+num2);
}
sun(5,10); // 執行函式
```

可以帶入多個參數進入函式，參數間用半形逗號（`,`）區隔，可以是不同型別。
## 全域變數與區域變數

### 全域變數

會被一直記住，不會被銷毀的變數。

好處是程式中的任何地方都可以使用。

缺點是全域變數多了記憶體會變肥，速度會變慢。

### 區域變數

在函式中宣告一變數，就叫做區域變數。區域變數在函式結束後，會被清除掉，是只存在在function內的變數。

雖然會在function執行完被清除，但仍然可以取得function運算的最後結果。

最大的好處在於可以將記憶體釋放出來。

缺點則是只能用在單一函式中，離開了函式使用，會出現not define的錯誤。

ex：

```javascript
var total;
function sun(num){
  var answer = num*0.8;
  console.log(answer);
}

total = sun(20);
```

其中的answer為區域變數，total為全域變數。所以answer在函式外無法使用，而total不受影響。

```javascript
var total;
function sun(num){
  var total = num*0.8;
  console.log(total); //16
}

sun(20);

console.log(total); //undefined
```

在上面的程式碼中，會發現第一個`console.log(total);`出來的結果是16，但第二個`console.log(total);`出現的卻是undefined。

這是因為第三行中的使用了var，重新宣告了變數，total是在function中被宣告的變數，屬於區域變數，會隨著function執行完成而被消除。

然而第一行全域變數total尚未被賦予型別與值，會出現undefined。

所以上面程式碼中的total是兩個不一樣的變數。

因此，只要使用var，就是一個新變數。



## 帶有return的函式

return寫在半形大括弧`{}`的最後，作用在於回傳函式運算完後的結果，會把值傳出函式。

```javascript
function sun(num){
  var answer = num*0.8;
  return answer;
}

sun(50);
```



## hoisting

就算先使用變數，或是呼叫函式，在JavaScript中，會自動把變數宣告（var 變數的那行）或是函式（function）放在最上面



## 內容參考課程範圍

- 六角學院 JavaScript 入門篇 - 學徒的試煉 Section 5
- 六角學院JS 學徒特訓直播 JS 函式與監聽 35:20到1:20:50
---
title: JS讀書筆記30天 - Day03 函式
---

