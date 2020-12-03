proc sql;
	create table bla as select *, "A" as joiner from work.aufgabe1;
quit;

proc sql;
	create table bla2 as select * from bla;
quit;

proc sql;
	create table bla3 as select * from bla;
quit;

proc sql;
	create table bla4 as 
	select bla.F1 as Number1,
	bla2.F1 as Number2,
	bla3.F1 as Number3
	from bla full join bla2 on bla.joiner=bla2.joiner
	full join bla3 on bla.joiner=bla3.joiner;
quit;

proc sql;
	create table bla5 as
	select Number1 * Number2 * Number3
	from bla4
	where Number1 + Number2 + Number3 = 2020;
quit;
