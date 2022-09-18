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
  
  //create roman numeral to number lookup table  
  const lookupTable={  
    M: 1000,  
    CM: 900,  
    D: 500,  
    CD: 400,  
    C: 100,  
    XC: 90,  
    L: 50,  
    XL: 40,  
    X: 10,  
    IX: 9,  
    V: 5,  
    IV: 4,  
    I: 1  
  };  
        
  //create roman numeral accumulator  
  let accumulator = '';  
  
  //loop through lookup table  
  for (const key in lookupTable){  
    const numberValue = lookupTable[key];  
    console.log(key, numberValue);  
    //while currentNumber <= num, then subtract currentNumber from num. Add symbol to accumulator  
    while (numberValue <= num){  
      num -= numberValue;  
      accumulator += key;  
    }  
  }  
  
  //return accumulator  
 return accumulator;  
}  
  
convertToRoman(36);
