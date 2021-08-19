# Diffusion-equation

## Using the heat-conduction/diffusion equation to determine the temperature at a particular time for a specific point in space. This will allows us to know the temperature and how it changed over time until an equilibrium is established. 

Parameters

kappa = The diffusivity coefficient 

x_rng = The bounds of the space range that is being considered

t_rng = The range of time that is being considered

u_init = The function handle that is giving the initial state 

u_bndry = The function handle giving the boundary conditions

nx = The number of intervals the x-range should be divided by

nt = The number of intervals the time should be divided into 

**To find the solution**

1. Error checking was done to make sure that kappa(dt/h^2) value is less than 0.5. This will ensure that the error is small. If it is greater than 0.5, the user is alerted to change their nt value and the function is stopped. 
2. Initilization the constant is done. This will be used in the heat-conduction/diffusion equation as well as the matrix to input the final values into. This will also give a matrix of answers. The boundaries of the matrix were also intialized to help find the solution of the interior points
3. Solved the problem by taking the value of the constant, the matrix with the initial boundaries. These were used to solve the heat-conduction/diffusion equation and inputted the values for their respective point in the matrix.  

**Example: Solving the diffusion equation using the command diffusion1d(0.1, [0,1],6,[1,3],12,@u2a_init,@u2a_bndry)**

![image](https://user-images.githubusercontent.com/58648072/130008958-65932811-1dae-4e26-8a74-96d20c5376d8.png)

![image](https://user-images.githubusercontent.com/58648072/130008999-a312b89d-9ac0-4365-94b7-5db7aacd84ee.png)

**Example: Solving the same diffusion equation as before with more points**

![image](https://user-images.githubusercontent.com/58648072/130009078-82f37c4e-c7ce-43d5-a884-1072801624d5.png)

**Example: Solving the diffusion equation using the command diffusion1d( 0.11, [0,5], 100, [0, 28], 5000, @u2c_init, @u2c_bndry )**

![image](https://user-images.githubusercontent.com/58648072/130009197-ca3ac83b-c664-4ecb-80a7-b1801802e93c.png)

