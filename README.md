# Roman_Numeral_Converter
JavaScript

Roman Numeral Converter  
Convert the given number into a roman numeral.  
  
Roman numerals	Arabic numerals  
M:	1000,  
CM:	900,  
D:	500,  
CD:	400,  
C:	100,  
XC:	90,  
L:	50,  
XL:	40,  
X:	10,  
IX:	9,  
V:	5,  
IV:	4,  
I:	1  
All roman numerals answers should be provided in upper-case.  
  
## Solution  
  
function convertToRoman(num) {  
  
  &ensp; //create roman numeral to number lookup table  
  &ensp; const lookupTable={  
    &ensp; M: 1000,  
    &ensp; CM: 900,  
    &ensp; D: 500,  
    &ensp; CD: 400,  
    &ensp; C: 100,  
    &ensp; XC: 90,  
    &ensp; L: 50,  
    &ensp; XL: 40,  
    &ensp; X: 10,  
    &ensp; IX: 9,  
    &ensp; V: 5,  
    &ensp; IV: 4,  
    &ensp; I: 1  
  &ensp; };  
        
  //create roman numeral accumulator  
  let accumulator = '';  
  
  //loop through lookup table  
  for (const key in lookupTable){  
    &ensp; const numberValue = lookupTable[key];  
    &ensp; console.log(key, numberValue);  
    &ensp; //while currentNumber <= num, then subtract currentNumber from num. Add symbol to accumulator  
    &ensp;  while (numberValue <= num){  
    &emsp; num -= numberValue;  
    &emsp; accumulator += key;  
    &ensp; }  
  &ensp; }  
  
  &ensp; //return accumulator  
 &ensp; return accumulator;  
}  
  
convertToRoman(36);
