# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
~~~
clc;
clear;
xn=[1 2 3 1 1 2 0 0];
n1=0:1:length(xn)-1;
subplot(3,1,1);
plot2d3(n1,xn);
xlabel('Time n');
ylabel('Amplitude xn');
title('Input Sequence');
j=sqrt(-1);
N=length(xn);
Xk=zeros(1,N);
      for k=0:N-1
          for n=0:N-1
              Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);
      end
end
disp(Xk)
K1=0:1:length(Xk)-1;
magnitude=abs(Xk)
subplot(3,1,2);
plot2d3(K1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');
angle=atan(imag(Xk),real(Xk))
subplot(3,1,3);
plot2d3(K1,angle);
xlabel('frequency(Hz)');
ylabel('phase');
title('Phase spectrum');
~~~
<br>
<br>
<br>
<br>
<br>

<br>
### CALCULATIONS:
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/a0070030-dd09-4dc6-b937-1f26b5b20c78" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/db3c3b4c-7991-4c19-a605-25b53e095a6b" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/bbd8537a-5fdb-4ad9-a962-03316398d60a" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/6b02e32d-8b7c-45d1-b1e8-8e55385809ed" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/9b9bf607-21df-4430-92b9-e73276332334" />

<br>
<br>
<br>
<br>
<br>
### SAMPLE OUTPUT:
<img width="1599" height="615" alt="image" src="https://github.com/user-attachments/assets/fc037848-cb9f-4c29-87ad-e1f5e0c60924" />

<br>
<br>
<br>
<br>



## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

