> ## VQ1 Remove Even Sub Arrays

**Problem Statement**

You are given a binary string, (string which contains 0's and 1's), You have to perform several operations on this string, in one operation choose a non-empty even length substring containing only 0's or only 1's and remove it from the string.

Your goal is to minimize the final length of the string after performing several operations.It is possible that the final string may become empty, in that case print "KHALI" without quotes.

And it can be proved that there is always an unique string with minimal length after performing the operations.


**Input Description**  

    First line of input contains an intger T denoting number of testcases.
    Next T lines of input contains a binary string S.


**Output Description**  

    for each testcase print the required minimal string.

**Constraints:**  

    1 <= T <= 10
    1 <= |S|  <= 105

**Time Limit:**

    Time Limit: 10000

**Sample Input**

    2
    101001
    1001

**Sample Output**

    10
    KHALI

<hr/>

**Test Case 1**

***Input 1***

    5
    100100100100100100
    1010010011101101010
    1001000100101010
    10010
    1

***Output 1***

    KHALI
    0
    1010
    0
    
<hr/>

**Test Case 2**

***Input 2***

    10
    10100
    10110
    100101001
    0010100101
    100100100
    0101010100101
    0101010101011100
    0001110010100001110
    010
    10

***Output 2***

    101
    1
    0
    KHALI
    1
    01010
    010101010101
    0
    010
    10
    
<hr/>

**Test Case 3**

***Input 3***

    1
    1

***Output 3***

    1    

<hr/>

**Test Case 4**

***Input 4***

    5
    1
    01010
    100100100
    110011001001110100
    1001001

***Output 4***

    1
    01010
    1
    01
    1
    
<hr/>

**Test Case 5**

***Input 5***

    10
    0111011010001010101011110100100001000011101101100010011100101001000011000101100001111011010111001001110001101011101010111010010101010110110101000101011101100101001101110101110111100111000110111100010010111000110111001110111101011100010110000000100111001001101001111110101100010001011110101110101011100011101101011000000010010000001011110010000110001100000010000011101011010111000010111011101101110101100110101000000111110011101111100001101011000101110000110000011110010101100011110101001000101000101100100001000000111011010010001100001101010001111110011101000111010001011101011111010101001101011000011011110110110111100011001001111011111101001010111001101000100010001110000000011001010000100000001010001111000010000001100111001110100001000111000001110001010011110111101010010011001101000111011010100011101100111101100111011011100100111101000000100100001001010100101001110111110110011100100111110101111111100110000010100010100100000000100100000101000000000000111110111111111101010110000011001110010001
    1011000000001100000010000010111001100111111000110001100111011000110011111000101000100101101000011111110110100011111000111001000111101111100010111000101110101100000010001010000111011001100000100100000110010010001010100100111010011100101100011101101000000011010111100000111000000010111111100011111011000101110111010011111101001100001000011000010001100110011001111100101110001110000110111011000100110011101010111101001000000010101010110100100110111101100000101101111010101001011001111010100101001100101000111100010110110001000010000010010000110100100001100101010100100101100100110100100110111000110110011010111000011001011000001010001011101000010101110111011010100111111000111110000001100111100110000101010110101000111101101001001111100111111001101010011001010010100111001011111011111101000110001001110001101010100101100010110011101110111100000000110111001011111110000110110100100111111010111111101010010110000100000001100010110101100100111000011101111001001110110011001011110001110101101010100000111010
    0101000111111010101000000111101010011101101100110100011011101010111001010000101011000010100001110011011111000100000111001001001101100101111101110110000101000000000001010111010110000001001110010001100000110000111010011110111011000110101010111010001101100100011100011100111010111010101110011011010011111101000000100100000001010101010011000010010100010000100001000011101000001110110101110010101000011100101101111000101001111001001110011001000000010010001101010101111110101001111101011011011100100000111010000001011000100100001110000000010111111001000111100001000001110011100011000100010011100101010011101101111011101111010000101010100000111101100111111101000111101111000111101010101101001010011001100100000111111110110110110100001000011100011010001101010100100111111111010010111101010111101001111110111110100110011010000011111101011000010001100101110011110010110001100111001001111110011000100100011111001010011101010010111010001011001110100010111001001001010010100100010001100110100000011010110110011011
    0100110001110100100101011110111100001101111100111111000111010010001000111001111110000010110110110001111000110111110100100011001000110100000010100000001101111111111000010000111011001100100001001110110100010000101101111101111000010100011100101011101100001000000000111010010010011110011100010111101111101101011001110111100110100101100101110111010101010001000101000000011010011101110001110011001001111101011101101110010001110100110110111010100110000110011011111100000110000001001101110011000110110010010011111000111111100111101001110100110101111101100000011001111010100010100000000001001010001110110111001110100000101011100110010101101011001011010100011111000010100110111101101111000100101111000100001011001101100100001000001001011111110000101010101010111110110111000110011101101110100011000100010101110110101110011000010000010101101000010101011000011010001001000011000001100100001011101110110010000110101110000010101100101111101111101000010110010110100010111110001101010001001011011110011100010000111001
    1010001011010101000000101001000010101101101101010100010011010100011111101001101101000000101101100010001100010010010011100101111110101110101000110101010010100010100100000101101001111110100010111010111101001111101100100001101100001011101001011101100001100001111001101001111101010100010011110111010011100010001011001111101101110110100011001011110011111101001001010100001101110101111000010010010100110100101100101001000010010000110011011001101100001100110111100000100010010111000000100110011110000001111101010100100001010101011101011101100110000011101110111111000101100100100000111000000100100001010011111011001010100000101000111000000001100111101011001101001011100011100001010011011000011011001011001100000000001011010110000011000010110100110010110110110011100011111100001101101100101001011001000111011110000001000111101000000010110111010110110011001100001001110111011110111111001010000001000011000111001101011110001101000011001100000011101100001101010001010100010100100010000010011001100100100101011001
    1011011110000100101010010010010000111111001100000110011111111000101111110110110100100010001000010000101111111101101101011010100011001101010111010000011110011010101000010001101000111010100110000001110010001111100110000101011001100101010100011101010011000110110011100111010001110011111110011110001100110111000010010010010110100000010110100000010110000110110010110100010111000011001100101010101000100100111111010110001101001011100001011100101011100110101110101000111010011010111000000010101011001011010001000110100000010010110101011101110100101111010100111101010101001100100100011101101110101011101011111100110000011100101011011000001011101010011110100001011100010010101100001010101010001010100000000100010011000000100011101010011100011010111110011011100010001110010000110011110101100101111110001011011000000001100101100101101001011100101001001001011010110111000101101011011001110001111011100001111011000110000101111110000010101111000010001010000010011111000011111100100000011000000011111010001000001001
    0001111101111000001000011110101011011010111101000010101101111010111101011110010001000001100110010110100110000111010000000100001010100001010010100110111111111010100101010101111110111010111101101111110010110110010010111000111111111001000010010001110110111000000100100110111010011101011111101101001100010001001000111101001001011011100000010010011001010010100101101110011110111100011110011100101001011100110100010011111101010000010010011100101000001101001101001111011010001101000101000111011011000000110000000100100010000001001111010010111001110100100100111000101111100000100101101000110001011100100110111100111011011011111110001011011101110101001000100110110011010011101110101100110010011100000100101000000100000101011001001000011010001101001101100110000001010110010011001000010000111000010101110011001101010101010001111001000011000000011001000110011000111100101001110000010111001000110111110110100000110000100111111110000001001100111100111010011100000001111001010011010011110111010011011011111001010111
    1011000111010111101101100000101011100011100110110001010110110111011000011101010110110111011011100000000011001010100010011011000010000011010000100100010011010000010101101101000001011101111011010001111001001111110011111000001000011101101100010110000100000110100101100000111001100011010010000000101100010001101110101000001001111111111101010110001000100010010100010111100111110110100000001110000101101101011010010100100000010000001011001110000111000110110101011000011011000100100111100110001111101010111101001101010000011101011101011011000100000100100100110101001100010111000011001011100100011101011101100001000101011000011100000011101001100010111101000111011011000001100000110011001011001100001011110011100111100111001100010110011100110100001100000011110011000101100111001101100000000011100100100110010100100110100100010110110110100000101001011110110110100010000011011110110010111011101111011000101111010001100010111000011001010001110111100000001001001110100000011001000001110111101101111001110001001000
    1011000001101100110111000100000000101011010110110110110101101010111010111110011000000101100111111100010100111011110010111010000110010101010000111110000111110001001110101111100010111011101011000001001001011110010000111010100101111100100101010000000011100000001000001110000110101011111101001011000001111110110001100011101100011010100010010111101101110101001101100001011010000110101011110110001000100111010011100101110010010100000010110011111101000011010011101111011101111101000101000001001001111100100001000100100101010110101100101001101111000011100110100100100001110101011111000001001100111010111111011000000100101011011011101010110111011101010111010010100010010100110010011111110000110001111000001010001111001001010000101100011101011111001111000010011010000010000100101101101011001101101000101111001111001000100011010110110111001101100110100000110000011101001010000000100110101111001110111110111010001000010000101001000110001100101110110111010110101111101000011011011000001111011000011011010000001010
    0110111000101001011110100111100101011000110111011000011010001001100110111001001000001110110010111110000001100100101110111101111010010100111010011000010110110000101101000010001001110111000001000001001001011010001100100001111010001000110000101001110101000100110011100011111101010000010011111010101011001111010101011110110011000100101110110100110010000110101101010101001001110100010011111001100000001001110110100111111110100000110100010010111100001101001000010011110000101001010111011101101111110000101100100001010010001101100111111001000000100010100111000111010101100010111100101000111000000001100100100001000000010110001001111011001101110011011000100101101110111001001011101101101110010001000011111110011111011101001001000000010010111001101110011111001110111101101101101001001111000110000101011100100101101010000011010101111011101101011011110011100101010100011010010011010001100101100111001010011101110111010111110101000101000111010110100011111111010111011011011111010100000110101111011110000110111001

