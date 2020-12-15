# exam2D
examen 2D

import matplotlib.pyplot as plt
import numpy as np
import math as mt

# DIMENCIONES 
plt.axis("on")
plt.axis([0,100,0,100])

# RADIO DEL CIRCULO CONFORME A MI NUMERO DE CONTROL
Numero_Control=2
Penultimo_Num_Control=6

# RADIO
r=Numero_Control*5

# PUNTO INICIAL
xc=50
yc=50
Rz=(xc,yc)
alpha1=mt.radians(1)
alpha2=mt.radians(360)
dalpha=mt.radians(1)

# PUNTO DEL CIRCULO
plt.scatter(xc,yc,s=1,color=(7/10, 4/10, 2/10))

for alpha in np.arange(alpha1,alpha2,dalpha):
    x=xc+r*mt.sin(alpha)
    y=yc+r*mt.cos(alpha)
    plt.scatter(x,y,s=1,color=(0/10, 6/10, 2/10))
x1=xc
x2=10
y1=yc
y2=10

# IMPRESION FIGURA 1
plt.plot([x1,x1],[y1,y2],linewidth=1,color=(0/10, 6/10, 2/10))
plt.plot([x2,x2],[y1,y2],linewidth=1,color=(0/10, 6/10, 2/10))
plt.plot([x1,x2],[y1,y1],linewidth=1,color=(0/10, 6/10, 2/10))
plt.plot([x1,x2],[y2,y2],linewidth=1,color=(0/10, 6/10, 2/10))

# IMPRESION ORIGINAL FIGURA 2
x1=70
x2=30
y1=70
y2=30

# DIBUJO DE LA FIGURA 
plt.plot([x1,x1],[y1,y2],linewidth=1,color=(0/10, 6/10, 2/10))
plt.plot([x2,x2],[y1,y2],linewidth=1,color=(0/10, 6/10, 2/10))
plt.plot([x1,x2],[y1,y1],linewidth=1,color=(0/10, 6/10, 2/10))
plt.plot([x1,x2],[y2,y2],linewidth=1,color=(0/10, 6/10, 2/10))

plt.title('Examen 2D')
plt.show()
