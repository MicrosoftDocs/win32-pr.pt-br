---
title: Transformações de matriz de apêndice
description: Este tópico fornece uma visão geral matemática das transformações de matriz para gráficos 2D.
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
# <a name="appendix-matrix-transforms"></a>Apêndice: transformações de matriz

Este tópico fornece uma visão geral matemática das transformações de matriz para gráficos 2D. No entanto, você não precisa conhecer a matriz Math para usar transformações em Direct2D. Leia este tópico se você estiver interessado na matemática; caso contrário, fique à vontade para ignorar este tópico.

-   [Introdução às matrizes](#introduction-to-matrices)
    -   [Operações de matriz](#matrix-operations)
-   [Transformações afim](#affine-transforms)
    -   [Transformação de tradução](#translation-transform)
    -   [Transformação de dimensionamento](#scaling-transform)
    -   [Rotação em volta da origem](#rotation-around-the-origin)
    -   [Rotação em um ponto arbitrário](#rotation-around-an-arbitrary-point)
    -   [Transformação de distorção](#skew-transform)
-   [Representando transformações no Direct2D](#representing-transforms-in-direct2d)
-   [Próximo](#next)

## <a name="introduction-to-matrices"></a>Introdução às matrizes

Uma matriz é uma matriz retangular de números reais. A *ordem* da matriz é o número de linhas e colunas. Por exemplo, se a matriz tiver 3 linhas e 2 colunas, a ordem será 3 × 2. As matrizes são geralmente mostradas com os elementos de matriz entre colchetes:

![matriz 3 x 2.](images/matrix01.png)

Notação: uma matriz é designada por uma letra maiúscula. Os elementos são designados por letras minúsculas. Subscritos indicam o número de linha e coluna de um elemento. Por exemplo, um *IJ* é o elemento na linha i'th e na coluna j'th da matriz a.

O diagrama a seguir mostra uma matriz i × j, com os elementos individuais em cada célula da matriz.

![uma matriz com i Rows e colunas j.](images/matrix15.png)

### <a name="matrix-operations"></a>Operações de matriz

Esta seção descreve as operações básicas definidas em matrizes.

*Adição*. A soma a + B de duas matrizes é obtida com a adição dos elementos correspondentes de A e B:

<dl> A + b = \[ a *IJ* \]  +  \[ B *IJ* \]  =  \[ a *IJ* + B *IJ*\]
</dl>

*Multiplicação escalar*. Esta operação multiplica uma matriz por um número real. Dado um número real *k*, o produto escalar ka é obtido multiplicando cada elemento de a por *k*.

<dl> Ka = k \[ a *IJ* \]  =  \[ k × a *IJ*\]
</dl>

*Multiplicação de matriz*. Dadas duas matrizes A e B com Order (m × n) e (n × p), o produto C = A × B é uma matriz com Order (m × p), definida da seguinte maneira:

![Mostra uma fórmula para multiplicação de matriz.](images/matrix02.png)

ou, de maneira equivalente:

<dl> c *IJ* = a *i* 1 x B1 *j* + a *i* 2 x B2 *j* +... + a *em* + b *NJ*  
</dl>

Ou seja, para computar cada elemento c *IJ*, faça o seguinte:

1.  Pegue a linha i'th de a e a coluna j'th de B.
2.  Multiplique cada par de elementos na linha e coluna: a primeira entrada de linha pela primeira entrada de coluna, a segunda entrada de linha pela segunda entrada de coluna e assim por diante.
3.  Some o resultado.

Aqui está um exemplo de multiplicação de uma matriz (2 × 2) por uma matriz (2 × 3).

![multiplicação de matriz.](images/matrix03.png)

A multiplicação de matriz não é comutada. Ou seja, A × B ≠ B × A. Além disso, da definição, ela segue que nem todos os pares de matrizes podem ser multiplicados. O número de colunas na matriz à esquerda deve ser igual ao número de linhas na matriz à direita. Caso contrário, o operador × não será definido.

*Identificar matriz*. Uma matriz de identidade, designada, é uma matriz quadrada definida da seguinte maneira:

<dl> Eu me *IJ* = 1 se *eu*  =  *j* ou 0 caso contrário.  
</dl>

Em outras palavras, uma matriz de identidade contém 1 para cada elemento em que o número da linha é igual ao número da coluna e zero para todos os outros elementos. Por exemplo, aqui está a matriz de identidade 3 × 3.

![matriz de identidade.](images/matrix04.png)

O equalities a seguir mantém a matriz M.

<dl> M x I = M  
X M = M  
</dl>

## <a name="affine-transforms"></a>Transformações afim

Uma *transformação afim* é uma operação matemática que mapeia um espaço de coordenadas para outro. Em outras palavras, ele mapeia um conjunto de pontos para outro conjunto de pontos. As transformações afim têm alguns recursos que os tornam úteis em gráficos de computador.

-   As transformações de afinidade preservam *Collinearity*. Se três ou mais pontos ficarem em uma linha, eles ainda formam uma linha após a transformação. Linhas retas permanecem retas.
-   A composição de duas transformações afim é uma transformação afim.

As transformações de afinidade para o espaço de 2 D têm o seguinte formato.

![Mostra uma transformação afim para o espaço de 2-D.](images/matrix05.png)

Se você aplicar a definição de multiplicação de matriz fornecida anteriormente, poderá mostrar que o produto de duas transformações afim é outra transformação afim. Para transformar um ponto 2D usando uma transformação afim, o ponto é representado como uma matriz 1 × 3.

<dl> P = \| x y 1 \|  
</dl>

Os dois primeiros elementos contêm as coordenadas x e y do ponto. O 1 é colocado no terceiro elemento para que o cálculo do seu trabalho seja feito corretamente. Para aplicar a transformação, multiplique as duas matrizes da seguinte maneira.

<dl> P ' = P × M  
</dl>

Isso se expande para o seguinte.

![a transformação afim.](images/matrix06.png)

onde

<dl> x ' = AX + Cy + e  
y ' = BX + DY + f  
</dl>

Para obter o ponto transformado, pegue os dois primeiros elementos da matriz P '.

<dl> p = (x ', y ') = (AX + Cy + e, BX + DY + f)  
</dl>

> [!Note]  
> Uma matriz 1 × *n* é chamada de *vetor de linha*. Direct2D e Direct3D usam vetores de linha para representar pontos em espaço 2d ou 3d. Você pode obter um resultado equivalente usando um vetor de coluna (*n* × 1) e transposando a matriz de transformação. A maioria dos textos de elementos gráficos usa o formulário de vetor de coluna. este tópico apresenta o formulário de vetor de linha para consistência com Direct2D e Direct3D.

 

As próximas várias seções derivam as transformações básicas.

### <a name="translation-transform"></a>Transformação de tradução

A matriz de transformação de tradução tem o seguinte formato.

![transformação de tradução.](images/matrix07.png)

A conexão de um ponto *P* a esta equação resulta:

<dl> P ' = (*x*  +  *DX*, *y*  +  *DY*)
</dl>

que corresponde ao ponto (x, y) traduzido pelo *DX* no eixo x e *DY* no eixo y.

![um diagrama que mostra a tradução de dois pontos.](images/graphics22.png)

### <a name="scaling-transform"></a>Transformação de dimensionamento

A matriz de transformação de dimensionamento tem o seguinte formato.

![transformação de dimensionamento.](images/matrix09.png)

Conectar um ponto *P* a essa equação gera:

<dl> P' = (*x* ∙ *dx*, *y* ∙ *dy*)
</dl>

que corresponde ao ponto (x,y) dimensionado por *dx* e *dy.*

![um diagrama que mostra o dimensionamento de dois pontos.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a>Rotação em torno da origem

A matriz para girar um ponto em torno da origem tem o seguinte formato.

![Mostra uma fórmula para uma transformação de rotação.](images/matrix11.png)

O ponto transformado é:

<dl> P' = (*x* cosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)
</dl>

Prova. Para mostrar que P' representa uma rotação, considere o diagrama a seguir.

![um diagrama que mostra a rotação em torno da origem.](images/graphics24.png)

Considerando:

<dl> <dt>

<span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x,y)
</dt> <dd>

O ponto original a transformar.

</dd> <dt>

Φ
</dt> <dd>

O ângulo formado pela linha (0,0) para P.

</dd> <dt>

Θ
</dt> <dd>

O ângulo pelo qual girar (x,y) sobre a origem.

</dd> <dt>

<span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x',y')
</dt> <dd>

O ponto transformado.

</dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

O comprimento da linha (0,0) para P. Além disso, o raio do círculo de rotação.

</dd> </dl>

> [!Note]  
> Este diagrama usa o sistema de coordenadas padrão usado em geometria, em que o eixo y positivo aponta para cima. Direct2D usa o Windows de coordenadas, em que o eixo y positivo aponta para baixo.

 

O ângulo entre o eixo x e a linha (0,0) para P' é A + Θ. As seguintes identidades são resdados:

<dl> x = R cosA  
y = R sinA  
x' = R cos(Θ + Θ)  
y' = R sin(Θ+ Θ)  
</dl>

Agora, resolva x' e y' em termos de Θ. Pelas fórmulas de adição trigonométrica:

<dl> x' = R(cosScosΘ – sinΘsinΘ) = RcosOcosS – Rsin A  
y' = R(sin AcosS + cosSinΘ) = Rsin AcosS + RcosSin A  
</dl>

Substituindo, podemos obter:

<dl> x' = xcosΘ – ysinΘ  
y' = xsinΘ + ycosO  
</dl>

que corresponde ao ponto transformado P' mostrado anteriormente.

### <a name="rotation-around-an-arbitrary-point"></a>Rotação em torno de um ponto arbitrário

Para girar em torno de um ponto (x,y) diferente da origem, a matriz a seguir é usada.

![transformação de rotação.](images/matrix13.png)

Você pode derivar essa matriz levando o ponto (x,y) para ser a origem.

![um diagrama que mostra a rotação em torno de um ponto.](images/graphics25.png)

Let (x1, y1) é o ponto que resulta da rotação do ponto (x0, y0) ao redor do ponto (x,y). Podemos derivar x1 da seguinte forma.

<dl> x1 = (x0 – x)cosΘ– (y0 – y)sinΘ + x  
x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]  
</dl>

Agora, conecte essa equação de volta à matriz de transformação, usando a fórmula x1 = ax0 + cy0 + e de anterior. Use o mesmo procedimento para derivar y1.

### <a name="skew-transform"></a>Transformação distorção

A transformação de distorção é definida por quatro parâmetros:

-   Θ: a quantidade a ser distorcida ao longo do eixo x, medida como um ângulo do eixo y.
-   ª: a quantidade a ser distorcida ao longo do eixo y, medida como um ângulo do eixo x.
-   (*px*, *py*): as coordenadas x e y do ponto sobre o qual a distorção é executada.

A transformação de distorção usa a matriz a seguir.

![distorção de transformação.](images/matrix14.png)

O ponto transformado é:

<dl> P' = (*x*  +  *y* tanΘ – *py* tanΘ, *y*  +  *x* tanA) – *py* tanA
</dl>

ou de forma equivalente:

<dl> P' = (*x* + (*y* – *py*)tanΘ, *y* + (*x* – *px*)tanA)
</dl>

Para ver como essa transformação funciona, considere cada componente individualmente. O parâmetro Θ move cada ponto na direção x por um valor igual a tanE. O diagrama a seguir mostra a relação entre Θ e a distorção do eixo x.

![Diagrama que mostra distorção ao longo do eixo x.](images/graphics26.png)

Aqui está a mesma distorção aplicada a um retângulo:

![Diagrama que mostra distorção ao longo do eixo x quando aplicado a um retângulo.](images/graphics27.png)

O parâmetro ª tem o mesmo efeito, mas ao longo do eixo y:

![Diagrama que mostra distorção ao longo do eixo y.](images/graphics28.png)

O diagrama a seguir mostra a distorção do eixo y aplicada a um retângulo.

![Diagrama que mostra distorção ao longo do eixo y quando aplicado a um retângulo.](images/graphics29.png)

Por fim, os parâmetros *px* e *py* deslocam o ponto central para a distorção ao longo dos eixos x e y.

## <a name="representing-transforms-in-direct2d"></a>Representando as transformação em Direct2D

Todas as Direct2D são transformações affine. Direct2D não dá suporte a transformação não affine. As transformaçãos são representadas pela [**estrutura D2D1 \_ MATRIX \_ 3X2 \_ F.**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) Essa estrutura define uma matriz 3 × 2. Como a terceira coluna de uma transformação de afinidade é sempre a mesma ( 0, 0, 1 ) e como o Direct2D não dá suporte a transformação não affine, não é necessário especificar toda a \[ \] matriz 3 × 3. Internamente, Direct2D usa três × três matrizes para calcular as transformaçãos.

Os membros do [**D2D1 \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) são nomeados de acordo com sua posição de índice: **\_ o membro 11** é elemento (1,1), **\_ o 12** membro é elemento (1,2) e assim por diante. Embora você possa inicializar os membros da estrutura diretamente, é recomendável usar a classe [**D2D1::Matrix3x2F.**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) Essa classe herda **D2D1 \_ MATRIX \_ 3X2 \_ F** e fornece métodos auxiliares para criar qualquer uma das transformaçãos de afinidade básicas. A classe também define [**o operador \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) para compor duas ou mais transformaçãos, conforme descrito em [Aplicando transformes em Direct2D](applying-transforms-in-direct2d.md).

## <a name="next"></a>Avançar

[Módulo 4. Entrada do usuário](module-4--user-input.md)

 

 