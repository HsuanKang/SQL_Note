# SQL_Note

datepart (dy(當年第幾天) / qq(季) / ww(週) / dw(星期-要減1) , @日期)</br>
datediff (dd / mm / yy , '開始日期', '結束日期') - 頭尾都算+1</br>
convert (datatype, @變數, 樣式)</br>
ISNULL (n1, y1)</br>
@@ROWCOUNT 筆數</br>
substring (@變數, 起, 個數)</br>
cast (@變數 as datatype)
having -> 加總後統計

<B>窗口函式</B></BR>
NTITLE( 組數 )  OVER ()</BR>
ROW_NUMBER()  OVER (PARTITION BY __ ORDER BY__)</BR>
LAG( 欄 , 前幾筆 )  OVER()</BR>
LEAD( 欄 , 後幾筆 )  OVER()</BR>
RANK() / DENSE_RANK()  OVER()</BR>
MAX() / MIN() / COUNT() / SUM() / AVG()   OVER() -----不可加 ORDER BY</BR>

# Tips

左連接右 (或相反) 的外側條件再 where 套用過濾 - 無法顯示</br>
對需要彙整或細節的查詢先在子查詢進行，再連接表單</br>
not exists > not in  (成本太高)</br>
<b>非關聯式子查詢</b>不依靠外層資料表查詢並能獨立執行 (通常放在 from 過濾後資料)</br>
<b>關聯式子查詢</b>用於回傳純亮值給 select、提供給 where、having、exists</br>
<a href="https://blog.xuite.net/f8789/DCLoveEP/30614743-SQL+-+%E4%BD%BF%E7%94%A8+%E4%B8%80%E8%88%AC%E8%B3%87%E6%96%99%E8%A1%A8%E9%81%8B%E7%AE%97%E5%BC%8F+CTE+%28Common+Table+Expression%29">CTE (資料表運算式)</a></br>
資料引擎先處理 FROM 在處理 WHERE
