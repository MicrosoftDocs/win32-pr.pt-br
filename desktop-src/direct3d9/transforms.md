---
description: A parte do Direct3D que leva a geometria através do pipeline de geometria de funções fixas é o mecanismo de transformação.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Transforms (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5570562c02f2283b869bbb5e60143ed4badac94eb10651b002a89aedf1cd60f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519659"
---
# <a name="transforms-direct3d-9"></a>Transforms (Direct3D 9)

A parte do Direct3D que leva a geometria através do pipeline de geometria de funções fixas é o mecanismo de transformação. Ele localiza o modelo e o visualizador do mundo, projeta vértices para a exibição na tela e corta os vértices no visor. O mecanismo de transformação também executa cálculos de iluminação para determinar os componentes difusos e especulares em cada vértice.

O pipeline de geometria leva vértices como entrada. O mecanismo de transformação aplica as transformações do mundo, modo de exibição e projeção para os vértices, recorta o resultado e passa tudo para o rasterizador.

No topo do pipeline, os vértices de um modelo são declarados em relação a um sistema de coordenadas local. Isso é uma origem local e uma orientação. Essa orientação de coordenadas geralmente é conhecida como espaço de modelo e coordenadas individuais são chamadas de coordenadas de modelo.

O primeiro estágio do pipeline de geometria transforma os vértices de um modelo de seu sistema de coordenadas local em um sistema de coordenadas usado por todos os objetos em uma cena. O processo de reorientação dos vértices é chamado de transformação do mundo. Essa nova orientação é normalmente conhecida como espaço do mundo e cada vértice no espaço do mundo é declarado usando coordenadas do mundo.

No próximo estágio, os vértices que descrevem o mundo 3D são orientados com relação a uma câmera. Ou seja, seu aplicativo escolhe um ponto de exibição para a cena e as coordenadas de espaço do mundo são realocadas e giradas em torno da exibição da câmera, transformando o espaço do mundo no espaço da câmera. Essa é a transformação de exibição.

O próximo estágio é a transformação de projeção. Nesta parte do pipeline, os objetos geralmente são dimensionados com relação à distância do visualizador para dar a ilusão de profundidade a uma cena; Objetos close são feitos para aparecerem maiores do que objetos distantes e assim por diante. Para fins de simplicidade, esta documentação refere-se ao espaço no qual os vértices existem após a transformação de projeção como espaço de projeção. Alguns livros de elementos gráficos podem se referir ao espaço de projeção como espaço homogêneo de pós-perspectiva. Nem todas as transformações de projeção dimensionam o tamanho dos objetos em uma cena. Uma projeção como essa às vezes é chamada de um afim ou projeção ortogonal.

Na parte final do pipeline, qualquer vértice que não ficará visível na tela é removido, para que o rasterizador não reserve um tempo para calcular as cores e o sombreamento para algo que jamais será visto. Esse processo é denominado recorte. Depois de recorte, os vértices restantes são dimensionados de acordo com os parâmetros do visor e convertidos em coordenadas da tela. Os vértices resultantes, vistos na tela quando a cena é rasterizada, existem no espaço de tela.

As transformações são usadas para converter a geometria de objeto de um espaço de coordenadas em outro. O Direct3D usa matrizes para realizar transformações 3D. Esta seção explica como as matrizes criam transformaçãos 3D, descreve alguns usos comuns para transformar e detalha como você pode combinar matrizes para produzir uma única matriz que abrange várias transformares.

-   [Transformação Mundo (Direct3D 9) –](world-transform.md) converter do espaço do modelo para o espaço do mundo
-   [Transformação de Exibição (Direct3D 9) –](view-transform.md) converter do espaço do mundo para exibir o espaço
-   [Transformação projeção (Direct3D 9) –](projection-transform.md) converter do espaço de exibição para o espaço de projeção

## <a name="matrix-transforms"></a>Transformações de matriz

Em aplicativos que trabalham com elementos gráficos 3D, você pode usar transformações geométricas para fazer o seguinte:

-   Expressar a localização de um objeto em relação a outro objeto.
-   Rotacionar e dimensionar objetos
-   Alterar as posições de visualização, trajetos e perspectivas.

Você pode transformar qualquer ponto (x, y, z) em outro ponto (x', y', z'), usando uma matriz 4x4, conforme mostrado na seguinte equação.

![equação para transformar qualquer ponto em outro ponto](images/matmult.png)

Execute as seguintes equações em (x, y, z) e na matriz para produzir o ponto (x', y', z').

![equações para o novo ponto](images/matexpnd.png)

As transformações mais comuns são conversão, rotação e dimensionamento. Você pode combinar as matrizes que produzem esses efeitos em uma única matriz para calcular várias transformações ao mesmo tempo. Por exemplo, você pode criar uma matriz única para traduzir e girar uma série de pontos.

Matrizes são escritas na ordem das colunas de linha. Uma matriz que dimensiona uniformemente os vértices em cada eixo, conhecida como dimensionamento uniforme, é representada pela matriz de seguir usando a notação matemática.

![equação de uma matriz de dimensionamento uniforme](images/matrix.png)

No C++, o Direct3D declara matrizes como uma matriz bidimensional, usando a [**estrutura D3DMATRIX.**](d3dmatrix.md) O exemplo a seguir mostra como inicializar uma **estrutura D3DMATRIX** para atuar como uma matriz de dimensionamento uniforme.


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a>Translate

A seguinte equação traduz o ponto (x, y, z) para um novo ponto (x', y', z').

![equação de uma matriz de translação para um novo ponto](images/transl8.png)

Você pode criar manualmente uma matriz de translação em C++. O exemplo a seguir mostra o código-fonte para uma função que cria uma matriz para traduzir vértices.


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



Para sua conveniência, a biblioteca do utilitário D3DX fornece a [**função D3DXMatrixTranslation.**](d3dxmatrixtranslation.md)

## <a name="scale"></a>Escala

A seguinte equação dimensiona o ponto (x, y, z) por valores arbitrários nas direções x, y e z para um novo ponto (x', y', z').

![equação de uma matriz de escala para um novo ponto](images/matscale.png)

## <a name="rotate"></a>Rotate

As transformações descritas aqui destinam-se aos sistemas de coordenadas à esquerda e, portanto, podem ser diferentes das matrizes de transformação que você já viu em outro lugar.

A seguinte equação rotaciona o ponto (x, y, z) em torno do eixo x, produzindo um novo ponto (x', y', z').

![equação de uma matriz de rotação x para um novo ponto](images/matxrot.png)

A seguinte equação gira o ponto em torno do eixo y.

![equação de uma matriz de rotação y para um novo ponto](images/matyrot.png)

A seguinte equação gira o ponto em torno do eixo z.

![equação de uma matriz de rotação z para um novo ponto](images/matzrot.png)

Nessas matrizes de exemplo, a letra grega "teta" significa o ângulo de rotação, em radianos. Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.

Em um aplicativo C++, use as funções [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)e [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) fornecidas pela biblioteca do utilitário D3DX para criar matrizes de rotação. A seguir está o código para a **função D3DXMatrixRotationX.**


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a>Concatenação de matrizes

Uma vantagem de usar matrizes é que você pode combinar os efeitos de duas ou mais matrizes multiplicando-as. Isso significa que, para girar um modelo e, em seguida, convertê-lo em um local, você não precisa aplicar duas matrizes. Em vez disso, multiplique as matrizes de rotação e conversão para produzir uma matriz de composição que contém todos os seus efeitos. Esse processo, chamado de concatenação de matriz, pode ser escrito com a seguinte equação.

![equação da concatenação de matriz](images/matrxcat.png)

Nesta equação, C é a matriz de composição que está sendo criada e M₁ por Mₙ são as matrizes individuais. Na maioria dos casos, apenas duas ou três matrizes são concatenadas, mas não há nenhum limite.

Use a [**função D3DXMatrixMultiply**](d3dxmatrixmultiply.md) para executar a multiplicação de matriz.

A ordem em que a multiplicação da matriz é realizada é essencial. A fórmula anterior reflete a regra da esquerda para a direita da concatenação de matriz. Ou seja, os efeitos visíveis das matrizes que você usa para criar uma matriz composta ocorrem na ordem da esquerda para a direita. Uma matriz de mundo típica é mostrada no exemplo a seguir. Imagine que você está criando a matriz do mundo para um disco voador estereotipado. Provavelmente, você desejaria girar o disco voador em torno de seu centro - eixo y do espaço de modelo - e levá-lo para algum outro local em sua cena. Para realizar esse efeito, você primeiro cria uma matriz de rotação e, em seguida, multiplica ela pela matriz de translação, conforme mostrado na seguinte equação.

![equação de rotação com base em uma matriz de rotação e uma matriz de translação](images/wrldexpl.png)

Nessa fórmula, R<sub>y</sub> é uma matriz de rotação sobre o eixo y e T<sub>w</sub> é uma translação para alguma posição nas coordenadas do mundo.

A ordem na qual você multiplica as matrizes é importante porque, ao contrário da multiplicação de dois valores escalares, a multiplicação de matrizes não é comutativa. Multiplicar as matrizes na ordem oposta tem o efeito visual de levar o disco voador para a sua posição do espaço de mundo e, em seguida, girando-o em torno da origem do mundo.

Não importa qual tipo de matriz você está criando, lembre-se da regra da esquerda para a direita para garantir que você obterá os efeitos esperados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> </dl>

 

 



