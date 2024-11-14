practical 5th
f=poly([1,-2,0,1],'x','c');
disp(f,'the polynomial f is');
k=horner(f,2);
disp(k,'value of polynomial f at x=2 is');

g=poly([1,0,-1],'x','r');
disp(g,'the polynomial g is');
l=horner(g,3);
disp(l,'the value of polynomial g at x=3 is');

x=poly(0,'x');
h=2*x^3-7*x^2+4*x-15;
disp(h,'the polynomial h is');
m=horner(h,5);
disp(m,'value of the polynomial h at x=5 is');
x=poly(0,'x');
p=2*x^3-7*x^2+4*x-15
disp(p,'the polynomial is');
k=horner(p,5);
disp(k,'value of the polynomial p at x=5 is');
