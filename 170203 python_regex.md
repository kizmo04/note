# 정규표현식 (Regular Expressions)

group()
일치하는 패턴 반환해줌


* 0회이상 == 없어도 된다는 의미

.+Lady : 앞에 글자가 하나는 있어야 한다 

.*Lady : 앞에 글자가 없어도 된다

y.. : y랑 뒤에 문자 두개



정규표현식의 패턴문자



r'\b' : r을 붙이는 이유는 이스케잎문자가 아닌 정규표현식의 패턴문자임을 알려주기 위해
패턴 문자열에 항상 r을 붙여준다고 생각하면 편함

정규표현식으로 주민번호, 전화번호 등을 검사할 수 있다

.도 정규표현식 패턴에 포함되므로 리터럴 문자의 .을 표현하려면 \. 으로 이스케잎문자 해줘야함


r = re.findall('\w+(?<=she) was', story)

(?<=she)는 검사조건
\w는 문자열 
was앞에 공백한칸 있고 she가 있는 was만 찾아서 문자열 같이 찯아주느것

\b \B : 독립된 문자 찾는데 그게 문장에 포함돼잇을때? (단어경계는 공백이나, 그런걸 말함)

(expr) : 괄호로 묶인 패턴부분만 리턴된다


### 매칭결과 그룹화
groups() 괄호를 지정한 그룹을 리스트로 나눠서 리턴해줌

### 최소일치와 최대일치
+,*에 갯수를 주고 싶으면 중괄호안에 숫자를 넣으면 된다

