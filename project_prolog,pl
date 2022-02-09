% starting points
% ending y-points
% size of th grid
% park goers
% created path

solve([SX,SY], EndY, [GX, GY], Locations, X) :-
   make([SX,SY],EndY, [GX, GY], Locations, [],X).

%base
make([_,SY], EndY,_,_,Path,X):-
     SY == EndY, append([],Path,X).

%recur
make([SX,SY], EndY,[GX, GY],Locations,Path,X):-
    SY \= EndY,
	move([SX,SY],[NX,NY]),
    safe(Locations,[NX,NY]),
	grid([GX,GY],[NX,NY]),
    not_member([NX,NY],Path),
    append(Path,[[NX,NY]],Newpath),
    make([NX,NY],EndY,[GX, GY],Locations,Newpath,X).

% not member
not_member(_, []) :- !.

not_member(X, [Head|Tail]) :-
     X \= Head,
    not_member(X, Tail).

%possible moves
move([X,Y],[X2,Y2]):- X2 is X, Y2 is Y+1.	%move up
move([X,Y],[X2,Y2]):- X2 is X+1, Y2 is Y.	%move right
move([X,Y],[X2,Y2]):- X2 is X-1, Y2 is Y.	%move left

% grid plan
grid([GX,GY],[X2,Y2]):- X2>=0, Y2>=0, X2=<GX, Y2=<GY.

% safe base case
safe([], _).

% safe recur
safe([[NX,NY]|Locations], [PX,PY]) :- sqrt((NX-PX)^2 + (NY-PY)^2) >= 6, safe(Locations,[PX,PY]).
