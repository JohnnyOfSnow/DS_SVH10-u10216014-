# DS_SVH10-u10216014-
DS_SVH10 = Data Structure Summer Vacation Homework for BFS(Breadth-first search) 廣度優先搜尋

一、程式說明
1.    目標：撰寫有向圖及無向圖之BFS
2.    修動態網頁設計者請用Javascript及Canvas撰寫，未修者請用Java applet。
3.    以鄰接矩陣表示Graph(以一維或二維array)，因此由user輸入時，亦用此方式，且1代表二個vertex連接，0代表不連接。
4.    須包含d[ ]，PI[ ]，Q等結構(在PI[ ]中-1代表nil)。
5.    畫面需要有：
            Run-all mode:一次完成所有內容及過程說明。
            Step mode:一次只完成一步驟，呈現該step之過程說明，且以白、綠、黑色變化。
            Quiz mode:要求user輸入d[ ],PI[ ]之內容，且由程式判斷對或錯，錯在何處？需有回饋。
            Clear all:清除所有輸入盒內容及變數恢復為內定初值。
6.  過程說明請搭配演算法:
    Algorithm:
        BFS(G,s)
          for each vertex u in V[G] - {s}
            do color[u] <- white
            d[u] <- infinity
            pi[u] <- NIL
          color[s] <- gray
          d[s] <- 0
          pi[s] <- NIL
          Q <- {s}
          While Q .ne.
            do u <- Head[Q]
              for each v in Adj[u]
                do uf color[v] = white
                  then color [v] <- gray
                    d[v] <- d[u] + 1
                    Pi[v] <- u
                    Enqueue(Q,v)
              Dequeue(Q)
              color[u] <- black
