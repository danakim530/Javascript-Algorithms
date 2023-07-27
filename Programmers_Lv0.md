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

# 문자열 split()

- arr1 = str1.split('') // 문자열 -> 배열
- str.slice() // str.substring()이랑 같음. 문자열 자르기
- for(let s of str){console.log(s);} // 요소 하나하나 검사
- toLowerCase() / toUpperCase()

# 배열 -> 문자열 join() or toString()

- arr.join('');
- var num = 24;
  var str = num.toString();

# 배열

- arr.forEach(c => console.log(c)) // 요소 하나하나 검사
- const result = numbers.map((number) => number \* 2);
- arr.push(str[i].toLowerCase());

# 두개의 수 중에 큰 수 선택

Math.max(num1, num2)

# 문자열 찾기

// 문자열의 시작 위치(숫자) 반환
str.indexOf('javascript') // 위치 리턴
str.index('javascript', 5) // 시작위치 지정 : 5 이후부터 검사

str.search('javascript') // indexOf랑 같은데 시작 위치 지정 불가

str.lastIndexOf('javascript') // 뒤에서부터 검사
str.startsWith('java'); // true or false

// true or false 반환
str.includes('javascript')
str.includes('javascript',3) // 시작 위치 지정 : 3 이후부터 검사

# 제곱

Math.pow(2,3) //2의 세제곱

# 문자열을 숫자화

Number(code[i]) === 1

# forEach와 map의 차이

- forEach : 말 그대로 for문 대체. 리턴하는 것이 없다.
  arr.forEach(n=> {
  squared.push(n+n);
  });

- map : 또 다른 배열을 리턴함.
  const squared = arr.map(n => n+n);

# Number()와 parseInt()의 차이 : 문자열 -> 숫자화

let test = '2020년도';
Number(test); // NAN
parseInt(test); // 2020 - 숫자만 뽑아주기 가능

let test2 = '10.1234';
Number(test2); // 10.1234
parseInt(test2); // 10
parseFloat(test2); // 10.1234

# 배열 중간에 요소 추가/교체/제거

mine = [0,1,2,3,4];
mine.splice(1,1,5); // 배열 1번째부터 1개를 제거하고, 숫자 5를 추가한다.
mine.splice(2,0,5); // 배열 2번째에 숫자 5를 추가
mine.splice(2,3); // 배열 2번째부터 3개 제거

# 배열의 값에 1씩 추가

arr[i]++;
arr[i] += 1;
// 이렇게 직접 접근 가능 arr.splice(i, 1, arr[i]+1) 안해도 됨

# 2차원 배열의 값 수정.. 이렇게 직접 대입해도 됨? splice 안 써도 되나?

queries= [[0, 3],[1, 2],[1, 4]];
// arr의 0번째, 3번째 항의 값을 서로 바꾸는 문제
queries.forEach( ([a,b]) => {
[arr[a],arr[b]] = [arr[b],arr[a]];
})
// 2차원 배열도 forEach 사용 가능

# 2차원 배열

queries= [[0, 3],[1, 2],[1, 4]];
queries[i][j]로 접근

# 2차원 배열 생성하기

