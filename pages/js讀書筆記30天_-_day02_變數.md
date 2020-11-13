---
title: JS讀書筆記30天 - Day02 變數
---

## JS讀書筆記30天 - Day02 變數

<!--more-->

## 什麼是變數？

只要是要被記住的資料，就叫做變數。

ex：

![](https://raw.githubusercontent.com/camellusforest/Image/master/imgs/20200917200238.jpg)

圖中的人數、文字、數字⋯⋯等等，只要有需要被記住，待到後續使用的，就稱為變數。



## 變數的型別

變數的型別可以分為幾種，分別是：

1. 數字（number），下方細說。
2. 字串（string），下方細說。
3. 布林（boolean），值有`true`和`false`兩種。
4. 其他，像是 null、undefined、symbol，這邊只會提到undefined。



## 變數的寫法

首先先用var建立變數，命名變數名稱並宣告，最後賦予一個值。

```javascript
var a = 3;
```

也可以分開寫成兩個步驟：

```javascript
var a;
a=3;
```

只要宣告過後，就可以不用寫var，直接`變數名稱=值`。

但如果沒有賦予變數值，就會出現undefined。（後面會細說）

要確認變數是否有宣告成功，可以用chrome開發者工具中console檢查變數。



## 數字（number）
:PROPERTIES:
:custom_id: 5fae6b75-7a68-4465-9af8-4d7167d43755
:END:

數字的變數宣告方式為：

```javascript
var price = 35;
```

直接在等號後給予數字就可以。
### 數字的運算

數字不只可以直接賦予數值，也可以做運算，把握先乘除、後加減的原則，且運算符號必須是半形，分為加法（`+`）、減法（`-`）、乘法（`*`）、除法（`/`），還有除法後的餘數（`%`）。

另外，數字的運算不僅僅可以用數字作運算，只要該變數被賦予的值是數字，也可以用變數名稱做運算。

ex：

```javascript
var apple = 10;
var grape = 20;
//total變數的算法除了
//var total = 10+20;
var total = apple+grape;
```



## 字串（string）

字串的變數宣告方式為：

```javascript
var girl = 'Jessie';
var boy = 'Andy';
```

等號後在單引號或雙引號內賦值，注意單雙引號皆可，但必須要成雙。

### 字串連結

字串與字串間可以用`+`來將兩個字串連在一起，要特別注意的是，`+`必須為半形，且被連結的兩個字串中間不會有空白。

![螢幕快照 2020-09-17 下午9.24.36](https://raw.githubusercontent.com/camellusforest/Image/master/imgs/20200917212503.png)

所以如果要在字串間加入空白，必須手動插入。

像是在原字串後（引號前）加空白，像是下方的Jessie後面。

![螢幕快照 2020-09-17 下午9.26.31](https://raw.githubusercontent.com/camellusforest/Image/master/imgs/20200917212713.png)

或是增加串連的字串，將空白也當一個字串。

![螢幕快照 2020-09-17 下午9.28.28](https://raw.githubusercontent.com/camellusforest/Image/master/imgs/20200917212850.png)



## 特殊的undefined

undefined表示瀏覽器發現一個變數，但沒有被賦予任何型別和值，是一個空位，目的就是「佔位置」。

此外，undefined不等於not define，not define會出現錯誤。

![螢幕快照 2020-09-17 下午9.12.17](https://raw.githubusercontent.com/camellusforest/Image/master/imgs/20200917211355.png)



## 命名變數的注意事項

1. 變數的開頭**不可以用數字**。
2. **不可用半形連字號**（ -，又稱dash）和**英文句點符號**（ . ，或稱dot）。
3. 要**區分大小寫**，dog和Dog是不一樣的。
4. 建議**語意化**，因為方便以後維護，知道自己在寫什麼。
5. 保留關鍵字不可使用，像是if、case⋯⋯可以參考[保留關鍵字](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Reserved_words)



## 內容參考課程範圍

- 六角學院 JavaScript 入門篇 - 學徒的試煉 Section 4
- 六角學院JS 學徒特訓直播 JS 環境與變數 51:30之前