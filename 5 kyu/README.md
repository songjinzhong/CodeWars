## 2016-11-17

[链接1](https://www.codewars.com/kata/decode-the-morse-code/train/javascript)

[链接2](https://www.codewars.com/kata/international-morse-code-encryption/train/javascript)

**描述：**

n this kata you have to write a simple Morse code decoder. While the Morse code is now mostly superceded by voice and digital data communication channels, it still has its use in some applications around the world.

Write a function that will encrypt a given sentence into International Morse Code, both the input and out puts will be strings.

Characters should be separated by a single space. Words should be separated by a triple space.

For example, "HELLO WORLD" should return -> ".... . .-.. .-.. --- .-- --- .-. .-.. -.."

To find out more about Morse Code follow this link: https://en.wikipedia.org/wiki/Morse_code

A preloaded object/dictionary/hash called CHAR_TO_MORSE will be provided to help convert characters to Morse Code.


**代码1：**

```javascript
var alist = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".split("");
var mlist = [".-", "-...", "-.-.", "-..", ".", "..-.", "--.", "....", "..", ".---", "-.-", ".-..", "--", "-.", "---", ".--.", "--.-", ".-.", "...", "-", "..-", "...-", ".--", "-..-", "-.--", "--.."]
var decodeMorse = function(morseCode){
  //your code here
  var dict = {};
  mlist.forEach(function(item, index){
    dict[item] = alist[index];
  });
  var words = morseCode.split("   ");
  return words.map(function(word){
    return word.split(" ").map(item => dict[item]).join("");
  }).join(" ");
}
console.log(decodeMorse('.... . -.--   .--- ..- -.. .'))
```

## 2016-11-18

[链接](http://www.codewars.com/kata/classic-hello-world/train/javascript)

**detail**:

如何构造一个类似这样的用法 `Solution.main(); // Hello World!`

**code**:

```javascript
class Solution{
  static main() {
    console.log("Hello World!");
  }  
}
Solution.main('a');
// 用对象也能实现，感觉跑偏
var Solution = {};
Solution.main = () => {console.log('Hello World!')};
```