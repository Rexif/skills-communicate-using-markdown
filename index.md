# NO Cap

This is my *attempt* to feel productive and not be distracted from my short term goals.

![image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

``` SQL
select 	distinct D.wID
from 	displays D
where 	exists
	 (select *
	  from graphic G 
	  where G.gType = 'jpg' and G.gID = D.gID) ;


gifGraphics := 
select 	distinct D.wID
from 	displays D
where exists
	(select *
	 from graphic G 
	 where G.gType = 'gif' and G.gID = D.gID) ;

sql4 :=
	select W.wID, W.wTitle
	from webpage W 
	where exists (select * from jpgGraphics J where J.wID = W.wID) and
	  not exists (select * from gifGraphics G where G.wID = W.wID);\
 
 ```
