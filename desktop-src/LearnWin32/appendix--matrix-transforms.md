---
title: Transformações de matriz de apêndice
description: Este tópico fornece uma visão geral matemática das transformaçãos de matriz para gráficos 2D.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d02976446824bba07829173bb326338a55732b39c640c93319630a209096b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389181"
---
# <a name="appendix-matrix-transforms"></a>Apêndice: Transformaçãos de Matriz

Este tópico fornece uma visão geral matemática das transformaçãos de matriz para gráficos 2D. No entanto, você não precisa saber matemática de matriz para usar as transformaçãos em Direct2D. Leia este tópico se você estiver interessado em matemática; caso contrário, sinta-se à vontade para ignorar este tópico.

-   [Introdução às matrizes](#introduction-to-matrices)
    -   [Operações de matriz](#matrix-operations)
-   [Transformações de afinidade](#affine-transforms)
    -   [Transformação de tradução](#translation-transform)
    -   [Transformação de dimensionamento](#scaling-transform)
    -   [Rotação em torno da origem](#rotation-around-the-origin)
    -   [Rotação em torno de um ponto arbitrário](#rotation-around-an-arbitrary-point)
    -   [Transformação distorção](#skew-transform)
-   [Representando as transformação em Direct2D](#representing-transforms-in-direct2d)
-   [Próximo](#next)

## <a name="introduction-to-matrices"></a>Introdução às matrizes

Uma matriz é uma matriz retangular de números reais. A *ordem* da matriz é o número de linhas e colunas. Por exemplo, se a matriz tiver 3 linhas e 2 colunas, a ordem será 3 × 2. Matrizes geralmente são mostradas com os elementos de matriz entre colchetes:

![Matriz 3 x 2.](images/matrix01.png)

Notação: uma matriz é designada por uma letra maiúscula. Os elementos são designados por letras minúsculas. Subscritos indicam o número de linha e coluna de um elemento. Por exemplo, um *ij* é o elemento na i'th linha e na coluna j'th da matriz A.

O diagrama a seguir mostra × matriz j, com os elementos individuais em cada célula da matriz.

![uma matriz com linhas i e colunas j.](images/matrix15.png)

### <a name="matrix-operations"></a>Operações de matriz

Esta seção descreve as operações básicas definidas em matrizes.

*Adição* de . A soma A + B de duas matrizes é obtida adicionando os elementos correspondentes de A e B:

<dl> A + B = \[ a *ij* \]  +  \[ b *ij* \]  =  \[ a *ij* + b *ij*\]
</dl>

*Multiplicação escalar.* Essa operação multiplica uma matriz por um número real. Dado um número real *k*, o produto escalar kA é obtido multiplicando cada elemento de A por *k*.

<dl> kA = k \[ a *ij* \]  =  \[ k × a *ij*\]
</dl>

*Multiplicação de matriz.* Considerando duas matrizes A e B com ordem (m × n) e (n × p), o produto C = A × B é uma matriz com ordem (m × p), definida da seguinte forma:

![Mostra uma fórmula para multiplicação de matriz.](images/matrix02.png)

ou, de forma equivalente:

<dl> c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *em* + b *nj*  
</dl>

Ou seja, para calcular cada elemento c *ij*, faça o seguinte:

1.  Pegue a linha i'th de A e a coluna j'th de B.
2.  Multiplique cada par de elementos na linha e na coluna: a primeira entrada de linha pela primeira entrada de coluna, a segunda entrada de linha pela segunda entrada de coluna e assim por diante.
3.  Soma o resultado.

Aqui está um exemplo de multiplicação de uma matriz (2 × 2) por uma matriz (2 × 3).

![multiplicação de matriz.](images/matrix03.png)

A multiplicação de matriz não é comutativa. Ou seja, A × B ≠ B × A. Além disso, na definição, ela segue que nem todos os pares de matrizes podem ser multiplicados. O número de colunas na matriz à esquerda deve ser igual ao número de linhas na matriz à direita. Caso contrário, o × operador não está definido.

*Identificar matriz*. Uma matriz de identidade, designada I, é uma matriz quadrada definida da seguinte forma:

<dl> I *ij* = 1 se *i*  =  *j* ou 0 caso contrário.  
</dl>

Em outras palavras, uma matriz de identidade contém 1 para cada elemento em que o número da linha é igual ao número da coluna e zero para todos os outros elementos. Por exemplo, aqui está a matriz de identidade 3 × 3.

![matriz de identidade.](images/matrix04.png)

As igualdades a seguir são ressaludas para qualquer matriz M.

<dl> M x I = M  
I x M = M  
</dl>

## <a name="affine-transforms"></a>Transformações de afinidade

Uma *transformação de afinidade é uma* operação matemática que mapeia um espaço de coordenadas para outro. Em outras palavras, ele mapeia um conjunto de pontos para outro conjunto de pontos. As transformação de afinidade têm alguns recursos que as torna úteis em gráficos de computador.

-   As transformaçãos de afinidade *preservam a collinearidade*. Se três ou mais pontos se enquadrarem em uma linha, eles ainda formarão uma linha após a transformação. As linhas retas permanecem retas.
-   A composição de duas transformaçãos affine é uma transformação affine.

As transformaçãos de afinidade para o espaço 2D têm o formulário a seguir.

![Mostra uma transformação de afinidade para o espaço 2D.](images/matrix05.png)

Se você aplicar a definição de multiplicação de matriz determinada anteriormente, poderá mostrar que o produto de duas transformaçãos afins é outra transformação afins. Para transformar um ponto 2D usando uma transformação de afinidade, o ponto é representado como uma matriz 1 × 3.

<dl> P = \| x y 1 \|  
</dl>

Os dois primeiros elementos contêm as coordenadas x e y do ponto. O 1 é colocado no terceiro elemento para fazer com que a matemática funcione corretamente. Para aplicar a transformação, multiplique as duas matrizes da seguinte maneira.

<dl> P' = P × M  
</dl>

Isso se expande para o seguinte.

![affine transform.](images/matrix06.png)

onde

<dl> x' = ax + cy + e  
y' = bx + dy + f  
</dl>

Para obter o ponto transformado, pegue os dois primeiros elementos da matriz P'.

<dl> p = (x', y') = (ax + cy + e, bx + dy + f)  
</dl>

> [!Note]  
> Uma matriz 1 × *n* é chamada de vetor *de linha*. Direct2D e Direct3D usam vetores de linha para representar pontos no espaço 2D ou 3D. Você pode obter um resultado equivalente usando um vetor de coluna (*n* × 1) e transpondo a matriz de transformação. A maioria dos textos gráficos usa o formulário de vetor de coluna. Este tópico apresenta o formulário de vetor de linha para consistência com Direct2D e Direct3D.

 

As próximas seções derivam as transformação básicas.

### <a name="translation-transform"></a>Transformação de tradução

A matriz de transformação de tradução tem o seguinte formato.

![transformação de tradução.](images/matrix07.png)

Conectar um ponto *P* a essa equação gera:

<dl> P' = (*x*  +  *dx*, *y*  +  *dy*)
</dl>

que corresponde ao ponto (x, y) traduzido por *dx* no eixo X e *dy* no eixo Y.

![um diagrama que mostra a tradução de dois pontos.](images/graphics22.png)

### <a name="scaling-transform"></a>Transformação de dimensionamento

A matriz de transformação de dimensionamento tem o seguinte formato.

![transformação de dimensionamento.](images/matrix09.png)

A conexão de um ponto *P* a esta equação resulta:

<dl> P ' = (*x* ∙ *DX*, *y* ∙ *DY*)
</dl>

que corresponde ao ponto (x, y) dimensionado por *DX* e *DY*.

![um diagrama que mostra o dimensionamento de dois pontos.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a>Rotação em volta da origem

A matriz para girar um ponto em volta da origem tem o seguinte formato.

![Mostra uma fórmula para uma transformação de rotação.](images/matrix11.png)

O ponto transformado é:

<dl> P ' = (*x* CosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)
</dl>

Gramatica. Para mostrar que P ' representa uma rotação, considere o diagrama a seguir.

![um diagrama que mostra a rotação em volta da origem.](images/graphics24.png)

Considerando:

<dl> <dt>

<span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x, y)
</dt> <dd>

O ponto original a ser transformado.

</dd> <dt>

Φ
</dt> <dd>

O ângulo formado pela linha (0, 0) a P.

</dd> <dt>

Θ
</dt> <dd>

O ângulo pelo qual girar (x, y) sobre a origem.

</dd> <dt>

<span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P ' = (x ', y ')
</dt> <dd>

O ponto transformado.

</dd> <dt>

<span id="R"></span><span id="r"></span>D
</dt> <dd>

O comprimento da linha (0, 0) a P. Também o raio do círculo de rotação.

</dd> </dl>

> [!Note]  
> Esse diagrama usa o sistema de coordenadas padrão usado em Geometry, onde o eixo y positivo aponta para cima. Direct2D usa o sistema de coordenadas Windows, em que o eixo y positivo aponta para baixo.

 

O ângulo entre o eixo x e a linha (0, 0) para P ' é Φ + Θ. As identidades a seguir contêm:

<dl> x = R cosΦ  
y = R sinΦ  
x ' = R cos (Φ + Θ)  
y ' = R sin (Φ + Θ)  
</dl>

Agora, resolva para x ' e y ' em termos de Θ. Pelas fórmulas de adição trigonométrica:

<dl> x ' = R (cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ  
y ' = R (sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ  
</dl>

Substituindo, obtemos:

<dl> x ' = xcosΘ – ysinΘ  
y ' = xsinΘ + ycosΘ  
</dl>

que corresponde ao ponto transformado P ' mostrado anteriormente.

### <a name="rotation-around-an-arbitrary-point"></a>Rotação em um ponto arbitrário

Para girar em um ponto (x, y) diferente da origem, a matriz a seguir é usada.

![transformação de rotação.](images/matrix13.png)

Você pode derivar essa matriz levando o ponto (x, y) para a origem.

![um diagrama que mostra a rotação em um ponto.](images/graphics25.png)

Let (x1, y1) é o ponto que resulta da rotação do ponto (x0, y0) ao contrário do ponto (x, y). Podemos derivar X1 da seguinte maneira.

<dl> X1 = (x0 – x) cosΘ – (y0 – y) sinΘ + x  
X1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]  
</dl>

Agora, conecte esta equação novamente à matriz de transformação, usando a fórmula X1 = aX0 + cy0 + e anterior. Use o mesmo procedimento para derivar Y1.

### <a name="skew-transform"></a>Transformação de distorção

A transformação de distorção é definida por quatro parâmetros:

-   Θ: o valor a ser distorcido ao longo do eixo x, medido como um ângulo do eixo y.
-   Φ: o valor a ser distorcido ao longo do eixo y, medido como um ângulo do eixo x.
-   (*PX*, *py*): as coordenadas x e y do ponto sobre o qual a distorção é executada.

A transformação de distorção usa a matriz a seguir.

![transformação de distorção.](images/matrix14.png)

O ponto transformado é:

<dl> P ' = (*x*  +  *y* tanΘ – *py* tanΘ, *y*  +  *x* tanΦ) – *py* tanΦ
</dl>

ou de maneira equivalente:

<dl> P ' = (*x* + (*y* – *py*) tanΘ, *y* + (*x* – *PX*) tanΦ)
</dl>

Para ver como essa transformação funciona, considere cada componente individualmente. O parâmetro Θ move todos os pontos na direção x por um valor igual a tanΘ. O diagrama a seguir mostra a relação entre Θ e a distorção do eixo x.

![Diagrama que mostra a inclinação ao longo do eixo x.](images/graphics26.png)

Aqui está a mesma distorção aplicada a um retângulo:

![Diagrama que mostra a inclinação ao longo do eixo x quando aplicado a um retângulo.](images/graphics27.png)

O parâmetro Φ tem o mesmo efeito, mas ao longo do eixo y:

![Diagrama que mostra a inclinação ao longo do eixo y.](images/graphics28.png)

O próximo diagrama mostra a inclinação do eixo y aplicada a um retângulo.

![Diagrama que mostra a inclinação ao longo do eixo y quando aplicado a um retângulo.](images/graphics29.png)

Por fim, os parâmetros *PX* e *py* alternam o ponto central para a distorção ao longo dos eixos x e y.

## <a name="representing-transforms-in-direct2d"></a>Representando transformações no Direct2D

todas as transformações de Direct2D são transformações afim. Direct2D não oferece suporte a transformações não afim. As transformações são representadas pela estrutura [**d2d1 \_ matriz \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) . Essa estrutura define uma matriz de 3 × 2. como a terceira coluna de uma transformação afim é sempre a mesma ( \[ 0, 0, 1 \] ) e como Direct2D não oferece suporte a transformações não-afim, não é necessário especificar a matriz 3 × 3 inteira. internamente, o Direct2D usa matrizes 3 × 3 para computar as transformações.

Os membros da [**matriz d2d1 \_ \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) são nomeados de acordo com sua posição de índice: o membro **\_ 11** é o elemento (1, 1), o membro **\_ 12** é o elemento (1, 2) e assim por diante. Embora você possa inicializar os membros da estrutura diretamente, é recomendável usar a classe [**d2d1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Essa classe herda o **d2d1 \_ Matrix \_ 3x2 \_ F** e fornece métodos auxiliares para a criação de qualquer uma das transformações de afinidade básicas. A classe também define o [**operador \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) para compor duas ou mais transformações, conforme descrito em [aplicando transformações no Direct2D](applying-transforms-in-direct2d.md).

## <a name="next"></a>Avançar

[Módulo 4. Entrada do usuário](module-4--user-input.md)

 

 