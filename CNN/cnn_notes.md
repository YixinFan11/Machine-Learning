### Section I: Architecture
<details>
  <summary> Convolutional Function</summary>
  
For continuous cases:
  
<img src="https://latex.codecogs.com/svg.image?s(t)=(f*g)(t)=\int_{-\infty}^{\infty}f(\tau)g(t-\tau)d\tau" title="s(t)=(f*g)(t)=\int_{-\infty}^{\infty}f(\tau)g(t-\tau)d\tau" />
  
For discrete cases:
  
<img src="https://latex.codecogs.com/svg.image?s(t)=(f*g)(t)=\sum_{-\infty}^{\infty}f(\tau)g(t-\tau)" title="s(t)=(f*g)(t)=\sum_{-\infty}^{\infty}f(\tau)g(t-\tau)" />
  
s(t) is typically referred to as the feature map, f is the input and g is the kernel filter that acts as an average weighting applied to f

Number of parameters:
  
  <img src="https://latex.codecogs.com/svg.image?n_{param}&space;=&space;(K_x&space;*&space;K_y&space;*&space;O_z&space;&plus;&space;1)&space;*&space;I_z&space;" title="n_{param} = (K_x * K_y * O_z + 1) * I_z " />
</details>

<details>
  <summary> Kernel Size</summary>
  The kernel size is also sometimes called the receptive field
</details>
