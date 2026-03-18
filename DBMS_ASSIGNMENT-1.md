**1.DEPOSIT TABLE**

QUERY:

CREATE TABLE DEPOSIT(ACTNO VARCHAR(5),CNAME VARCHAR(15),BNAME VARCHAR(15),AMOUNT NUMBER(9,2),ADATE DATE);



OUTPUT:

TABLE CREATED.



QUERY:

DESC DEPOSIT;



OUTPUT:

Name                                      Null?    Type

&nbsp;----------------------------------------- -------- ----------------------------

&nbsp;ACTNO                                              VARCHAR2(5)

&nbsp;CNAME                                              VARCHAR2(15)

&nbsp;BNAME                                              VARCHAR2(15)

&nbsp;AMOUNT                                             NUMBER(9,2)

&nbsp;ADATE                                              DATE



QUERY:

INSERT INTO DEPOSIT VALUES('\&ACTNO','\&CNAME','\&BNAME',\&AMOUNT,'\&ADATE');

Enter value for actno: 100

Enter value for cname: ANIL

Enter value for bname: VRCE

Enter value for amount: 1000

Enter value for adate: 01-MAR-95

old   1: INSERT INTO DEPOSIT VALUES('\&ACTNO','\&CNAME','\&BNAME',\&AMOUNT,'\&ADATE')

new   1: INSERT INTO DEPOSIT VALUES('100','ANIL','VRCE',1000,'01-MAR-95')



OUTPUT:

1 ROW CREATED.



QUERY:

SELECT \* FROM DEPOSIT;



OUTPUT:

ACTNO CNAME           BNAME               AMOUNT ADATE

----- --------------- --------------- ---------- ---------

100   ANIL            VRCE                  1000 01-MAR-95

101   SUNIL           AJNI                  5000 04-JAN-96

102   MEHUL           KAROLBAGH             3500 17-NOV-95

104   MADHURI         CHANDI                1200 17-DEC-95

105   PRAMOD          M G ROAD              3000 27-MAR-96

106   SANDIP          ANDHERI               2000 31-MAR-96

107   SHIVANI         VIRAR                 1000 05-SEP-95

108   KRANTI          NEHRU PALACE          5000 02-JUL-95

109   MINU            POWAI                 7000 10-AUG-95



9 rows selected.



**2.BRANCH TABLE**

QUERY:

CREATE TABLE BRANCH(BNAME VARCHAR(15),CITY VARCHAR(15));



OUTPUT:

Table created.



QUERY:

DESC BRANCH;



OUTPUT:

Name                                      Null?    Type

&nbsp;----------------------------------------- -------- ----------------------------

&nbsp;BNAME                                              VARCHAR2(15)

&nbsp;CITY                                               VARCHAR2(15)



QUERY:

&nbsp;INSERT INTO BRANCH VALUES('\&BNAME','\&CITY');

Enter value for bname: VRCE

Enter value for city: NAGPUR

old   1: INSERT INTO BRANCH VALUES('\&BNAME','\&CITY')

new   1: INSERT INTO BRANCH VALUES('VRCE','NAGPUR')



OUTPUT:

1 ROW CREATED.



QUERY:

SELECT \* FROM BRANCH;



OUTPUT:

BNAME           CITY

--------------- ---------------

VRCE            NAGPUR

AJNI            NAGPUR

KAROLBAGH       DELHI

CHANDI          DELHI

DHARAMPETH      NAGPUR

M G ROAD        BANGLORE

ANDHERI         BOMBAY

VIRAR           BOMBAY



**3. CUSTOMERS TABLE**

QUERY:

CREATE TABLE CUSTOMERS(CNAME VARCHAR(15),CITY VARCHAR(15));



OUTPUT:

Table created.



QUERY:

DESC CUSTOMERS;



OUTPUT:

Name                                      Null?    Type

&nbsp;----------------------------------------- -------- ----------------------------

&nbsp;CNAME                                              VARCHAR2(15)

&nbsp;CITY                                               VARCHAR2(15)



QUERY:

INSERT INTO CUSTOMERS VALUES('\&CNAME','\&CITY');

Enter value for cname: ANIL

Enter value for city: CALCUTTA

old   1: INSERT INTO CUSTOMERS VALUES('\&CNAME','\&CITY')

new   1: INSERT INTO CUSTOMERS VALUES('ANIL','CALCUTTA')



OUTPUT:
1 ROW CREATED.



QUERY:

SELECT \* FROM CUSTOMERS;



OUTPUT:

CNAME           CITY

--------------- ---------------

ANIL            CALCUTTA

SUNIL           DELHI

MEHUL           BARODA

MANDAR          PATNA

MADHURI         NAGPUR

PRAMOD          NAGPUR

SANDIP          SURAT

SHIVANI         BOMDAY



8 rows selected.



**4.BORROW TABLE**

QUERY:

&nbsp;CREATE TABLE BORROW(LOANNO VARCHAR(5),CNAME VARCHAR(15),BNAME VARCHAR(15),AMOUNT NUMBER(9,2));



OUTPUT:

Table created.



QUERY:

DESC BORROW;



OUTPUT:
Name                                      Null?    Type

&nbsp;----------------------------------------- -------- ----------------------------

&nbsp;LOANNO                                             VARCHAR2(5)

&nbsp;CNAME                                              VARCHAR2(15)

&nbsp;BNAME                                              VARCHAR2(15)

&nbsp;AMOUNT                                             NUMBER(9,2)



QUERY:
INSERT INTO BORROW VALUES('\&LOANNO','\&CNAME','\&BNAME',\&AMOUNT);

Enter value for loanno: 201

Enter value for cname: ANIL

Enter value for bname: VRCE

Enter value for amount: 1000

