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