***Output 5***

    01010101010101010101
    101010101010101010101010101010101010101010101010101010101010101010101010101010101010101010
    KHALI
    0101
    0101010101010101
    101010101010101010101010101010101010101010101010101010101010
    010101010101010101010101010101010101010101
    010101010101010101010101010101010101010101010101
    1010101010101010101010101010101010
    0101010101010101010101010101010101

<hr/>

**Example Snippet (Python)**

```python
t=int(input())
for i in range(t):
    s=str(input())
    while('00' in s or '11' in s):
        if '00' in s:
            s=s.replace('00','')
        if '11' in s:
            s=s.replace('11','')
 
 
    if s=='':
        print('KHALI')
    else:
        print(s)
```

<hr/>

> ## VQ2 Balanced Brackets

**Problem Statement**

A bracket is considered to be any one of the following characters: '(' , ')' , '{' , '}' , '[' , or ']'.

Given n strings of brackets, determine whether each sequence of 
brackets is balanced. If a string is balanced, return YES. Otherwise, return NO.

**Explanation**

- Two brackets are considered to be a matched pair if the an opening bracket (i.e., (, [, or {) occurs to the left of a closing bracket (i.e., ), ], or }) of the exact same type. There are three types of matched pairs of brackets: [], {},and ().
- A matching pair of brackets is not balanced if the set of brackets it encloses are not matched. For example, {[(])} is not balanced because the contents in between { and } are not balanced. The pair of square brackets encloses a single, unbalanced opening bracket, (, and the pair of parentheses encloses a single, unbalanced closing square bracket, ].
- By this logic, we say a sequence of brackets is balanced if the following conditions are met:
- It contains no unmatched brackets.
- The subset of brackets enclosed within the confines of a matched pair of brackets is also a matched pair of brackets.

**Input Description**  

    The first line contains a single integer n, the number of strings. 
    Each of the next n lines contains a single string s, a sequence of brackets.

**Output Description**  

    For each string, return YES or NO.

**Constraints:**  

    1<=n<=10^3
    1<=|s|<=10^3, where  is the length of the sequence.
    All chracters in the sequences ? { {, }, (, ), [, ] }.

**Time Limit:**

    Time Limit: 10000

**Sample Input**

    3
    {[()]}
    {[(])}
    {{[[(())]]}}

**Sample Output**

    YES
    NO
    YES

<hr/>

**Test Case 1**

