# 💻 NET112 SSE Image Processing 💻
Optimising an image program using the SSE instruction set to speed up processing of the image. Implemented using C++.

## Speed Comparison
The algorithm is run on the image 100 times in order to gain an accurate mean time.

### Debug Build

***Compiler Optimisations***
> Optimisation : Disabled (/Od)

> Inline Function Expansion : Default

> Favor Size Or Speed : Neither

> Enable Fibre-Safe Optimisations : No

> Whole Program Optimisation : No

**Results**

|  Algorithm Used|Speed (s)|
|----------------|---------------------|
|Default Gaussian Algorithm|`7.65893` |
|Optimised SSE Algorithm |`3.03469` |


### Release Build

***Compiler Optimisations***
> Optimisation : Maximum Optimization (Favor Speed) (/O2)

> Inline Function Expansion : Any Suitable (/Ob2)

> Favor Size Or Speed : Favor fast code (/Ot)

> Enable Fibre-Safe Optimisations : Yes (/GT)

> Whole Program Optimisation : Yes (/GL)

**Results**

|  Algorithm Used|Speed (s)|
|----------------|---------------------|
|Default Gaussian Algorithm|`2.76909` |
|Optimised SSE Algorithm |`0.693454` |


## Output Comparison

### Original Image
![](images/rec.png)

### Processed Image
![](images/filtered.png)