// arr[5][2] (빈 배열 생성)
const arr1 = Array.from(Array(5), () => new Array(2)

// arr[5][2] (null로 초기화하여 생성)
const arr2 = Array.from(Array(5), () => Array(2).fill(null))

# 그냥 배열 생성하기 let arr = Array(31).fill(0);

# 숫자의 배열 중 min, max 값 찾기

// Math.min 또는 Math.max 메서드에 배열을 넘기면 NaN이 나옴..배열이 아닌 고유한 숫자를 기대하기 때문
const nums = [1, 2, 3]
Math.min(nums) // NaN
Math.max(nums) // Nan

// 풀어서 보내야 함
Math.min(...nums); //1

# forEach() vs map() : 리턴값 차이!!!

for문은 break; 사용 가능
forEach()는 break; 사용 불가 + 그냥 for문이랑 같음. 리턴하는 것 없음.
map()은 break; 사용 불가 + 새로운 배열 만들어서 리턴함.

function solution(arr) {
return arr.map(num => {
if(num >= 50 && !(num % 2)) return num / 2;
if(num < 50 && num % 2) return num \* 2;
return num;
})
} // 새로운 배열을 뱉어냄

# 문자열 순서 뒤집기

방법1. str.split('').reverse()
// split() : 문자열 -> 배열로
// reverse(0) : 배열을 반전
// join() : 배열 -> 문자열로

방법2. 내림차순으로 for문
for(let i=str.length-1; i>=0; i--){
newString+= str[i];
}

# 문자열/배열 자르기 slice - 뒤에서부터 음수도 가능!

new_arr= arr.slice(1,4); // 1부터 4까지 배열만 가져다 쓰기

var str = '자바스크립트';
var result2 = str.slice(2, 6); // 결과 : "스크립트"
var result3 = str.slice(2); // 결과 : "스크립트"
var result4 = str.slice(-4); // 결과 : "스크립트"
var result6 = str.slice(2, -1); // 결과 : "스크립"

# 맨 뒤 배열 값 빼기 pop()

arr.pop(); // 괄호 안에 아무 것도 안들어감

# 배열 쉽게 만들기 map() vs from()

- 둘 다 새로운 배열을 생성하는데, from() can be used with array-like and iterable objects.

ex. 1부터 31까지의 수를 원소로 갖는 배열

const arr = Array.from(Array(31), (\_, index) => index + 1); // 맵핑 함수의 첫 번째 인자 언더스코어(\_) 는 특별한 인자가 아니라, 불필요한 인자의 공간을 채우기 위한 용도

// 이렇게 for문 안돌려도 됨
for (let i = 1; i <= 31; i++) {
arr.push(i);
}

# 사전순 정렬 sort()

arr1.sort();

# 문자열 있는지 여부 검사

- indexOf() : index 또는 -1 리턴
- includes() : true or false
- startsWith(), endsWith() : true or false

# 절댓값 Math.abs()

# 정확한 개수 모르면 ... rest 연산자 쓰기

arr.splice(a, slicedArr.length , ...slicedArr.reverse());

# 문자열 앞의 n 글자 출력하기 = 그냥 slice(0,n)하면 됨 !

# 문자열 -> ASCII 코드로 변환

"hello".charCodeAt(); // 104 문자열 입력하면, 가장 앞에 있는 문자만 변환됨
"hello".charCodeAt(1); // 101 인덱스 번호 추가 가능!

Str.charCodeAt();
Str.codePointAt();

# ASCII 코드 -> 문자로 변환

String.fromCharCode(97) => 97 -> 'a'로 변환

# reduce

const result2 = numbers.reduce((acc, cur, idx, src) => {
console.log('acc: ', acc, 'cur: ', cur, 'idx: ', idx);
return acc + cur;
}, 0);

"정수 리스트 num_list가 주어집니다. 가장 첫 번째 원소를 1번 원소라고 할 때, 홀수 번째 원소들의 합과 짝수 번째 원소들의 합 중 큰 값을 return 하도록 solution 함수를 완성해주세요. 두 값이 같을 경우 그 값을 return합니다."
function solution(num_list) {
return Math.max(num_list.reduce((acc,cur,idx)=> acc+(idx%2==0? cur: 0),0),
num_list.reduce((acc,cur,idx)=> acc+(idx%2!=0? cur: 0),0) //초기값 입력 안하면 틀림
);
}

# 들어오는 인자의 길이를 모르면 [...my_string] 해줘야 함. 에러남 ㅠ

[...my_string].splice(n,1,0) // 에러 안남
my_string.splice(n,1,0)하니까 에러났음 ㅠㅠ

# filter

.filter(a => a!==0) // a가 0이 아닌 경우만 가져오기 - 새로운 배열을 뱉음

# map() - 1대1로 맵핑하는 것

result = oneTwoThree.map((v) => {
return v + 1;
});
result; // [2, 3, 4]

// 콜백에 3개의 매개변수 있고, thisArg는 콜백에서 this로 사용될 값.
array.map(callbackFunction(currenValue, index, array), thisArg)

# 대표 예제 외우기... 어렵다. [프로그래머스 글자지우기 레벨0]

1. map은 새로운 배열을 리턴
2. 길이가 정해지지 않은 [...my_string]의
3. 요소(c)를 하나하나 돌며 체크
4. i는 인덱스
5. indices배열에 i가 있으면, 0을 대신 넣고, 없으면 현재 요소(c)를 그대로 넣기
6. filter로 0들어가 있는거 지우기
   7 다시 문자열로 변환
   function solution(my_string, indices) {
   return [...my_string].map((c,i) => indices.includes(i)?0:c).filter(n => n!=0).join('');
   }

# if( 2 < num < 4 ) 이렇게 쓰면 안됨!! If(2<num && num<4) &&로 쓰기!!

# reduce랑 map 정복하기!!!

# a부터 b까지 c 간격으로!! for(let i=a; i<=b; i+=c)

나는 i=i+c했는데 그럴 필요 없었음.

또는 a부터 b까지 다 넣고, filter로 거르기.  
numList.slice(a, b + 1).filter((\_, i) => i % c === 0) // 안쓰이는 요소는 \_ 밑에바 처리. 작대기는 Eslint때문에 나옴..

# 앞에서부터 특정 값 찾기 indexOf() / 뒤에서부터 특정 값 찾기 lastIndexOf()

하나 찾으면 동작 그만함.

# 두 배열 합치기 concat => 새로운 배열 뱉음

const concated = arr1.concat(arr2);

# 대체하기 str.replaceAll(a, a.toUpperCase())

문자열 a를 만나면 대문자로 변환

# 문자열의 크기 비교 시, 아스키 코드로 안해도 됨(직접 비교 가능)

[...myString].map((v) => v < 'l' ? 'l' : v).join('');

# 정규표현식 RegExp : 검색!!

// myString 문자열 중 l보다 작은 a-k는 모두 'l'로 변경
const solution = myString => myString.replace(/[a-k]/g,'l')

/a/ : 맨 뒤에 플래그 없으면 최초에 발견된 문자만 반환
/[a-k]/g : 글로벌 플래그, 전역검사하는 것(전체 발견된 모든 결과가 문자열 반환), []는 문자 그룹을 의미, 대괄호 내부의 문자열 중 하나라도 일치하는 경우를 의미

// 아래의 두 정규식은 같습니다
const regex1 = /[A-Z]/;
const regex2 = /[ABCDEFGHIJKLMNOPQRSTUVWXYZ]/;

// 숫자가 아닌 것만 찾아보았습니다
str.match(/[^0-9]/g);

# 배열 삭제 - remove 함수가 없음

arr.pop() - 마지막 요소 삭제
arr.shift() - 첫번째 삭제
arr.splice() - 요소 삭제
arr.filter() - 조건에 맞는 새 배열 생성
delete arr[0] - 빈 값으로 변경이라서 삭제보다는 변경에 가까운 개념

# 공백을 제거 str.trim()

# SQL은 두가지로 풀 수 있음. ORACLE, MySQL

SQL = Structured Query Language (관계형 데이터베이스시스템(RDBMS)에서 자료를 처리하기 위해 설계된 언어)
= DB에 있는 데이터 꺼낼 때 필요한 것. DB가 알아들을 수 있는 유일한 언어. 데이터 추출, 가공 가능.

두 DB의 SQL 쿼리 차이 있음.

- 모든 레코드 조회 SELECT

# 제곱근 Math.sqrt(4) == 2