***Input 1***

    5
    []{}()([{}])
    )[[[})(])({][(}][)]((})[}([)({[(){(([(}]})(](]}}]}](}]}}})}([[()])[[{})[][](]()}{{}({)}((]}){{)([{([({)]{{()]{){[[)(}}(()[}}{(}{}]{}()(})))(((())}([][)][}[({)[[}))){[[(()({)}]{]([}]({]{{{{[]{}{{){]][]{)[{(]}{(]}]]{[}[]}}](}}}{{){][(](}[])}[){{(]}[]{{{)}}{]{]}}[(]{)[)]{)({}]}){[[])]]][[)[[[([(}((((]}]]()({{)[((]{[[](]}]((}})[()(][{[)[[}[{[}[]]])}([}]}](]{}]]}())])]){])[(}()[{()(())([])(}]]{(}{[]})}(][)}({[)(]{)]})}({)}(]{[[]})[}[[([(})][(})}}{])(]}[][)))]][}]{)[))]))(}[}{({
    [{)](}]{{()({(}([{]}[{]{[[{][}{{[]{[{((]{[[]){)}{()[])({[](}][{]{})]{{[])]{([]}{{){])([}}{)[)}{}{()([)])[[)}}}]{}{([]{{}()[()()(][[[{])}])[}(}){{){](}]([){[){{{[{[)]}]}{[){[{]{]{][))[]}}[[(({[{[}[)[)[}][[)[[][]{]]{}]])}{{[{}({()(()}{(][[[})[[{()}(){)})[[([)]}}]}}((}){{]}}[}][(})))])}}})]})]}]}{}}}{[(][)(][()}([[((){{)}[()[})}[))[)[[])[]{{)])((([[[]]}){{[((()){[]])}))]}()(]}}{{()})[}{{([}{[)}{(}{}}{(){{{[{){)([[([[{]}]]})]}([][{{[)))]]}{[[[(])})(]}}[{{}[[){][]){))]][}])[)[[(({{[]]}[{{)))}(]}}{}((]){)({{[())[{]()}(])(}{}[}]()[]]{}(]}){((}{)}{({(]}({]][[{]{})[{(((}}))}}}[}]{)]](}))}){((]}))]}]}(}}])][){}{{}}])()(}[)([(]([[((]{]{]))){{})]([({()][{}[)((}))]({(}{{]])([}[))})]){[[))}[](}[](]](){](](({{])([}}][}[{)}{{[}](}[}{}}}}{{)](}[)]
    ]][](]}[{[}][)(]{)})]][([[)[}{}({[}](}())[}({)(}[]([}[)}([){(})])[}(){}{{(}{}){[[(]](})){][]))]]}[[]}{[}({]]{
    ({})(})[((]){]{}][[([]{{[[(){[)]]}})[}}}[{}][[{{{)[)(([}{}[{[({][([[])}}]])][(}](}}}{[({(]}]}{{{][{(()[](])(){[{){{}]]}{{{((]][[)[]}(}[([(](]{[(]]{((}[[)){)({(]{()}{]{([)[{)[}[))]]{{{){[]})(}[(}(]{})}][[([)]}]{{[(]())})]])[[](]}}(}][[(}}(()}())]}}])[{){)})}]}{]}[([}}{}{}][)}[]{{[)])([)}{([[{}[[}((]}]}[}[)][{)){[[[{]))]({))[][)[]{){))]{{})}{{{][{]]]{][})}{](]]])()]){(])[])}[()][(}({{{})(]{(}}{{}{)}}}[{]}}])}[[)[]]))()][))]}()[)({[(}{(){]])]]()}())])])]({][[{)([)){({{(}{([)[]())({}[({]}]]}[)[[){[}))(}{)(([))}){{})]}}({{(](]}(({}({}[(]][[{[]))({([}}({({{({)}{]}}){)])){[{}}))(}(){({}]}]{}[[[{})}{)[}{(}()})}{}]}[()(}}}}}[)[([([[]()(}]}[)}(}([][{][[[({[])(}{]{)}({]](([)()[){[]][[](]}[(})[}}]}}(){({(]{{)[))[}[[{]]((()[]](]}}})){))}([}(


***Output 1***

    YES
    NO
    NO
    NO
    NO    

<hr/>

**Test Case 2**

***Input 2***

    5
    [))(}){}([}}}))}}]]}}[[{(]}[}])((}}[[))[)((]{]}]][}[[)})((){{{[{{[])[([}))[)({((({{]])([{(]{]()[)}[](})(()([}}}[[[]{(]{({[)([}}[}}[}[[[))(({}]{{[(}}}{[{}[{](})]]{{{]{(]][)({([)]([{})((}]]]}[}([][}()]]]{}[((({][})}[)]{(})[}{)(]{[[}][)(][]]}[[]])])[}}{)[}]{}}[[}{}})[]]]]]))}[(}](}{{}({}{]}]]{][(([][{{{{([}({)]}}{{[{))[){[]]}){]}}[{{)([){))([[)}]]](}}}{]}][[][)}]}}{){}[)]))}]{()){[}()}[)[][{)({]]}[}]}{]{{[]{{()}[)(()[({{[}{}}[(}[)))({}{}(}({(}([)][})}{{}(})[))])]](}}((}]}}}}[}[]]])[}({{])[)}})(][)[[]][}[[[(([([]}]]}{)[[][
    ]][()([}}()])([{[][})[)])[{{[(}]){[][{(]}{({]]]]][)[)]({]{))[}[)})(][[[{]}}[{][)]{]){)([({{})}[({}[){({)}}({{))}[}}{{{)][}]]}]]})][][[)]}{[)](([{]][[)({]}}})))]})]}({{){([]}}][}{[[])((}{))[{]))(][}]{)(}}}}}{(][[)[])(((}{[)}}(}[{[([[{{[[)]}(]{[(](]](][)[)]}}]]]{({((}]})][(}[(}){)}}}({(]}[))])]]({}{}}()[){)({[{[(({]{)}}{{])))){[(({)}{}}][{]}(}[{]({[({{(]({({]({{]]{[[[[[]){){{[(){]}(())]]}{][}{)[({}){{]}}]{])}][}}[(((((][][[[][{)}(([])((]{])[{[}[({}]}({[[[}[({)]]}))[}(})){}[[]]})}{[{[)(][])}}([}][)(][){([[})}{(]}[}{()[
    (()(](()([)[}{){}{{([}{](([]{({(}}))(]{][([}{(([]{())[]]{][}[[)))]]]]})]}([[{)){[([]()]}{{()(}[[}])}((][{]))]]}}})[}{]{]}((][}{{]{)))}())]])}[(]]{[)))][{([)]]}][][{}{)}[}}{)}]({[({({(({{]()[]){){]{(]((][]}]]][{][}}[]))][[}{])()}}}}{()][}})[{[}[({{)})]{}{[}]([[{(]{([{)[[[]{}[)[({[][})](]{]{{{{}{]}[[{{())]}{]]}}]{[]])[{}[{){}(]{})]][({]({]}[}])[[]]]]))])}{()[)}{)][)]]}[](}{[}]{{{{][{[}))}({]}{}](}[](}}[})){}}](])))((]{{]{{]}]]{}()]})[}))]}[)]){}}}[}[)[]})]{[(][)(){)}))({(){{(}{]([]}({){{(][{[)][({(]{)}[]}(])}[[[([{{){{[[((())(}[[](}])]}])})))}[{[()})[]}}]}{}]]]]](])(([)}(})}{]({}({)]}))((())({{(}(]]][{)))[}([}}}]){])(}({{[}[}})(}
    [)[}[]{(())][{}[}[{){[}](}}{}[))]([{{[}}}}[{){))){){)[{[([{({[{]{{[)[(][{{[{}]{[([}(][](])({[}{(](}(})}}(()}}){}{)((]}))(]}})()[[}](()[}(((][({[])][({[{{[)}))])[})}}(({(}){)[((){](]}{]}]}[[[)}})}])[{[{{}[]{)})()]}[}[][}}]])){{)})[{({[}))((){)(]({{(]({]][()}[))}{})))[}]{]))]{(]}}[})(}{}]][}[{]}{]([][]}(}{]}])](}])}{{]{)}[[[]][[(}[{]]{}{({{]})]{))[)}]]{}([((({](]{{{)((]]][)({}({](}(}([}]))[[}]{){)[]{{([])]]}})[[[(((}(])]{[){[)))]][[)(()}})}[({){{]{{)){]}(){}[[}([[({}}{{)[)(([[(}{({(][)[{]}[)[}))]]}]{)][}))(()}{]([()[){[)])))]]({()[((}[}}{][)][}[])](}]]()]])(}}{{[]}}([{})[]]}}]{(}}])]{]]]]{){})}{({{{](({){]]({]){{[(}}[[(})}])]}{}{[])[}[([)([]}){{)[}}[])()}(([[{(})((}}]]{])(])]{]}]]{[((({)){{[](][)](({[}(}}{(([}[[{}}))]({))[}{{({[{]
    ()[})([][())[}]{[)({()[(}{)[}}[[{[]({{)()(){)]{{}{](()[]]{[))))[}[)[(]{}({{[{{[]([[(][{{){{)[}([)(}({{)([]){}})[{(){}]})]}][]){{}{[[)]}[((][{)](}(]{}}]}]({]}]))])[)[}[()]{([){[{}[(}]({){}{({(})({{))([]]]]}])])(([[((][(][}){(}{}(}(}[[(]]({{[}())]]){}(}){()[()(}[)}){(}[[{[{}]{[[}{])}]][{}}[])(})]][)]}({}([({[}[))[]({({[[[)}}){]}[}{))}{[(}[}]]}}](](){(}{[]}[)[)}(})]]}[(}])}[({)[](}]([)][}[)())[[[}})}({)[}}(){](}}([)[((}]))]([}{)(}{{)][{[}}({(){{[()]]({({[)(]{)(({}((}]{}[}){[][{([}[((]})]]([]{][({]}}({[[][{}{){}{[{][({({))()}{[}[))[{()}][}]{{{)){{()[}}})(}(])(({]}({()((]])}))[)}]()}()[}]]}}()[{{{()])[[[{


***Output 2***

    NO
    NO
    NO
    NO
    NO

<hr/>

**Test Case 3**

***Input 3***

    5
    })})]({{)[}((()[[[[)]{[}}]()[{]]([((][{[}]([[(()[]]})){[)(}{}}{)}](]]{}}(({}){([)()}[}[[}[]}{}}](][)[{(]]}){{]){(]]{(]{}](){]][({([(}[)))]{}]()))[[}}]([)](([(}(](({[]]([}))([{))]))({)}]({}(({(}){]})([([](}}){)[[}[[(({)}[({]]{)][){[}}{[){])))()])]{){[)){)[][[])))[{)(())]][}}[[{(((]]][]}(}(}}{}}[))[)([([)(}{[)[](])]}{(][{((({{}{{)[)}{(){}{){{][)(()}[){]]})})({[](]])[]])[{((]{[}((]]]{{({)][))[)))[]))}{)[}({})(([(]]]))([}}}))}()]}(}](}{[)()](]){()}(}]]]}(]]({][{}))({{}{}}((({))([{{]]{(])]{([]]{{}))}{{][]])[)[{([(([){[({(){)[[)){[)})(])[})(()(]{{{)))){}}{{({[[[}]]){}([])}[[]{{[{(){)(]})}[{]}))){]}[([(([[)}]][}[{)(}(]})({]{((}}[{])({[}}{}{[)}][}}[})({}[)])){}{]}[{}][(({))}]}(){{[}(}(]]]()[]}[]({}}[[)){)}{([}]][}[)){]))({[{[[)}()(}){})[}[[})()[][{((]}[[()({({([[](}})[()}])[([][]}[[(][[}[){(])(}]({)(){}{)]}{{}{)]{][)}}[[{{{{(([][}([{({))]{})]{[{{})}]}})[[{}(())]}]}(}{]{([))](]][[]([}{
    ]{[]}}](][[)(({)][{]]}[({)[(}(}[{{{{}[)}(()[)({}[]{]])})}}))[)]}()(()({[{{]{(]()[(]}([{)[[}}{)[})]]]]({[[){[{{}}[}[{))[(({][]}}{][)((]]}[()[}[{)({(}}))][())]([(}[[{{])(]]{}({({(}[(({{}{[]{}[([{([{]])[](}{}]]}[}]}){}]{){]}}{[}{}[(]][{({[}[)}[}]([{[{{[))[])}]}{})])[]{({}])([{{([])[([()}})))])]{}[)[([[[[]{}]]]((][(}
    [({(}[}{{}(]{}{]{{({[)(}{]}{{(){]}}{{(([[}{[{]})))}(}{]))[(([})(()[){)([][){}{(}[]()(])}()(](}[[[(}}{][{{][}{)(][]{[]]{{({]}[[](}()({{{}(}{)][}])({{(}((){}[{]}}(]}])}[(]](}{{(([[][(}[{}(]}}{]({])}[{])({][]}[(])]([[{(([]}(}{)]{{}}{{}{(([]]()()(]{[([)]]](}]}]{]])])[){}}{[({){}{(}()[{))){{){)){[[}((][[({)[]}((]]{{(][)}){]]))(}]}{(){]((}}}((}[)]{{{])[[]({)[{({({)}[{[{)[}[}((}[}[()]{[[]{]})[[([]}[){]{))}[}{{[{)[))([{()({}}}[((]()}[)}[](]]]([[][[{}[{{{}}([}))){(()}){{)(([}][{[])}][{)]{)([({)[}([][)[(](])}[[[(})((
    [((})(}}))([]())][[((}})]({)}{(](}]({[}[[({[[]}{[})[(][})[[[{}}]}]{]]({}))]}{])}[]]]]}}[))][(}{]((])]){((()]{[(}[]})()]}({)[[(]}{])(){)){)}]})}}[[}(({[{[{}[{{}]{]}){[)}]([)[]{))}}{{}{][[()}}[]][{)(}}()}}{{})]]][[)}]}}})([})}]])[][((]((){()(][)}(}}}}{]([)])([[][{[]]}]))){}[](][{(}](])]({(}){{}[]{)]}]){[{}[}(}][())[}[(][]}]}({]({]){{{({})){[]]][[]{[{)}]}][]]}{()){}{)]}}]))([[((}}}()()[[)({)]()){}]})({})({[][][{}{}})}{{()[[({({)[(}}{](]()}(][()[()){[}{{[([)([})]]{)}[)]({][}]]()}([}{)]][((}()(){{){{(}{{([]{})){}]}[]([[(}[}){[][{{[([]}{[}))(}{([(]{{{[)[{]])[}[{}}[{{}{][))[(][)]{}]{(}(]})[(}[({)(]{([([{{{(]()(}}]}][])]{([(({]{]([[{[}{(]){(}{[{(}}]}{[{[}(]{[{}}))(]}(})][]{}}]({}{}}}[)][){(]{)[]{(}{([[{)}
    {]]]){]}(]([{}[()}[{]})({}]}){[[({][)])}}[{{[)()]]


***Output 3***

    NO
    NO
    NO
    NO
    NO
    

<hr/>

**Test Case 4**

***Input 4***

    5
    }][(}}}{(]))([{[((({[))})]{}{[[{)}{(){))){[)](])))]{[(}(]((]}[}}]({[]](][(]}()]{}(]})[({{(}(}[)({))})[])))[][))([([[[[{[)[){{([{)[})]{((({]]{){{{{[{})[{])}])])}]{){]{{{(])[)]]]})()}}(]{({[][}[)[[]]{})[})]][})({]][{(})(}[(([{)((]]{]}({(]{((](]{()[}}[}]})}({{}])[}[){[{})[[{]}]}(]))(}])}}{([(}])(](]}{[{{)}))](}}[}([{{}{{(()[{(][{}){((({]{[[({([][[][]]()[)}])]}}}][))}){]})][)[[[}][][}{{][]])(}{[]))}{[{[}]({[]{}]}}}{]]}})(]]]({]{[{{}(]]{(({]][[{]))]])([(]][})]}()({[])}({{({}]([){[][)]}}][[]](}}[]){}]{
    )})}))}()({[}((][[)((](]}{)}}((}[])(([[([)}}}}{[}}}(](]([()](()}({(](()(]([{(][])]{)][)())[(((}(()[)[)])[)}({(}{[])]()[({{){)){(}[[](}({)}){((){}(){))[{{{()(][){([)]}(][[]](}))}{[}{]()]]{}])(}(())})({}[{{]}}]]{))([[[{{]({(}{(](]}](([}()]}([]}}]{}({{]{]{{))((]][(()({)(}(){({[)({))[[({{))[[)}{](][[{[{{{}}[{}})}}{)){{}}[)]]]{])[[{)][{)){)([}]}[[{]{)]][]{[){({](]})(([()((}}}})(((]}[)[)(][}([}}[(]))[[]{{(}[[)([}[(((}{[)](}){}([)[{[)]]{[)({({(()[}([{]{(}]))][})){[{{]])})[{)()}(}(}()([}))}}]]){)})[}[(}]({(][]}](]]{{[[[}]{]]{}}}{][]{([){([[]][)[}[]}{(])]}})}{))}])[}[[(({(]])}))[[((}{(})]()(((}[)[[[[(](((](((}]({)][{][}[[}}{{[([}}[{}(]}}(}}({[[[](})}){[[}{[
    {){(())(][}[({]((]{}}{](}[}}}){){]}{[}[))[()]{}])][)))((}[())[)}(][(([[[])()]]}}]{((([()[[[((){))}{[])]]]}{)[}(()(}(][[()
    )[}([]})}((]{]()((])]]])[{])[}{])})([[}]({](([]())[{[(()[}[[((]((]())})]([[[((()}(((}])({]((}}{(][)({]]}}{[{(]{[)}]]{(}[](([[()}}{{[[][]{[))}(}})([(]]})[}[)]}((]
    {{}}){][][){{}{)}()[[{(}])[({(])[}{{}{[[){[([}[](){}](()})()}{])[)){]{})(}}})]({]][)(}]])){{]))[[)}}}}}({)[(({{)}])[{[})](]]]{}{[})[()]{}[()][)[}]}()})[)])()})))(){{({)[]]}[]})}(({{{){](](}[[]}{]][[([[]]{}]{][[{})][({[])}]{(}](({)[([[{}(}[)[([}]))}}({({}[)}]])[]}])]{]})))]{]]}[(]{[])}({)({}[]()({{(}[[)[()()])]()}()[{)[}}]({)(())]{()}{[([)(})]][()()]]]{)]()[[][({{({{{][{)}}((}({[({})}{))()(}{{}{{}[((]]])}}])}[}}{{(((})([{[]][]{)[}{]{)([}[(}}[(){}}((]{{}]}(}({)[)([))(}]{])}){[)({)]()]{(((({{)][)[{])}[[}]})}]]((})[])([](()(})({])}{(]}[[)[))}][][}}{)]}((([]{})}(}{[}[)]]]}[(}[[{)})))}(([]))([)][]){)]{)}[[)}][{))][[{}[})][{{{{]}}})(]][[[}[](]){[(}

***Output 4***

    NO
    NO
    NO
    NO
    NO
    
<hr/>

**Test Case 5**

***Input 5***

    5
    [[{[})[((]]({}[{)){(]})[]}}{)](]]]{}))[){{}}[)({[)}[[]{)([)]])((()]{)[][]}[)([{}())(]({{{{([)(}}(}}][{](]]([[({({))}]{}}}[])({}{}[[(]{([]})(}{)(}[{({()]](]})}[][]])](}{}[{){)}{)[[}]{[[})))([[[}}{)[((}]{]({{})(}}[([(({[()){)})]))))])[]}}}][{}]){}](){(}[})[[(})]([)]{)[]{{])]}}]}[}]]([[[{}]){]([([([{[(([]]{[}(]){][))(}}]]){]}}[{[])}}{)}({)(]{})[{)[}]()(}}))]{()]()[}[{(}]])}{)]{]{))()([(]))}((][{{[)}(]}]([[]}({][{)]}{())({}{]{)((]()}}))}}[]{)][[[[}}](]({{[{([[}[([})}){]((((}({)()[}}[[)}{))({[}({}){})[][]{[[{)]}{[][)}]{))}((](]]()(((]([]}}]){}){][)}}([))[]}]][]]]((](({{}))((([{}(]{])[}[})[]((}[[[{{}{)}({[{[)({})))({}[{})(])}]])({}}[()
    [{]{}{]{)({((({[{]])][[]{}[{[){}]]}[((}[}{)})(}{([[)[]}(([(({({({[}]}){]}]{][{{([([{]{((]]]]{]({]{[][}[}[{}([]){)(])[))({{){{((){{}({]]{]]){{[}({[)]][[(([}{[}{}][}][{]{)]]{(]}](}][)}}((}(}}}[}[{[)[{}]]}})){{)](({{][])])}})(]][{([(}(]}{{(])[(])[{{)[[}{})}({{{])(]){))((}}({]}[)[(}[))}{{({)]]][[}}][{}}])({)]){){}{[}{[[]]]}{[({)}}())((]])({})){[{[[}}]
    (]{{(]}}][{}(()]}(}{[{[)[({[[(}]]{}({{)[[])[)[{[[}][(}}([[]([]{[))}(][)]([)())([((]{[)]{)}}}()(){))[{)[{)]}[][[}}][[[[{)[(]]}{[})((}{]]]][[[{}}[]}{{[][}{[[][)]}[)){{)]])}}(([{){}]
    }{(([]]}}]()]{){)[{{){}{]}]})[{[{]}{([}){}{{)[)]]{[[{}([[([(]{([}{]]][){[()][[)[{)]]]}]}}{{{(}}]]{]]]}}}(]][}]]{}}[()}[]]{][{{)[}[()))[})[[]}(({))[[]{]{[]][[())}[(}}]({(}[}}[[({)]{}}]]]]{({)[{])(())[)({){[{}[}([[(((]][)])[])][)]])))){((]}}}][{(}[(]([{)[[}[{}]}(}}}(()[)(]])()}]]]{)])[{({}])]({[}[[[}[({))(})[{))({)(]}[{{)})(){))(}{([}([][([{[[{((}){{]](([){][[}][{[{{(([[{){(]{(]{[)([)](]]{{]([){{})])}}}{({[[)[{){)]](]{}](}({})]){]]})}}[([}})}))[((}{)){{[}}}[[){((}(}((}}[)[]}}[()]}}([}[])(]][]([[][{(](})]}){(]}[]){){[}][}({)[[[][{[}]}}}[{([}{{{)))}{){}(}[[[[]][]]]({{}({}([)()[[[})]{(}}(]]}([][()((][(()[({{]{]]}([{){)])()[)}}(}{{{{)]]])[))){(})[{[({{{]))[[{)(([){}{(}[(})}}}(}([({({}{{(](]]))]]])([]))[}{}}}])[}{}}))()(])]](]}
    [){{](([{)))(}{{[({)]{)[[}[[{{{[[[]}}{((}()}[}(}{[]()(}}[({([})()}(][}[())([}{]({)(}{({{]})]{][[[[)[[(([]}]])[{((){(}{][(}[(([)][)((])([]{]{)({{{((]}{}))][{


***Output 5***

    NO
    NO
    NO
    NO
    NO    

<hr/>

**Example Snippet (Python)**

```python
def is_matched(expression):
    stack = []
    for bracket in expression:
        if bracket == ')':
            if len(stack) == 0 or stack.pop() != '(':
                return False
        elif bracket == '}':
            if len(stack) == 0 or stack.pop() != '{':
                return False
        elif bracket == ']':
            if len(stack) == 0 or stack.pop() != '[':
                return False
        else:
            stack.append(bracket)
    return len(stack)==0
 
t = int(input().strip())
for a0 in range(t):
    expression = input().strip()
    if is_matched(expression) == True:
        print("YES")
    else:
        print("NO")
```

<hr/>

> ## VQ3 Minimum Add to Make Parentheses Valid

**Problem Statement**

Given a string S of '(' and ')' parentheses, we add the minimum number of parentheses ( '(' or ')', and in any positions ) so that the resulting parentheses string is valid.

Given a parentheses string, return the minimum number of parentheses we must add to make the resulting string valid.

**Explanation**

Formally, a parentheses string is valid if and only if:

- It is the empty string, or
- It can be written as AB (A concatenated with B), where A and B are valid strings, or
- It can be written as (A), where A is a valid string.

**Input Description**  

    The Input Consists of an single line contains a String S

**Output Description**  

    The Output Should contains the integer N that specifies the minimum number of brackets can be added to balance the brackets

**Constraints:**  

    1 <= LENGTH(S) <= 1000000

**Time Limit:**

    Time Limit: 10000

**Sample Input**

    ()))((

**Sample Output**

    4

<hr/>

**Test Case 1**

***Input 1***

    ()()(((()(((())()(()()(()()(())())()(()()(()(()(()())(((()(((()((())()((()()())))))))))(())

***Output 1***

    9

<hr/>

**Test Case 2**

***Input 2***

    )(()())()()()(()())(((()()))((((()(())(((()())((()()(())()((((())(())((())(())()()))))()(()

***Output 2***

    11

<hr/>

**Test Case 3**

***Input 3***

    ((((()((((()((()())))))(())((((()()))()(((())()((()())))(((((()((()))))))(()(()))()(()()()(

***Output 3***

    11    

<hr/>

**Test Case 4**

***Input 4***

    ())()(((()()()((())()))(()))()()())))))()()()(((((()())))))))()(((())(())))(())())(()))))))

***Output 4***

    13

<hr/>

**Test Case 5**

***Input 5***

    )))())()))((())))()()()))((((())(((((()()((())()(())((())())))))())((())((()((()()))((()())

***Output 5***

    17

<hr/>

**Example Snippet (Python)**

```python
from collections import deque
s=input()
q=deque()
for i in s:
    if q:
        #print("i= ",i,"q-1= ",q[-1])
        if i==')' and q[-1]=='(':
            q.pop()
        elif i =='}' and q[-1]=='{':
            q.pop()
        elif i==']' and q[-1]=='[':
            q.pop()
        else:
                q.append(i)
    else:
        q.append(i)
print(len(q))
```

<hr/>

> ## VQ4 Monk and Power of Time

**Problem Statement**

The Monk is trying to explain to its users that even a single unit of time can be extremely important and to demonstrate this particular fact he gives them a challenging task.

There are N processes to be completed by you, the chosen one, since you're Monk's favorite student. All the processes have a unique number assigned to them from 1 to N.

Now, you are given two things:

The calling order in which all the processes are called.
The ideal order in which all the processes should have been executed.
Now, let us demonstrate this by an example. Let's say that there are 3 processes, the calling order of the processes is: 3 - 2 - 1. The ideal order is: 1 - 3 - 2, i.e., process number 3 will only be executed after process number 1 has been completed; process number 2 will only be executed after process number 3 has been executed.

> Iteration #1: Since the ideal order has process #1 to be executed firstly, the calling ordered is changed, i.e., the first element has to be pushed to the last place. Changing the position of the element takes 1 unit of time. The new calling order is: 2 - 1 - 3. Time taken in step #1: 1.

> Iteration #2: Since the ideal order has process #1 to be executed firstly, the calling ordered has to be changed again, i.e., the first element has to be pushed to the last place. The new calling order is: 1 - 3 - 2. Time taken in step #2: 1.

> Iteration #3: Since the first element of the calling order is same as the ideal order, that process will be executed. And it will be thus popped out. Time taken in step #3: 1.

> Iteration #4: Since the new first element of the calling order is same as the ideal order, that process will be executed. Time taken in step #4: 1.

> Iteration #5: Since the last element of the calling order is same as the ideal order, that process will be executed. Time taken in step #5: 1.

Total time taken: 5 units.

PS: Executing a process takes 1 unit of time. Changing the position takes 1 unit of time.

**Input Description**  

    The first line a number N, denoting the number of processes. The second line contains the calling order of the processes. The third line contains the ideal order of the processes.

**Output Description**  

    Print the total time taken for the entire queue of processes to be executed.

**Constraints:**  

    1<=N<=100

**Time Limit:**

    Time Limit: 5000

**Sample Input**

    3
    3 2 1
    1 3 2

**Sample Output**

    5

<hr/>

**Test Case 1**

***Input 1***

    40
    5 29 12 16 25 36 18 37 27 32 34 40 20 3 1 24 26 19 33 9 6 22 8 13 15 21 28 7 11 2 31 39 14 38 4 17 30 35 10 23
    14 39 4 5 23 7 40 8 36 17 30 21 3 35 33 32 12 16 20 25 31 13 22 34 19 18 29 11 27 15 1 38 26 6 28 10 9 37 2 24

***Output 1***

    491

<hr/>

**Test Case 2**

***Input 2***

    30
    5 29 12 16 25 17 18 30 27 10 4 23 20 3 1 24 26 19 14 9 6 22 8 13 15 21 28 7 11 2
    17 20 6 18 21 5 22 24 28 7 23 3 27 19 10 30 15 25 12 16 2 1 11 9 4 8 29 14 13 26

***Output 2***

    226    

<hr/>

**Test Case 3**

***Input 3***

    5
    5 4 2 3 1
    5 2 1 4 3

***Output 3***

    7

<hr/>

**Test Case 4**

***Input 4***

    10
    5 4 8 9 1 6 3 2 7 10
    1 6 8 9 5 4 10 3 2 7

***Output 4***

    27

<hr/>

**Test Case 5**

***Input 5***

    15
    5 11 12 13 15 6 14 2 7 10 4 8 9 3 1
    4 15 8 2 6 9 11 10 7 5 13 14 3 1 12

***Output 5***

    75

<hr/>

**Example Snippet (Python)**

```python
n=int(input())
call=list(map(int,input().split()))
ideal=list(map(int,input().split()))
count=0
i=0
while(len(call)!=0):
    if(call[i]==ideal[i]):
        del call[i]
        del ideal[i]
        count+=1
    else:
        b= call.pop(i)
        call.append(b)
        count+=1  
print(count)
```

<hr/>


> ## VQ5 Disk tower

**Problem Statement**

Your task is to construct a tower in N days by following these conditions:

Every day you are provided with one disk of distinct size.
The disk with larger sizes should be placed at the bottom of the tower.
The disk with smaller sizes should be placed at the top of the tower.
The order in which tower must be constructed is as follows:

You cannot put a new disk on the top of the tower until all the larger disks that are given to you get placed.
Print N lines denoting the disk sizes that can be put on the tower on the i<sup>th</sup> day.

**Explanation**

- On the first day, the disk of size 4 is given. But you cannot put the disk on the bottom of the tower as a disk of size 5 is still remaining.

- On the second day, the disk of size 5 will be given so now disk of sizes 5 and 4 can be placed on the tower. 

- On the third and fourth day, disks cannot be placed on the tower as the disk of 3 needs to be given yet. Therefore, these lines are empty. 

- On the fifth day, all the disks of sizes 3, 2, and 1 can be placed on the top of the tower.

**Input Description**  

    First line: N denoting the total number of disks that are given to you in the N subsequent days
    Second line: N integers in which the i<sup>th</sup> integers denote the size of the disks that are given to you on the i<sup>th</sup> day

**Output Description**  

    Print N lines. In the i<sup>th</sup> line, print the size of disks that can be placed on the top of the tower in descending order of the disk sizes.
    If on the i<sup>th</sup> day no disks can be placed, then leave that line empty.

**Constraints:**  

    1<=N<=10<sup>6</sup>
    1<=size of disc<=N

**Time Limit:**

    Time Limit: 5000

**Sample Input**

    5
    4 5 1 2 3

**Sample Output**

    5 4
    
    
    3 2 1

<hr/>

**Test Case 1**

***Input 1***

    1
    1

***Output 1***

    1

<hr/>

**Test Case 2**

***Input 2***

    2
    1 2

***Output 2***

    2 1

<hr/>

**Test Case 3**

***Input 3***

    4
    3 2 1 4

***Output 3***

    4 3 2 1

<hr/>

**Test Case 4**

***Input 4***

    15
    11 7 14 3 9 4 12 2 5 1 15 13 10 8 6

***Output 4***

    15 14
    13 12 11
    10 9
    8 7
    6 5 4 3 2 1

<hr/>

**Test Case 5**

***Input 5***

    12
    3 4 10 12 9 1 2 7 11 8 6 5

***Output 5***

    12
    11 10 9
    8 7
    6
    5 4 3 2 1

<hr/>

**Example Snippet (Python)**

```python
def Solve (arr):
    # Write your code here
    stack = []
    mxn = len(arr)
    j = 0
    out = []
    d = {}
    
    for i in arr :
        d[i] = True
        s = ''
        if i == mxn:
            s += str(i) + ' '
            mxn -=1
            while (mxn in d):
                s += str(mxn) + ' '
                mxn -=1
            print(s)
        else:
            print(' ')
 
N = int(input())
arr = list(map(int, input().split()))
Solve(arr)
```

<hr/>

> ## VQ6 Hamiltonian and Lagrangian

**Problem Statement**

Students have become secret admirers of SEGP. They find the course exciting and the professors amusing. After a superb Mid Semester examination its now time for the results. The TAs have released the marks of students in the form of an array, where arr[i] represents the marks of the ith student.

Since you are a curious kid, you want to find all the marks that are not smaller than those on its right side in the array.

**Input Description**  

    The first line of input will contain a single integer n denoting the number of students.
    The next line will contain n space separated integers representing the marks of students.

**Output Description**  

    Output all the integers separated in the array from left to right that are not smaller than those on its right side.

**Constraints:**  

    1 <= n <= 1000000
    0 <= arr[i] <= 10000

**Time Limit:**

    Time Limit: 2000

**Sample Input**

    6
    16 17 4 3 5 2

**Sample Output**

    17 5 2

<hr/>

**Test Case 1**

***Input 1***

    5
    446 107 111 209 383

***Output 1***

    383

<hr/>

**Test Case 2**

***Input 2***

    8
    431 257 313 423 498 415 93 145

***Output 2***

    498 415 145

<hr/>

**Test Case 3**

***Input 3***

    4
    457 92 171 300

***Output 3***

    300

<hr/>

**Test Case 4**

***Input 4***

    8
    248 192 6 410 55 356 334 145

***Output 4***

    410 356 334 145

<hr/>

**Test Case 5**

***Input 5***

    3
    307 115 500

***Output 5***

    500

<hr/>

**Example Snippet (Python)**

```python
n=int(input())
arr=list(map(int,input().split(' ')))
max=arr[-1]
output=[arr[-1]]
for i in range(n-2,0,-1):
    if arr[i]>=max:
        output.append(arr[i])
        max=arr[i]
output=output[::-1]
for i in output:
    print(i, end=" ")
```

<hr/>


> ## VQ7 Possible Polygon

**Problem Statement**

> You are given length of n sides, you need to answer whether it is possible to make n sided convex polygon with it.
 

**Input Description**  

    First line contains T, no of testcases.
    For each test case , first line consist of single integer N,second line consist of N (l1,l2…ln) spaced integers, size of each side.

**Output Description**  

    For each test case print "Yes" if it is possible to make polygon or else "No" if it is not possible.

**Constraints:**  

    1≤T≤10
    1≤n≤10<sup>5</sup>
    1≤l<sub>i</sub>≤10<sup>4</sup>

**Time Limit:**

    Time Limit: 5000

**Sample Input**

    2
    3
    4 3 2 
    4
    1 2 1 4 

**Sample Output**

    Yes
    No

<hr/>

**Test Case 1**

***Input 1***

    2
    3
    2 3 4
    5
    1 2 3 4 5

***Output 1***

    Yes
    Yes    

<hr/>

**Test Case 2**

***Input 2***

    2
    2
    6 7
    1
    4

***Output 2***

    No
    No    

<hr/>

**Test Case 3**

***Input 3***

    1
    1
    9

***Output 3***

    No    

<hr/>

**Test Case 4**

***Input 4***

    3
    2
    89 45
    2
    76 4
    2
    23 45

***Output 4***

    No
    No
    No

<hr/>

**Test Case 5**

***Input 5***

    2
    4
    45 67 23 67
    3
    45 784 34    

***Output 5***

    Yes
    No    

<hr/>

**Example Snippet (Python)**

```python
t = int(input())
a=[]
while t:
    n = int(input())
    l = list(map(int, input().split()))
    sides_sum = sum(l)
    max_l = max(l)
    if sides_sum - max_l > max_l:
        a.append("Yes")
    else:
        a.append("No")
    t -= 1
print("\n".join(a))
```

<hr/>

