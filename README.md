# Generalizing Uncertainty Propagation Calculations

**Theo Estoup Ruiz**

## Theory

### Uncertainty

Functions that involve measured values take on the uncertainty of these measured values in accordance to their uncertainty and the partial derivative of the function. The general expression is:

$$\delta y = \sqrt{\left(\frac{\partial y}{\partial x_1}\right)^2 \delta x_1^2 + \left(\frac{\partial y}{\partial x_2}\right)^2 \delta x_2^2 + \left(\frac{\partial y}{\partial x_3}\right)^2 \delta x_3^2 + \dots + \left(\frac{\partial y}{\partial x_n}\right)^2 \delta x_n^2}$$

Formalized as

$$\delta y = \sqrt{\sum_i \left(\frac{\partial y}{\partial x_i} \delta x_i\right)^2}$$

Where $\delta \mathbf{y}$ is the uncertainty of a function $\mathbf{y}$, a function of measured quantities $(\mathbf{x_1, x_2, x_3 \dots x_n})$, $\frac{\partial y}{\partial x}$ is the partial derivative of the function $\mathbf{y}$ with respect to a given measured quantity $\mathbf{x_n}$, and $\delta \mathbf{x}$ is the uncertainty of the measured quantity.

### Using the Jacobian

The Jacobian matrix describes a function as a transformation of a plane. Generally, it is described as:

$$\mathbf{J_y} = \begin{bmatrix} \frac{\partial y_1}{\partial x_1} & \cdots & \frac{\partial y_1}{\partial x_n} \\ \vdots & \ddots & \vdots \\ \frac{\partial y_n}{\partial x_1} & \cdots & \frac{\partial y_n}{\partial x_n} \end{bmatrix}$$

Where $\mathbf{J_y}$ is the jacobian of $\mathbf{y}$, a function of variables $(\mathbf{x_1, x_2, x_3 \dots x_n})$, and $\frac{\partial \mathbf{y_n}}{\partial \mathbf{x_n}}$ is the partial derivative of the component $\mathbf{y_n}$ of function $\mathbf{y}$ in $\mathbb{R}^n$ vector space with respect to variable $\mathbf{x_n}$.

For the purposes of this function, we can say that the Jacobian is a way of extracting all the derivative information from a function and putting it into a neat matrix we can reference.

That's all the theory we need to understand what the function is doing. The comments should give more insight as to what each step is doing.
