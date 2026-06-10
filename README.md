# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
```
clc; 
clear; 

xn = [1 2 1 2 1 2 1 2]; 

n1 = 0:1:length(xn)-1; 
subplot(3,1,1); 
plot2d3(n1, xn); 
xlabel('Time n'); 
ylabel('Amplitude xn'); 
title('Input Sequence'); 

j = sqrt(-1); 
N = length(xn); 
Xk = zeros(1, N); 

for k = 0:N-1 
    for n = 0:N-1 
        Xk(k+1) = Xk(k+1) + xn(n+1)*exp((-j*2*%pi*k*n)/N); 
    end 
end 

disp(Xk); 

K1 = 0:1:length(Xk)-1; 
magnitude = abs(Xk); 

subplot(3,1,2); 
plot2d3(K1, magnitude); 
xlabel('frequency(Hz)'); 
ylabel('magnitude(gain)'); 
title('magnitude spectrum'); 

angle = atan(imag(Xk), real(Xk)); 

subplot(3,1,3); 
plot2d3(K1, angle); 
xlabel('frequency(Hz)'); 
ylabel('Phase'); 
title('Phase spectrum');
```
## CALCULATIONS:

<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/f0a39507-9beb-43e2-b122-66f95c679793" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/1bb660d5-ab3d-4a18-84da-d9276359c3f3" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/3b345c93-f4f0-4676-97f2-0acd58eb1e96" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/803112f4-2749-4c9d-9085-a9c62ab895e5" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/c37067bf-7d62-472a-a377-65671e1e38a3" />




## SAMPLE OUTPUT:

<img width="1599" height="899" alt="image" src="https://github.com/user-attachments/assets/24fb7f48-b522-48ec-8a58-0cb450de8201" />



## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

