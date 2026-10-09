
male(abraham).
male(clancy).
male(herb).
male(homer).
male(bart).

female(mona).
female(jackie).
female(marge).
female(patty).
female(selma).
female(lisa).
female(maggie).
female(ling).

parent(abraham,herb).
parent(abraham,homer).
parent(mona,homer).
parent(clancy,marge).
parent(jackie,marge).
parent(clancy,patty).
parent(jackie,patty).
parent(clancy,selma).
parent(jackie,selma).
parent(homer,bart).
parent(marge,bart).
parent(homer,lisa).
parent(marge,lisa).
parent(homer,maggie).
parent(marge,maggie).
parent(selma,ling).

%--------------------------------------------

father(X, Y) :-
    male(X),
    parent(X, Y).

mother(X,Y) :-
    female(X),
    parent(X,Y) .

brother(X,Y) :-
    male(X),
    parent(P,X),
    parent(P,Y),
    X \= Y.

sister(X,Y) :-
    female(X),
    parent(P,X),
    parent(P,Y),
    X \= Y.

daughter(X,Y) :-
    female(X),
    parent(Y,X).

son(X,Y) :-
    male(X),
    parent(Y,X).

sibling(X,Y) :-
    parent(P,X),
    parent(P,Y),
    X \= Y.

grandfather(X,Y) :-
    male(X),
    parent(X,P),
    parent(P,Y).

aunt(X,Y) :-
    female(X),
    sibling(X,P),
    parent(P,Y).

uncle(X,Y) :-
    male(X),
    sibling(X,P),
    parent(P,Y).

cousin(X,Y) :-
    parent(P1,X),
    parent(P2,Y),
    sibling(P1,P2).

ancestor(X,Y) :-
    parent(X,Y).

ancestor(X,Y) :-
    parent(X,Z),
    ancestor(Z,Y).










