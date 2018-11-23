# ParcialFinal

DECLARE 
  TYPE number_array IS VARRAY(50) OF INTEGER;
  vE number_array;
  suma number ;
  maxsuma number;
  valor number;
BEGIN
  vE := number_array(-2, -3, 4, -1, -2, 1, 5, -3);
  suma := vE(1);
  maxsuma := vE(1);
  FOR i IN 1..vE.COUNT LOOP
    suma := suma + vE(i);
    IF suma >= vE(i) THEN
       valor := suma;
    ELSE  
       valor := vE(i);
    END IF;
    IF valor >= maxsuma THEN
        maxsuma := valor;
    END IF;
  END LOOP;
  DBMS_OUTPUT.put_line('El max es'|| maxsuma); 
END;

CREATE TABLE PEDIDOS (
items integer,
cajas_grandes integer,
cajas_pequenas integer,
cantidad_cajas integer
)

