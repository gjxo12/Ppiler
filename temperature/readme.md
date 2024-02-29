## FLEX
- [FLex](https://github.com/westes/flex)
- 토큰화: 구문 분석기를 만드는데 사용, C로 구문 문석 코드 생성 가능
- %% 사이의 문법: [...] 정규식이 평가될때, {} 사이의 코드가 실행됨
- 매칭된 단어의 문자열을 yytex 변수에 저장 및 yylval에 리턴값 돌려줌

```c++
%%
stop printf("Stop command receive\n");
start printf("Start command receive\n");
[0123456789]+           printf("NUMBER\n");
[a-zA-Z][a-zA-Z0-9]*    printf("WORD\n");
%%
```
stop 이란 문자열 또는 정규 표현식을 읽을때, 뒤에 내용 실행됨

`flex test.l`


## BISON
- [BISON](https://github.com/akimd/bison)
- BNF(context-free-grammer)
- 토큰의 정보를 받아서 처리

```
... 정의(definitions) ...
%%
... 규칙(rules) ...
%%
... 함수들(subroutines) ...
```
`bison -d test.y`


## refernece
- This is Simple Tutorial link below
- [Flex/Bison](https://www.joinc.co.kr/w/Site/Development/Env/Yacc)