# ASC
Assembly operations

## Cerinta 1
Fie dat ca input un sir hexa, se cere sa se afiseze la standard output instructiunea assembly de
executat.
De exemplu, pentru inputul A78801C00A7890EC04, se va afisa la standard output x 1 let x -14 div.

## Cerinta 2
Fie dat ca input o instructiune in limbajul de asamblare al procesorului aritmetic considerat, se
cere sa se afiseze la standard output evaluarea instructiunii. Pentru aceasta cerinta, in instructiune
nu exista variabile, ea fiind formata doar din numere intregi si operatii.
De exemplu, poate fi data instructiunea 2 10 mul 5 div 7 6 sub add. Rezultatul trebuie sa
fie conform urmatorului algoritm:
• se adauga 2 pe stiva;
• se adauga 10 pe stiva;
• se identifica operatia mul, se aplica inmultirea dintre 2 si 10, se obtine 20, se elimina 2 si 10
de pe stiva si se pastreaza doar 20;
• se adauga 5 pe stiva;
• se identifica div - actioneaza ca 20 div 5, iar rezultatul este 4; se elimina 20 si 5 de pe stiva,
si se pastreaza doar 4;
• se adauga 7 pe stiva;
• se adauga 6 pe stiva;
• se identifica sub - se calculeaza diferenta dintre 7 si 6, se obtine 1, se elimina 7 si 6 de pe stiva,
si se adauga pe stiva valoarea 1. Atentie! in acest moment, pe stiva avem 4 (la baza) si 1 in
varf, intrucat sub este operatie binara si a lucrat doar cu argumentele 7 si 6, dar nu si cu 4
care era deja la baza stivei.
• se identifica add - se calculeaza suma dintre 1 si 4, se obtine 5, se elimina 1 si 4 de pe stiva, se
adauga 5;
• am terminat de parcurs sirul, iar rezultatul obtinut este, acum, situat in varful stivei. Rezultatul acestui calcul este 5.

## Cerinta 3
Fie dat ca input o instructiune in limbajul de asamblare al procesorului aritmetic considerat. Se
cere sa se afiseze la standard output evaluarea instructiunii. Pentru aceasta cerinta, spre deosebire
de cerinta 2, se folosesc variabile introduse prin let.
Un exemplu de input poate fi x 1 let 2 x add y 3 let x y add mul.
Evaluarea va fi facuta astfel:
• se adauga x si 1 pe stiva, este gasit let, si se intelege de acum ca x = 1 in toata expresia
aritmetica; sunt eliminati x si 1 de pe stiva;
• se adauga 2 si 1 pe stiva (deoarece acel x este = 1 de acum);
• se intalneste add, se calculeaza suma 3, se elimina 2 si 1 de pe stiva si se pastreaza doar 3;
• se adauga y si 3 pe stiva, este gasit let, si se intelege de acum ca y = 3 in toata expresia
aritmetica; sunt eliminati y si 3 de pe stiva;
• se adauga 1 si 3 pe stiva (x, respectiv y);
• se efectueaza adunarea, rezultatul va fi 4, se elimina 1 si 3 de pe stiva, se adauga 4;
• este identificat mul, iar pe stiva aveam deja 3 (de la a treia bulinuta din explicatia curenta) si
4, de la bulinuta anterioara, si se calculeaza rezultatul, 12, se elimina apoi 3 si 4 de pe stiva si
se adauga 12;
• nu mai sunt elemente in sir, deci rezultatul final este 12.
