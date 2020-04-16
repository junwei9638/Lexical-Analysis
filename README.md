# Lexical-Analysis
System Program Project1

開發平台: MacBook Pro (Retina, 13-inch, Early 2015)

開發環境 : MacOs Catalina 
	  
IDE : Xcode 11.1

程式語言 : C++

組合語言 : x86

程式設計功能 :  
1.	能輸入所需table檔並建立database
2.	輸入input檔輸出output檔並能重複執行
3.	Table 1~3大小寫輸入無差別

程式設計流程 : 
1.	開table檔並建立database
2.	請使用者輸入檔名並且判斷有無此檔，有則開檔進入InputAndAnalyze();
3.	使用getline輸入一整行再進行切割
4.	如果字元是delimiter的話，直接丟進whichtype判斷是哪一個token，並且直接output，不是delimiter的字元先丟到暫存字元的vector CutLetter
5.	如果碰到空白或是delimiter的時候，會把CutLetter裡面的東西變成字串，丟到whichtype判斷是哪一個token，並且直接output
6.	whichtype是判斷table 1~4，如果不是就先判斷是不是string，是的話進入StringProcess，再判斷是不是integer，是的話進入IntProcess，再不是就進入         
    SymbolProcess
7.	最後碰到EOF時把再把最後CutLetter的token進行判斷並output

