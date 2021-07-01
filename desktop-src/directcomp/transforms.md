---
title: Transforms (DirectComposition)
description: Este tópico discute o suporte do Microsoft DirectComposition para transformaçãos de afinidade (linear) bidimensionais e descreve os tipos de transformação aos quais o DirectComposition dá suporte.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991e1205422864efdec82bbd4067b9c7662aaf29
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118651"
---
# <a name="transforms-directcomposition"></a>Transforms (DirectComposition)

> [!NOTE]
> Para aplicativos Windows 10, é recomendável usar APIs Windows.UI.Composition em vez de DirectComposition. Para obter mais informações, consulte [Modernizar seu aplicativo da área de trabalho usando a camada visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico discute o suporte do Microsoft DirectComposition para transformaçãos de afinidade (linear) bidimensionais e descreve os tipos de transformação aos quais o DirectComposition dá suporte.

DirectComposition também dá suporte a transformaçãos de perspectiva 3D, mas como elas exigem a criação de um bitmap intermediário, DirectComposition as considera como efeitos em vez de transformaçãos. Para obter informações sobre efeitos de transformação de perspectiva 3D, consulte [Efeitos](effects.md).

Este tópico inclui as seções a seguir:

-   [O que é uma transformação DirectComposition 2D?](#what-is-a-directcomposition-2d-transform)
-   [O espaço de coordenadas 2D do DirectComposition](#the-directcomposition-2d-coordinate-space)
-   [Suporte para transformar 2D affine](#support-for-affine-2d-transforms)
-   [Transformaçãos de Matriz 2D](#matrix-2d-transforms)
-   [Transformar grupos](#transform-groups)
-   [Transformar animação](#transform-animation)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a>O que é uma transformação DirectComposition 2D?

Uma transformação 2D permite alterar a posição, o tamanho ou a natureza de um visual em duas dimensões movendo o visual para outro local (tradução), tornando-o maior ou menor (dimensionamento), transformando-o (rotação) ou distorcendo sua forma (distorção).

Uma transformação 2D é feita mapeando os pontos de um visual de uma posição para outra dentro do mesmo espaço de coordenadas ou de um espaço de coordenadas para outro. Esse mapeamento é descrito por uma tabela de valores chamada matriz de transformação, definida como uma coleção de três linhas com três colunas de valores de ponto flutuante, conforme mostrado na tabela a seguir.

:::row:::
    :::column:::
        M11Default: 1.0<br/>
        M21Default: 0.0<br/>
        M31OffsetX: 0.0
    :::column-end:::
    :::column:::
        M12Default: 0.0<br/>
        M22Default: 1.0<br/>
        M32OffsetY: 0.0
    :::column-end:::
    :::column:::
        0,0<br/>
        0,0<br/>
        1,0
    :::column-end:::
:::row-end:::

A matriz de transformação para transformações 2D de afinidade é uma matriz 3 por 2 que omite a terceira coluna da matriz de transformação anterior. A tabela a seguir mostra o layout dessa matriz.

:::row:::
    :::column:::
        M11Default: 1.0<br/>
        M21Default: 0.0<br/>
        M31OffsetX: 0.0
    :::column-end:::
    :::column:::
        M12Default: 0.0<br/>
        M22Default: 1.0<br/>
        M32OffsetY: 0.0
    :::column-end:::
:::row-end:::

> [!Note]  
> DirectComposition não faz nenhum processamento especial ao aplicar as transformaçãos 2D ao conteúdo estéreo. Isso significa que o conteúdo 3D pode parecer distorcido quando uma transformação 2D é aplicada a ele.

 

## <a name="the-directcomposition-2d-coordinate-space"></a>O espaço de coordenadas 2D do DirectComposition

DirectComposition usa um espaço de coordenadas 2D à esquerda; ou seja, os valores positivos do eixo x aumentam para a direita e os valores positivos do eixo y aumentam para baixo. Os visuais são posicionados em relação à origem, que é o ponto em que o eixo x e o eixo y interseccionam (0, 0), conforme mostrado na ilustração a seguir.

![o eixo x e o eixo y de um espaço de coordenadas à esquerda](images/coordinatespace.png)

Manipulando valores em uma matriz de transformação 3 por 2, você pode girar, dimensionar, distorcer e converter um objeto em duas dimensões. Por exemplo, se você definir OffsetX como 100 e OffsetY como 200, mova o objeto para a direita 100 pixels e 200 pixels para baixo.

## <a name="support-for-affine-2d-transforms"></a>Suporte para transformar 2D affine

A tabela a seguir descreve os tipos de transformações 2D affine com suporte pelo DirectComposition e lista as interfaces que você pode usar para executar os vários tipos de transformações.



| Transformar/interface                                                                               | Descrição                                                                                              | Ilustração                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Girar [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)newline 2D \[\]          | girar um visual pelo ângulo especificado sobre o ponto central especificado.                                 | ![ilustração de um quadrado girado 45 graus no sentido horário sobre o centro do quadrado original](images/rotate.png)               |
| Dimensionar [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform) \[ newline\]             | dimensionar um visual pelo fator especificado sobre o ponto central especificado.                                 | ![ilustração de um quadrado dimensionado em 130%](images/scale.png)                                                                  |
| Distorcer [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)newline 2D \[\]                | distorce um visual pelo ângulo especificado ao longo do eixo x e do eixo y e ao redor do ponto central especificado. | ![ilustração de um quadrado distorceu 30 graus no sentido anti-horário do eixo y](images/skew.png)                                   |
| Traduzir [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)newline 2D \[\] | altere a posição de um visual na direção do eixo x e eixo y.                               | ![ilustração de um quadrado movido 20 unidades ao longo do eixo x positivo e 10 unidades ao longo do eixo y positivo](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a>Transformaçãos de Matriz 2D

A interface [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) permite que você defina sua própria matriz de transformação 2D de afinidade 3 por 2 e aplicá-la a um visual. Essa interface será útil se você precisar aplicar um tipo de transformação 2D affine que não está disponível por meio de outras interfaces de transformação DirectComposition. Defina a matriz preenchendo uma estrutura [**D2D \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) e passando-a para o [**método IDCompositionMatrixTransform::SetMatrix.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix)

## <a name="transform-groups"></a>Transformar grupos

Você pode usar transformar grupos para combinar várias transformaçãos em uma. Um grupo de transformação define uma coleção de objetos de transformação cujas matrizes são multiplicadas juntas na ordem em que são especificadas na coleção. A matriz de transformação resultante é aplicada ao visual. Um grupo de transformação produz o mesmo resultado que aplicar cada transformação separadamente.

Tenha em mente que a ordem dos objetos de transformação em um grupo de transformação é importante. Por exemplo, se um visual for girado primeiro, depois dimensionado e, em seguida, convertido, o resultado será diferente de se o visual for convertido pela primeira vez, depois girado e, em seguida, dimensionado. DirectComposition sempre aplica as transformação a um visual na ordem em que elas são especificadas na coleção.

Para criar um grupo de transformação, primeiro crie os objetos de transformação que você deseja incluir no grupo e, em seguida, passe uma matriz de ponteiros de objeto de transformação para o método [**IDCompositionDevice::CreateTransformGroup.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) Depois de criar um grupo de transformação, você não pode adicionar ou remover nenhum objeto de transformação. No entanto, você pode modificar as propriedades dos objetos de transformação individuais na coleção e as alterações serão refletidas na matriz de transformação resultante.

## <a name="transform-animation"></a>Transformar animação

As propriedades de uma transformação podem ser animadas. Quando uma propriedade é animada, DirectComposition altera o valor da propriedade ao longo do tempo, em vez de tudo de uma vez. Isso é particularmente útil ao criar transições. Para obter mais informações, consulte [Animação](animation.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
