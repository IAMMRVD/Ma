
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Java Code Snippets</title>
<style>
    pre {
        background-color: #ffffff;
        padding: 1px;
        border-radius: 1px;
        overflow-x: auto;
    }
</style>
</head>
  <center><img src="https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png" alt="Google Logo"></center>
<body style="background-color: white; color: white;">


<form action="https://www.google.com/search" method="get" target="_blank">
        <label for="search-query">Enter your search query:</label><br>
        <input type="text" id="search-query" name="q" required><br><br>
        <input type="submit" value="Google Search">
    </form>

<h1>NAVUSA COPY MADTHA IDVI NIVSA MADI</h1>
<p style="color: red;">A</p>

<button onclick="copyCode(1)">1</button>
<button onclick="copyCode(2)">2</button>
<button onclick="copyCode(3)">3</button>
<button onclick="copyCode(4)">4</button>
<button onclick="copyCode(5)">5</button>
<p style="color: red;">B</p>
<button onclick="copyCode(6)">6</button>
<button onclick="copyCode(7)">7</button>
<button onclick="copyCode(8)">8</button>
<button onclick="copyCode(9)">9</button>
<button onclick="copyCode(10)">10</button>
<pre id="code1">

from sympy import *
var('x y z') 
a=int(input("Enter the value of a :"))
b=int(input("Ener the value of b :")) 
c=int(input("Enter the value of c :")) 
I= integrate(x**2+y**2+z**2, (z,-a,a), (y,-b,b), (x,-c,c))
print("I=",I)

</pre>

<pre id="code2">
from sympy import *

var(' x y z') 

a=int(input("Enter the value of a :"))

b=int(input("Enter the value of b :"))

c=int(input("Enter the value of c :"))

V= integrate(1,(z,0,c*(1-x/a-y/b)), (y,0,b*(1-x/a)), (x,0,a))

print("Volume, V=",V)
</pre>

<pre id="code3">
from sympy import *
from sympy.physics.vector import *
var('x y z')
v=ReferenceFrame('v') 
phi=v[0] ** 2*v[1]+2*v[0]*v[2]-4
G= gradient (phi, v ) 
G=G. subs ([(v[0],x), (v[1],y), (v[2],z)])
print ("\n Gradient of the scalar function is")
display (G)
</pre>

<pre id="code4">

from sympy import *
from sympy.physics.vector import *
var('x y z')
v=ReferenceFrame('v')
F=2*v[0]**2*v.x-3*v[1]*v[2]*v.y+v[0]*v[2]**2*v.z
D= divergence (F, v)
D=D. subs ([(v[0],x), (v[1],y), (v[2],z)])
print ("\n Divergence of the vector point function F is")
display (D)
C= curl (F,v)
C=C. subs ([(v[0],x), (v[1],y), (v[2],z)]) 
print ("\n Curl of the vector point function F is")
display (C)
</pre>

<pre id="code5">

from sympy import *
var('x y')
a=int(input("Enter the value of a :")) 
b=int(input("Ener the value of b:"))
A=4*integrate (1, (y, 0,(b/a)*sqrt(a**2-x**2)), (x,0,a))
print(' A=',A)

</pre>

<pre id="code6">
from sympy import*
var ('x,y')
p=y-sin(x)
q=cos(x)
f= diff (q, x) -diff (p, y) 
soln= integrate (f, [y, 0,2*x/2], [x,0, pi/2])
print ("I", soln)
</pre>

<pre id="code7">
from sympy import*
var('x y')
x0,y0=0,0
x1,x2,x3=0.1,0.2,0.3 
y1=2*y+3*exp(x)
y2=2*y1+3*exp(x) 
y3=2*y2+3*exp(x)
y4=2*y3+3*exp(x) 
y1=y1.subs({x:0,y:0})
y2=y2.subs({x:0,y:0}) 
y3=y3.subs({x:0,y:0}) 
y4=y4. subs({x:0,y:0})
print(f'yl={y1},y2={y2},y3={y3},y4={y4}')
TS=y0+(x-x0)*y1+(x-x0)**2*y2/2+(x-x0)**3*y3/6+(x-x0)**4*y4/24 
print(f'The required Taylors series is\n y= ') 
display(TS) 
TSx1=round(TS.subs({x:x1}),4)
print(f'The va value of y({x1})= {TSx1}') 
TSx2=round(TS.subs({x:x2}),4) 
print(f'The value of y({2})={TSx2}') 
TSx3=round(TS.subs( {x:x3}),4)
print(f'The value of y({x3})={TSx3}')
</pre>
<pre id="code8">
from numpy import*
def f(x,y):
    return 1+(y/x)
x0=float(input('Enter value of x0='))
y0=float(input('Enter value of y0='))
h=float(input('Enter value of step size h'))
n=int(input('Enter value of n='))
for i in range(1,n):
    k1=round(h*f(x0,y0),4)
    k2=round(h*f(x0+(h/2),y0+(k1/2)),4)
    k3=round(h*f(x0+(h/2),y0+(k2/2)),4)
    k4=round(h*f(x0+h,y0+k3),4)
    y=round(y0+(1/6)*(k1+2*k2+2*k3+k4),4)
    print(f'k1={k1}, k2={k2}, k3={k3}, k4={k4}')
    x0,y0=x0+h,y 
    print(f'The value of y{round(x0,4)}={y}')
 </pre>
<pre id="code9">
from numpy import*
def f(x,y):
    return 2*x + y

x0=float(input('Enter value of x0='))
y0=float(input('Enter value of y0='))
h=float(input('Enter value of step size h'))
n=int(input('Enter value of n='))
for i in range(1,n):
    k1=round(h*f(x0,y0),4)
    k2=round(h*f(x0+(h/2),y0+(k1/2)),4)
    k3=round(h*f(x0+(h/2),y0+(k2/2)),4)
    k4=round(h*f(x0+h,y0+k3),4)
    y=round(y0+(1/6)*(k1+2*k2+2*k3+k4),4)
    print(f'k1={k1}, k2={k2}, k3={k3}, k4={k4}')
    x0,y0=x0+h,y 
    print(f'The value of y({x0})={y}')
</pre>
<pre id="code10">
from numpy import*
def f(x,y):
    return x-y**2
x0,x1, x2,x3,x4=0.0,0.2,0.4,0.6,0.8
y0,y1,y2,y3=0.0,0.02,0.0795,0.1762
h=0.2
f0,f1,f2,f3=f(x0,y0),f(x1,y1),f(x2,y2),f(x3,y3)
y4_p=round(y0+(4*h/3)*(2*f1-f2+2*f3),4)
print(f'The predicted value of y4 is y4_p={y4_p}')
f4=round(f(x4, y4_p),4)
print(f'f4={f4}')
for i in range (1,3):
    y4_c=round(y2+(h/3)*(f2+4*f3+f4),4) 
    print(f'The corrected value of y4 is y4_c={y4_c}')
    f4=round(f(x4,y4_c),4)
    print(f'f4={f4}')
</pre>
<script>
function copyCode(id) {
    var code = document.getElementById('code' + id);
    var range = document.createRange();
    range.selectNode(code);
    window.getSelection().removeAllRanges();
    window.getSelection().addRange(range);
    document.execCommand("copy");
    window.getSelection().removeAllRanges();
    alert("Code " + id + " copied to clipboard!");
}
</script> 
<p style="color: red;">created by mr_______d</p>

