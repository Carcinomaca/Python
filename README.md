prac1:Bisection method
p = poly([-3,-1,0,1],'x','c');
a = 1
b = 2
for i = 1:10
    fa = horner(p,a);
    fb = horner(p,b);
    c = (a+b)/2;
    fc = horner(p,c);
    if (fa * fc) < 0 then
        b = c;
    else 
        a = c;
    end    
end
disp(p);
disp(c);
prac2:false position method
v = poly([1,-3,1],'x','c')
x1 = 1;
x2 = 3;
for i = 1:5
   p = horner(v,x1);
    q = horner(v,x2);
    x3 = ((x2*p)-(x1*q))/(p-q);
    n = horner(v,x3)
    if (p*n)>0 then
        x1 = x3;
    else
        x2 = x3;
    end
    
end
disp(v);
disp(x3);
prac3:false pos method using function
function[c]=FalsePos(a,b,p,n)
    while n >0
        fx = horner(p,a)
        fy = horner(p,b)
        c = (b*fx-a*fy)/(fx-fy)
        fz = horner(p,c)
        if (fx*fz)>0 then 
            a = c
        else
            b = c
        end 
        n = n - 1
    end
    disp(c)
endfunction
prac4:newton raphson
function [x2] = newraph(x1,p,n)
    p1 = derivat(p);
    for i = 1:n
        fo = horner(p,x1);
        f1 = horner(p1,x1);
        x2 = x1 - (fo/f1);
        x1=x2;
        
    end
endfunction
prac5:trapezoidal
function[val] = trapezoidal(a,b,n,p)
    h = (b-a)/n
    x = a:h:b
    lim = length(x)
    val = horner(p,a)+horner(p,b)
    for i = 2:(lim-1)
        val = val + 2*horner(p,x(i))
    end
    val = val*(h/2)
    disp(val)
endfunction
prac6:simpson1/3
function [val]=simpson13(a,b,n,p)
    h = (b-a)/n;
    x = a:h:b
    lim = length(x);
    val =horner(p,a) + horner(p,b);
    for i = 2:(lim-1)
        if (modulo(i,2)==0)
            val = val + 4 * horner(p,x(i));
        else
            val = val + 2 * horner(p,x(i));
        end    
    end
    val = val*(h/3);
    disp(val)
endfunction
prac7:simpson3/8
function [val]=simpson38(a,b,n,p)
    h = (b-a)/n;
    x = a:h:b
    lim = length(x);
    val =horner(p,a) + horner(p,b);
    for i = 2:(lim-1)
        if (modulo(i-1,3)==0)
            val = val + 2 * horner(p,x(i));
        else
            val = val + 3 * horner(p,x(i));
        end    
    end
    val = val*(3*h/8);
    disp(val)
endfunction
prac8:Eulerm
function [y0]=eulerm(x0,y0, h, x, f)
n=(x-x0)/h;
for i=1:n
y0=y0+f(x0,y0) *h;
x0=x0+h;
y0
end
endfunction
prac9:Runge kutta 2nd order. 
function[y1]=rk(x0,y0,h,x,f)
    h = 0.2
    k1=h*f(x0,y0)
    k2=h*f(x0+h,y0+k1)
    y1=y0+0.5*(k1+k2)
endfunction
prac10:scattered diagram.
x = [2,3,7,9,15,20]
y = [25,20,17,14,11,8]
plot(x,y)
prac11:karl pearson
function[r]=correl(x,y)
    n=length(x)
    sx=sum(x)
    sy=sum(y)
    sxy=sum(x*y)
    sxx=sum(x*x)
    syy=sum(y*y)
    xmean=sx/n
    ymean=sy/n
    sd1=sqrt(sxx/n)-(xmean^2)
    sd2=sqrt(syy/n)-(ymean^2)
    c=((sxy/n)-xmean*ymean)
    r=c/(sd1*sd2)
    if r >0 then
        print("x and y are positively related/n")
    else
        print("x and y are negatively related/n")
    end
    disp(r)
endfunction


