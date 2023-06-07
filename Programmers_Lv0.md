# 변수 출력

- 다음 줄 넘기기 : \n
- `${}`
  console.log(`a = ${a}\nb = ${b}`);

# 동일한 문자열 반복해서 이어붙이기

- 방법1. for문

- 방법2. str.repeat(n)
  console.log(str.repeat(3))

- 방법3. fill()과 join()
  console.log(Array(3).fill('ABC').join('')); //ABCABCABC
  // 값이 존재하지 않는 배열 3개 생성 & 'ABC'로 채우기 & '' 구분자 없이 이어 붙이기

# 대소문자 변경 & 체크

str.toUpperCase();
str.toLowerCase();
if(str === str.toUpperCase()) // 대문자인지 확인

\*\* str[i] = str[i].toLowerCase() // 에러 : 이런식으로 바로 대입 불가. 문자열은 '읽기 전용'으로 수정 불가. 새로운 문자열 만들어서 push하기
\*\* str.replace('world', 'Lee'); //world -> Lee로 문자열 대체하여 '새로운' 문자열 반환

\*\* 배열 추가! push는 배열꺼!
let arr = [];
arr.push(str[i].toLowerCase());하고
마지막에 문자열로 출력할거면 arr.join('');로 문자열화 해줘야 함
\*\* 문자열 추가! 간단히 덧셈으로 +=로 가능! let c = a + b;
ss = "";
ss += i.toLowerCase();
ss는 그대로 문자열임

# 특수문자 출력(이스케이프 처리)

- 방법 1. ``으로 특수문자 둘러싸기
- 방법 2. 특수문자 앞에 \ 넣기

# 삼항 연산자로 바로 대입(할당) 가능

answer = n < m ? 1 : 0; // n < m 이면 1 리턴, 아니면 0 리턴

# eval() - 문자열을 코드로 인식하게 하는 함수(안쓰는게 좋음 eval is evil)

eval(str)
eval('2+2') //4
eval('console.log(1+1)') //콘솔에 2 찍힘

# Falsy : undefined / null / 0 / '' / NaN

Falsy한 값을 거를 필요가 있을 때,
If(!person){
console.log('person이 없습니다.');
}

# 문자열의 합

num += '1'
num += '2'
return num; // 3 아니고 '12'임
// parseInt() 써주기

# 문자열의 합 vs 정수의 합

'1' + '2' = '12'
1 + 2 = 3

# 정수 -> 문자열

num.toString()

# 문자열 -> 배열

arr1 = str1.split('') // 단어별로 잘라서 배열에 담기
arr2 = str2.split(',') // 쉼표 별로 잘라서 배열에 담기
arr3 = str3.split(',', 2) // 쉼표 별로 자르는데 2개만 배열로 저장. 나머지는 버림

# map

const result = numbers.map((number) => number \* 2); //새로운 배열을 반환

\*\* 만약 string인데 map 쓰고 싶다면,
[...str1].map((x,idx) => x + str2[idx]).join('');

# 요소 하나씩 검사

- 문자열 for(let s of str){console.log(s);}
- 배열 arr.forEach(c => console.log(c))

# 문자열

- arr1 = str1.split('') // 문자열 -> 배열
- str.slice() // str.substring()이랑 같음. 문자열 자르기
- for(let s of str){console.log(s);} // 요소 하나하나 검사
- toLowerCase() / toUpperCase()

# 배열

- arr.join(''); // 배열 -> 문자열
- arr.forEach(c => console.log(c)) // 요소 하나하나 검사
- const result = numbers.map((number) => number \* 2);
- arr.push(str[i].toLowerCase());

# 두개의 수 중에 큰 수 선택

Math.max(num1, num2)
