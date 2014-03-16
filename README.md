MATLAB
======

Metoda Newtona

za pomocą pętli for 

format compact
format long %obliczenia bardziej dokładne%
clc%czyści ekran%
x=-2*pi:0.1:2*pi;
y=cos(x)+sin(x);
x=x/pi;
y1=x*0; %funkcja liniowa przechodząca przez y=0 taka prowizoryczna oś x %
plot(x,y,x,y1)
xlabel('x/\pi') 
x0=0.01*pi;
for i=1:10
    x1=x0-(cos(x0)+sin(x0))/(-sin(x0)+cos(x0));%wzór na metodę newtona%
    if abs(x1-x0)<10^-3 %abs wartość bezwzględna spr warunek zadania|xn+1-xn|<t0=10 do -8%
        break %robi się w w instrukcji warunkowej%
    end
    %x1/pi% %zamiana x1 na radiany% 
    x0=x1;
end
i %ilosc iteracji%
x1/pi

