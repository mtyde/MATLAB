MATLAB
======

#Metoda Newtona

##za pomocą pętli for 

format compact<br>
format long %obliczenia bardziej dokładne%<br>
clc%czyści ekran%<br>
x=-2*pi:0.1:2*pi;<br>
y=cos(x)+sin(x);<br>
x=x/pi;<br>
y1=x*0; %funkcja liniowa przechodząca przez y=0 taka prowizoryczna oś x %<br>
plot(x,y,x,y1)<br>
xlabel('x/\pi') <br>
x0=0.01*pi;<br>
for i=1:10<br>
    x1=x0-(cos(x0)+sin(x0))/(-sin(x0)+cos(x0));%wzór na metodę newtona%<br>
    if abs(x1-x0)<10^-3 %abs wartość bezwzględna spr warunek zadania|xn+1-xn|<t0=10 do -8%<br>
        break %robi się w w instrukcji warunkowej%<br>
    end<br>
    %x1/pi% %zamiana x1 na radiany% <br>
    x0=x1;<br>
end<br>
i %ilosc iteracji%<br>
x1/pi<br>

##za pomocą pętli while


format compact<br>
format long %obliczenia bardziej dokładne%<br>
clc%czyści ekran%<br>
x=-2*pi:0.1:2*pi;<br>
y=cos(x)+sin(x);<br>
x=x/pi;<br>
y1=x*0; %funkcja liniowa przechodząca przez y=0 taka prowizoryczna oś x %<br>
plot(x,y,x,y1)<br>
xlabel('x/\pi') <br>
x00=0.01*pi;<br>
x1=x00<br>
x0=x1+1; %przy pętli for x1=x0+1;%<br>
while abs(x1-x0)<10^-3<br>
    x0=x1;<br>
     x1=x0-(cos(x0)+sin(x0))/(-sin(x0)+cos(x0));<br>
end<br>
i %ilosc iteracji%<br>
x1/pi

lub zdefnwać funcję f=@(x)(cos(x0)+sin(x0))/(-sin(x0)+cos(x0))<br>

format compact<br>
format long %obliczenia bardziej dokładne%<br>
clc%czyści ekran%<br>
f=@(x)(cos(x0)+sin(x0))/(-sin(x0)+cos(x0))<br>
x=-2*pi:0.1:2*pi;<br>
y=cos(x)+sin(x);<br>
x=x/pi;<br>
y1=x*0; %funkcja liniowa przechodząca przez y=0 taka prowizoryczna oś x %<br>
plot(x,y,x,y1)<br>
xlabel('x/\pi') <br>
x00=0.01*pi;<br>
x1=x00<br>
x0=x1+1; %przy pętli for x1=x0+1;%<br>
while abs(x1-x0)<10^-3<br>
    x0=x1;<br>
     x1=x0-f(x0);<br>
end<br>
i %ilosc iteracji%<br>
x1/pi

