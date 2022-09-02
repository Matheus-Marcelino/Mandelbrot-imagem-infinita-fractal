import numpy as np
import matplotlib.pyplot as plt


def fractal(Real, Imaginario, Nmax):  # verifica o N (complexo) pertence ao conjunto
    c = complex(Real, Imaginario)
    z = 0.0j

    for i in range(Nmax):
        z = z * z + c
        if(z.real * z.real + z.imag * z.imag) >= 4:
            return i

    return Nmax


x = y = 2000  # Pixels
tamanho = np.zeros([x, y])

# varrendo todos os pixels do conjunto
for eixo_x, Real in enumerate(np.linspace(-2, 1, num=x)):
    for eixo_y, Imaginario in enumerate(np.linspace(-1, 1, num=y)):
        tamanho[eixo_x, eixo_y] = fractal(Real, Imaginario, 100)

plt.figure(dpi=100)  # grafico
plt.imshow(tamanho.T, cmap='hot',
           interpolation='bilinear', extent=[-2, 1, -1, 1])
plt.xlabel('Real')
plt.ylabel('Imaginario')
plt.show()
