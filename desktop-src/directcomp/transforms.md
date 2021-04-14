---
title: Transformações (DirectComposition)
description: Este tópico discute o suporte do Microsoft DirectComposition para transformações de afinidade (linear) bidimensionais e descreve os tipos de transformações com suporte do DirectComposition.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27a1fec5774d208f240e6d2f1c8b7df09d25c486
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104555467"
---
# <a name="transforms-directcomposition"></a>Transformações (DirectComposition)

> [!NOTE]
> Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico discute o suporte do Microsoft DirectComposition para transformações de afinidade (linear) bidimensionais e descreve os tipos de transformações com suporte do DirectComposition.

O DirectComposition também dá suporte a transformações de perspectiva 3D, mas, como elas exigem a criação de um bitmap intermediário, o DirectComposition considera que eles são efeitos em vez de transformações. Para obter informações sobre efeitos de transformação de perspectiva 3D, consulte [efeitos](effects.md).

Este tópico inclui as seções a seguir:

-   [O que é uma transformação 2D DirectComposition?](#what-is-a-directcomposition-2d-transform)
-   [O espaço de coordenadas 2D DirectComposition](#the-directcomposition-2d-coordinate-space)
-   [Suporte para transformações 2D afim](#support-for-affine-2d-transforms)
-   [Transformações 2D da matriz](#matrix-2d-transforms)
-   [Transformar grupos](#transform-groups)
-   [Transformar animação](#transform-animation)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a>O que é uma transformação 2D DirectComposition?

Uma transformação 2D permite que você altere a posição, o tamanho ou a natureza de um Visual em duas dimensões movendo o Visual para outro local (tradução), tornando-o maior ou menor (dimensionando), virando-o (rotação) ou distorcendo sua forma (distorção).

Uma transformação 2D é obtida mapeando os pontos de um Visual de uma posição para outra dentro do mesmo espaço de coordenadas ou de um espaço de coordenadas para outro. Esse mapeamento é descrito por uma tabela de valores chamada matriz de transformação, definida como uma coleção de três linhas com três colunas de valores de ponto flutuante, conforme mostrado na tabela a seguir.



|                 |                 |     |
|-----------------|-----------------|-----|
| M11Default: 1,0 | M12Default: 0,0 | 0.0 |
| M21Default: 0,0 | M22Default: 1,0 | 0.0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 | 1,0 |



 

A matriz de transformação para transformações 2D afim é uma matriz 3-por-2 que omite a terceira coluna da matriz de transformação anterior. A tabela a seguir mostra o layout desta matriz.



|                 |                 |
|-----------------|-----------------|
| M11Default: 1,0 | M12Default: 0,0 |
| M21Default: 0,0 | M22Default: 1,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 |



 

> [!Note]  
> O DirectComposition não faz nenhum processamento especial ao aplicar transformações 2D ao conteúdo estéreo. Isso significa que o conteúdo 3D pode parecer distorcido quando uma transformação 2D é aplicada a ele.

 

## <a name="the-directcomposition-2d-coordinate-space"></a>O espaço de coordenadas 2D DirectComposition

DirectComposition usa um espaço de coordenadas 2D de mão esquerda; ou seja, os valores positivos do eixo x aumentam para a direita e os valores positivos do eixo y aumentam para baixo. Os visuais são posicionados em relação à origem, que é o ponto em que o eixo x e o eixo y interseccionam (0,0), conforme mostrado na ilustração a seguir.

![o eixo x e eixo y de um espaço de coordenadas da mão esquerda](images/coordinatespace.png)

Ao manipular valores em uma matriz de transformação 3-by-2, você pode girar, dimensionar, inclinar e traduzir um objeto em duas dimensões. Por exemplo, se você definir OffsetX como 100 e OffsetY como 200, moverá o objeto para a direita de 100 pixels e para baixo em 200 pixels.

## <a name="support-for-affine-2d-transforms"></a>Suporte para transformações 2D afim

A tabela a seguir descreve os tipos de transformações 2D afim com suporte do DirectComposition e lista as interfaces que você pode usar para executar os vários tipos de transformações.



| Transformação/interface                                                                               | Descrição                                                                                              | Ilustração                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Girar[](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[ nova linha idcompositionrotatetransform 2D\]          | girar um Visual pelo ângulo especificado sobre o ponto central especificado.                                 | ![ilustração de um quadrado girado em 45 graus no sentido horário sobre o centro do quadrado original](images/rotate.png)               |
| Dimensionar nova linha de [**Idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)2D \[\]             | dimensionar um Visual pelo fator especificado sobre o ponto central especificado.                                 | ![ilustração de um percentual de escala em quadrado de 130%](images/scale.png)                                                                  |
| Distorcer linha de [**Idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)2D \[\]                | distorcer um Visual pelo ângulo especificado ao longo do eixo x e eixo y e ao lado do ponto central especificado. | ![ilustração de um quadrado inclinado em 30 graus no sentido anti-horário do eixo y](images/skew.png)                                   |
| Traduzir nova linha de [**Idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)2D \[\] | Altere a posição de um Visual na direção do eixo x e eixo y.                               | ![ilustração de um quadrado moveu 20 unidades ao longo do eixo x positivo e 10 unidades ao longo do eixo y positivo](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a>Transformações 2D da matriz

A interface [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) permite que você defina sua própria matriz de transformação 2D afim 3 por 2 e a aplica a um Visual. Essa interface será útil se você precisar aplicar um tipo de transformação 2D afim que não esteja disponível por meio de outras interfaces de transformação DirectComposition. Você define a matriz preenchendo uma estrutura [**D2D \_ matriz \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) e passando-a para o método [**IDCompositionMatrixTransform:: setmatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) .

## <a name="transform-groups"></a>Transformar grupos

Você pode usar grupos de transformação para combinar várias transformações em uma. Um grupo de transformação define uma coleção de objetos de transformação cujas matrizes são multiplicadas em conjunto na ordem em que são especificadas na coleção. A matriz de transformação resultante é então aplicada ao Visual. Um grupo de transformação produz o mesmo resultado que aplicar cada transformação separadamente.

Tenha em mente que a ordem dos objetos de transformação em um grupo de transformação é importante. Por exemplo, se um Visual for girado primeiro, em escala e, em seguida, traduzido, o resultado será diferente de se o Visual for convertido primeiro, então girado e então dimensionado. DirectComposition sempre aplica as transformações a um Visual na ordem em que elas são especificadas na coleção.

Para criar um grupo de transformação, primeiro crie os objetos de transformação que você deseja incluir no grupo e, em seguida, passe uma matriz de ponteiros de objeto de transformação para o método [**IDCompositionDevice:: CreateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) . Depois de criar um grupo de transformação, você não pode adicionar ou remover objetos de transformação. No entanto, você pode modificar as propriedades dos objetos de transformação individuais na coleção e as alterações serão refletidas na matriz de transformação resultante.

## <a name="transform-animation"></a>Transformar animação

As propriedades de uma transformação podem ser animadas. Quando uma propriedade é animada, DirectComposition altera o valor da propriedade ao longo do tempo, em vez de tudo de uma só vez. Isso é particularmente útil ao criar transições. Para obter mais informações, consulte [animação](animation.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
