# This is Practice C Compiler

## Theory
### Compiler Composition
- Lexical Analysis(어휘 분석,스캐닝)
- Syntex Analysis(구문 분석, 파싱)
- Sementic Analysis(의미 분석) ----> 중간언어변환
----------------------------------------------------- FrontEnd
-----> 코드 생성
- Optimization(최적화)
- Code Generation(코드 생성)
----------------------------------------------------- BackEnd


### Lexical Analysis

```
Lexical Specification -> 정규 표현식 -> NFA -> DFA -> Minimul DFA or Tavle Driven DFA Impl -> Generate Scanner
                                    |
                                    |
                                    | (RE -> NFA): Thompson`s Construction Algorithm 
                                            |
                                            |
                                            | (NFA -> DFA): Subset Construction Algorithm
                                                   |
                                                   |
                                                   | (DFA -> Minumul DFA): State Minimization Algorithm



```

- Regular Expression: pattern(identifier, keyword ...), Lexeme --> Token
  - Ambiguity(모호성)
    - else vs elsewhere
    - longest match: 갈때까지 가보기, 분석을 최대한 해보는 방식
    - Priority Ordering: 


### Syntax Analysis
