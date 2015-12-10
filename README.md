# Publib

Produce publication-level quality images on top of Matplotlib

For similar librairies, see seaborn, which also add neat high-end API to 
Matplotlib function calls.


### Use

    Call set_style() at the beginning of the script
    Call buff_style() after each new axe is plotted
    
    Note that importing publib will already load the default style. 

    A couple more styles ('poster', 'article') can be selected with the function
    set_style()
    
    Because some matplotlib parameters cannot be changed before the lines are 
    plotted, they are called through the function buff_style() which:
    - changes the minor ticks
    - remove the spines
    - turn the legend draggable by default

## Examples
```import numpy as np
import matplotlib.pyplot as plt
import publib
a = np.linspace(0,6.28)
plt.plot(a,np.cos(a))   # plotted by publib 'default' style
plt.show()

publib.set_style('article')
plt.plot(a,a**2)
publib.buff_style('article')
plt.show()
```