old   1: INSERT INTO BORROW VALUES('\&LOANNO','\&CNAME','\&BNAME',\&AMOUNT)

new   1: INSERT INTO BORROW VALUES('201','ANIL','VRCE',1000)



OUTPUT:

1 row created.



QUERY:

&nbsp;SELECT \* FROM BORROW;


OUTPUT:
LOANN CNAME           BNAME               AMOUNT

----- --------------- --------------- ----------

201   ANIL            VRCE                  1000

206   MEHUL           AJNI                  5000

311   SUNIL           DHARAMPETH            3000

321   MADHURI         ANDHERI               2000

375   PRMOD           VIRAR                 8000

481   KRANTI          NEHRU PALACE          3000

201   ANIL            VRCE                  1000

206   MEHUL           AJNI                  5000

311   SUNIL           DHARAMPETH            3000

321   MADHURI         ANDHERI               2000



10 rows selected.



**PERFORM THE QUERIES:-**

**1.DESCRIBE DEPOSIT,BRANCH TABLES.**

 **ANSWER-** DESC DEPOSIT;

&nbsp;Name                                      Null?    Type

&nbsp;----------------------------------------- -------- ----------------------------

&nbsp;ACTNO                                              VARCHAR2(5)

&nbsp;CNAME                                              VARCHAR2(15)

&nbsp;BNAME                                              VARCHAR2(15)

&nbsp;AMOUNT                                             NUMBER(9,2)

&nbsp;ADATE                                              DATE



  DESC BRANCH;

&nbsp;Name                                      Null?    Type

&nbsp;----------------------------------------- -------- ----------------------------

&nbsp;BNAME                                              VARCHAR2(15)

&nbsp;CITY                                               VARCHAR2(15)





**2.DESCRIBE BORROW,CUSTOMERS TABLE.**

**ANSWER-** DESC BORROW;

&nbsp;Name                                      Null?    Type

&nbsp;----------------------------------------- -------- ----------------------------

&nbsp;LOANNO                                             VARCHAR2(5)

&nbsp;CNAME                                              VARCHAR2(15)

&nbsp;BNAME                                              VARCHAR2(15)

&nbsp;AMOUNT                                             NUMBER(9,2)



&nbsp;DESC CUSTOMERS;

&nbsp;Name                                      Null?    Type

&nbsp;----------------------------------------- -------- ----------------------------

&nbsp;CNAME                                              VARCHAR2(15)

&nbsp;CITY                                               VARCHAR2(15)



**3.LIST ALL DATA FROM TABLE DEPOSIT.**

**ANSWER-**  SELECT \* FROM DEPOSIT;

ACTNO CNAME           BNAME               AMOUNT ADATE

----- --------------- --------------- ---------- ---------

100   ANIL            VRCE                  1000 01-MAR-95

101   SUNIL           AJNI                  5000 04-JAN-96

102   MEHUL           KAROLBAGH             3500 17-NOV-95

104   MADHURI         CHANDI                1200 17-DEC-95

105   PRAMOD          M G ROAD              3000 27-MAR-96

106   SANDIP          ANDHERI               2000 31-MAR-96

107   SHIVANI         VIRAR                 1000 05-SEP-95

108   KRANTI          NEHRU PALACE          5000 02-JUL-95

109   MINU            POWAI                 7000 10-AUG-95



9 rows selected.



**4.LIST ALL DATA FROM TABLE BORROW.**

**ANSWER-**  SELECT \* FROM BORROW;



LOANN CNAME           BNAME               AMOUNT

----- --------------- --------------- ----------

201   ANIL            VRCE                  1000

206   MEHUL           AJNI                  5000

311   SUNIL           DHARAMPETH            3000

321   MADHURI         ANDHERI               2000

375   PRMOD           VIRAR                 8000

481   KRANTI          NEHRU PALACE          3000

201   ANIL            VRCE                  1000

206   MEHUL           AJNI                  5000

311   SUNIL           DHARAMPETH            3000

321   MADHURI         ANDHERI               2000



10 rows selected.



**5.LIST ALL DATA FROM TABLE CUSTOMER.**

**ANSWER-** SELECT \* FROM CUSTOMERS;



CNAME           CITY

--------------- ---------------

ANIL            CALCUTTA

SUNIL           DELHI

MEHUL           BARODA

MANDAR          PATNA

MADHURI         NAGPUR

PRAMOD          NAGPUR

SANDIP          SURAT

SHIVANI         BOMDAY



8 rows selected



**6.LIST ALL DATA FROM TABLE BRANCH.**

**ANSWER-** SELECT \* FROM BRANCH;



BNAME           CITY

--------------- ---------------

VRCE            NAGPUR

AJNI            NAGPUR

KAROLBAGH       DELHI

CHANDI          DELHI

DHARAMPETH      NAGPUR

M G ROAD        BANGLORE

ANDHERI         BOMBAY

VIRAR           BOMBAY



8 rows selected.



**7.GIVE THE ACCOUNT NO AND AMOUNT OF DEPOSITORS.**

**ANSWER-** SELECT ACTNO,AMOUNT FROM DEPOSIT;



ACTNO     AMOUNT

----- ----------

100         1000

101         5000

102         3500

104         1200

105         3000

106         2000

107         1000

108         5000

109         7000



9 rows selected.



**8.GIVE NAME OF CUSTOMERS WHO OPENED ACCOUNT AFTER DATE '01-DEC-96'.**

**ANSWER-**  SELECT AMOUNT FROM DEPOSIT WHERE AMOUNT > 4000;



&nbsp;   AMOUNT

----------

&nbsp;     5000

&nbsp;     5000

&nbsp;     7000

**10.LIST ALL THE CUSTOMERS FROM BOMBAY CITY.**

**ANSWER-** no rows selected.













































