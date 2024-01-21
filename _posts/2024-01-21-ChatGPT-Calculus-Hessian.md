---
title: ChatGPT로 미적분학 공부하기 (2) 이변수함수의 극점과 안장점
sidebar:
  nav: docs-ko
aside:
  toc: true
key: 20240120
tags: ChatGPT 미적분학 편미분 안장점 'saddle point'
lang: ko
---

이변수함수의 헤시안 행렬(Hessian matrix)을 이용하여 극점(extrema)과 안장점(saddle point)을 구해달라고 요청해봅시다.
>[!user] User
> Find the local maximum and minimum values and saddle points of the functions:
(a) $f(x, y)=\frac{1}{x}+x y+\frac{1}{y}$,
(b) $g(x, y)=x^4+x^2-2 x y+y^2+2 x-2 y+3$

>[!gpt] ChatGPT
> To find the local maximum, local minimum, and saddle points of the given functions, we'll need to use the second partial derivative test. Here's the process:
> 
> 1. Compute the first partial derivatives, $f_x$ and $f_y$.
> 2. Set the first partial derivatives equal to zero to find critical points.
> 3. Compute the second partial derivatives: $f_{xx}$, $f_{yy}$, and $f_{xy}$.
> 4. Evaluate the second partial derivatives at each critical point.
> 5. Use the discriminant, $D$, given by $D = f_{xx}f_{yy} - f_{xy}^2$.
> 
> If $D > 0$ and $f_{xx} > 0$, the point is a local minimum.  
> If $D > 0$ and $f_{xx} < 0$, the point is a local maximum.  
> If $D < 0$, the point is a saddle point.  
> If $D = 0$, the test is inconclusive.
> 
> Let's start with function $f(x, y) = \frac{1}{x} + xy + \frac{1}{y}$:
> 
> 1. Compute $f_x$ and $f_y$.
> 2. Solve for the critical points.
> 3. Compute $f_{xx}$, $f_{yy}$, and $f_{xy}$.
> 4. Evaluate the second partial derivatives at each critical point.
> 5. Apply the second partial derivative test.
> 
> >[!tip] Analysis : Error
> 
> It seems I made an error when evaluating the second partial derivatives at each critical point. The issue is likely related to the format of the critical points obtained. Let's first inspect the critical points to better understand their structure and then proceed with the evaluation.
> 
> >[!tip] Analysis : Error
> 
> The critical points we obtained for $f$ are:
> 1. $(1, 1)$
> 2. $\left( -\frac{1}{2} - \frac{\sqrt{3}i}{2}, -\frac{1}{2} - \frac{\sqrt{3}i}{2} \right)$
> 3. $\left( -\frac{1}{2} + \frac{\sqrt{3}i}{2}, -\frac{1}{2} + \frac{\sqrt{3}i}{2} \right)$
> 
> The second and third critical points are complex, which means they're not relevant for our study of local extrema in the real plane. We'll only consider the first critical point, $(1, 1)$, for further analysis.
> 
> Let's proceed with the evaluation of the second partial derivatives at the point $(1, 1)$ and then apply the second partial derivative test.
> 
> >[!tip] Analysis : Completed
> 
> The values of the second partial derivatives at the point $(1, 1)$ are:
> 
> $$
> f_{xx}(1,1) = 2, \quad f_{yy}(1,1) = 2, \quad f_{xy}(1,1) = 1
> $$
> 
> Now, let's compute the discriminant $D$ using the formula:
> 
> $$
> D = f_{xx}f_{yy} - f_{xy}^2
> $$
> 
> and then apply the second partial derivative test.
> 
> >[!tip] Analysis : Completed
> 
> The value of the discriminant $D$ at the point $(1, 1)$ is $3$.
> 
> Given that $D > 0$ and $f_{xx}(1,1) > 0$, the point $(1, 1)$ is a local minimum for the function $f$.
> 
> Next, let's analyze the function $g(x, y) = x^4 + x^2 - 2xy + y^2 + 2x - 2y + 3$. We'll follow the same steps:
> 
> 1. Compute $g_x$ and $g_y$.
> 2. Solve for the critical points.
> 3. Compute $g_{xx}$, $g_{yy}$, and $g_{xy}$.
> 4. Evaluate the second partial derivatives at each critical point.
> 5. Apply the second partial derivative test.
> 
> >[!tip] Analysis : Error
> 
> Again, I made an error when evaluating the second partial derivatives at the critical points for the function $g$. Let's inspect the critical points for $g$ to better understand their structure and then proceed with the evaluation.
> 
> >[!tip] Analysis : Completed
> 
> The critical point for function $g$ is $(0, 1)$.
> 
> Let's evaluate the second partial derivatives at this critical point and then apply the second partial derivative test.
> 
> >[!tip] Analysis : Completed
> 
> The values of the second partial derivatives at the point $(0, 1)$ are:
> 
> $$
> g_{xx}(0,1) = 2, \quad g_{yy}(0,1) = 2, \quad g_{xy}(0,1) = -2
> $$
> 
> Now, let's compute the discriminant $D$ for $g$ using the formula:
> 
> $$
> D = g_{xx}g_{yy} - g_{xy}^2
> $$
> 
> and then apply the second partial derivative test.
> 
> >[!tip] Analysis : Completed
> 
> The value of the discriminant $D$ at the point $(0, 1)$ for function $g$ is $0$.
> 
> Given that $D = 0$, the second partial derivative test is inconclusive for the function $g$ at the point $(0, 1)$. This means we cannot determine whether the point is a local maximum, local minimum, or saddle point using this test.
> 
> In summary:
> - For the function $f$, the point $(1, 1)$ is a local minimum.
> - For the function $g$, the test is inconclusive at the point $(0, 1)$.

풀이에 필요한 논리를 설계한 후, 파이썬 코드를 스스로 작성하여 시도해보고, 에러가 발생하면 원인을 파악하여 버그를 고치고 다시 시도하여 풀이과정을 진행함을 확인할 수 있습니다. 