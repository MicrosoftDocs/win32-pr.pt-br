---
title: Efeitos (DirectComposition)
description: Este tópico discute os conceitos básicos dos efeitos DirectCompositions da Microsoft e descreve os tipos de efeitos aos quais o DirectComposition dá suporte.
ms.assetid: 805B17D2-2F6B-4C25-8C6D-41FFA5DFC774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cfd1ca154dcbc7e55ca65cc34d04cfa7d73ccee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366192"
---
# <a name="effects-directcomposition"></a>Efeitos (DirectComposition)

> [!NOTE]
> Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico discute os conceitos básicos dos efeitos DirectCompositions da Microsoft e descreve os tipos de efeitos aos quais o DirectComposition dá suporte.

Este tópico contém as seguintes seções:

-   [O que é um efeito de DirectComposition?](#what-is-a-directcomposition-effect)
-   [Opacidade](#opacity)
-   [efeitos de transformação de perspectiva 3D](#3d-perspective-transform-effects)
    -   [O espaço de coordenadas 3D do DirectComposition](#the-directcomposition-3d-coordinate-space)
    -   [efeito de transformação de rotação 3D](#3d-rotation-transform-effect)
    -   [efeito de transformação de dimensionamento 3D](#3d-scaling-transform-effect)
    -   [efeito de transformação de translação 3D](#3d-translation-transform-effect)
    -   [efeito de transformação de matriz 3D](#3d-matrix-transform-effect)
    -   [grupo de efeitos de transformação 3D](#3d-transform-effect-group)
-   [Objetos de efeito](#effect-objects)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-a-directcomposition-effect"></a>O que é um efeito de DirectComposition?

Um *efeito* DirectComposition é uma operação de bitmap que é aplicada durante a rasterização de um Visual para alterar a aparência do Visual de alguma forma.

O DirectComposition cria um efeito colocando uma subárvore visual e renderizando-a em um único bitmap antes de aplicar o efeito. Por exemplo, para criar um efeito de transformação de perspectiva 3D, DirectComposition produz uma imagem de uma subárvore visual e, em seguida, textura a imagem em um plano 3D que é transformado de acordo com a matriz resultante do efeito de transformação 3D.

O DirectComposition dá suporte aos seguintes tipos de efeitos.



| Tipo de efeito                                                   | Descrição                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------|
| [Opacidade](#opacity)                                           | Define a opacidade de um Visual inteiro.                                      |
| [transformação de perspectiva 3D](#3d-perspective-transform-effects) | Aplica um efeito de transformação de perspectiva tridimensional (3D) a um Visual. |



 

> [!Note]  
> O DirectComposition não faz nenhum processamento especial ao aplicar efeitos ao conteúdo estéreo 3D. Isso significa que o conteúdo 3D pode parecer distorcido quando um efeito é aplicado a ele.

 

## <a name="opacity"></a>Opacidade

O efeito de opacidade permite definir o fator de opacidade que é aplicado a um Visual inteiro quando o Visual é renderizado. Ele difere de uma máscara alfa, pois o mesmo fator de opacidade é aplicado a todos os pixels no Visual. A opacidade é especificada como um valor que varia de 0 (completamente transparente) para 1 (completamente opaco).

O fator de opacidade é aplicado de elementos visuais pai a filho, mas os efeitos visíveis das configurações de opacidade aninhadas não são indicados no valor da propriedade de visuais filho individuais. Por exemplo, se um visual raiz tiver uma opacidade de 50% (0,5) e um de seus filhos tiver uma opacidade de 20% (0,2), a opacidade líquida para esse filho será renderizada como 10% (0,1), mas o valor da propriedade de opacidade do filho ainda será 0,2.

## <a name="3d-perspective-transform-effects"></a>efeitos de transformação de perspectiva 3D

Esta seção descreve o espaço de coordenadas que o DirectComposition usa para executar efeitos de transformação de perspectiva 3D. Ele também descreve os tipos de efeitos de transformação de perspectiva 3D aos quais o DirectComposition dá suporte.

-   [O espaço de coordenadas 3D do DirectComposition](#the-directcomposition-3d-coordinate-space)
-   [efeito de transformação de rotação 3D](#3d-rotation-transform-effect)
-   [efeito de transformação de dimensionamento 3D](#3d-scaling-transform-effect)
-   [efeito de transformação de translação 3D](#3d-translation-transform-effect)
-   [efeito de transformação de matriz 3D](#3d-matrix-transform-effect)
-   [grupo de efeitos de transformação 3D](#3d-transform-effect-group)

> [!Note]  
> No DirectComposition, a aplicação de efeitos 3D a vários níveis na árvore visual não funciona da mesma maneira que faz com um mecanismo 3D completo, como o Microsoft Direct3D. Por exemplo, considere um visual pai que tenha um único Visual filho. Se o Visual filho for girado para frente na direção z (ao lado do eixo y) em 90 graus, a borda do Visual Edge filho enfrentaria o visualizador e, portanto, esperamos que o Visual não fique visível (porque um bitmap não tem profundidade real). Se o visual pai for girado para trás na direção z negativa (ao lado do eixo y) por 90 graus, poderemos esperar que o Visual filho se torne totalmente visivelmente (uma vez que as transformações são negadas entre si). No entanto, em DirectComposition, esse não é o caso. O Visual filho não será visível porque foi "mesclado" no bitmap pai.

 

### <a name="the-directcomposition-3d-coordinate-space"></a>O espaço de coordenadas 3D do DirectComposition

O espaço de coordenadas DirectComposition para efeitos de transformação 3D localiza a origem (0, 0, 0) no canto superior esquerdo da superfície do bitmap, com valores positivos do eixo x, prosseguindo para a direita, valores positivos do eixo y continuando para baixo e valores positivos do eixo z continuando para fora da origem, para o visualizador. Esta ilustração mostra o espaço de coordenadas 3D DirectComposition.

![espaço de coordenadas 3D directcompostion](images/3d-coordinate-space.png)

### <a name="3d-rotation-transform-effect"></a>efeito de transformação de rotação 3D

Um efeito de transformação de rotação 3D gira um Visual em três dimensões pelo ângulo especificado sobre um vetor de eixo \[ x, y, z \] localizado no ponto central especificado (x, y, z). O ângulo é especificado em graus. O vetor do eixo de rotação padrão é \[ 0, 0,-1 \] , e o ponto central padrão é (0, 0, 0).

Use o método [**IDCompositionDevice:: CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) para criar um objeto de transformação de rotação 3D. O método recupera uma interface [**IDCompositionRotateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d) que você pode usar para definir as propriedades do objeto.

### <a name="3d-scaling-transform-effect"></a>efeito de transformação de dimensionamento 3D

Um efeito de transformação de dimensionamento 3D torna um Visual maior ou menor. Ele dimensiona um Visual na \[ direção x, y, z \] sobre o ponto central (x, y, z). O ponto central padrão é (0, 0, 0).

Use o método [**IDCompositionDevice:: CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d) para criar um objeto de transformação de dimensionamento 3D. O método recupera uma interface [**IDCompositionScaleTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform3d) que você pode usar para definir as propriedades do objeto.

### <a name="3d-translation-transform-effect"></a>efeito de transformação de translação 3D

Um efeito de transformação de translação 3D altera a posição de um Visual na \[ direção x, y e z \] .

Use o método [**IDCompositionDevice:: CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d) para criar um objeto de transformação translação 3D. O método recupera uma interface [**IDCompositionTranslateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d) que você pode usar para definir as propriedades do objeto.

### <a name="3d-matrix-transform-effect"></a>efeito de transformação de matriz 3D

A interface [**IDCompositionMatrixTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) permite que você defina sua própria matriz de transformação 4 por 4 e a aplica a um Visual. Essa interface será útil se você precisar aplicar um tipo de efeito de transformação de perspectiva 3D que não está disponível por meio de outras interfaces de efeito de transformação 3D DirectComposition. Você define a matriz preenchendo uma estrutura [**D3DMATRIX**](/windows/desktop/direct3d10/d3d10-d3dmatrix) e passando-a para o método [**IDCompositionMatrixTransform3D:: setmatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) . Como alternativa, você pode definir cada elemento da matriz usando o método [**IDCompositionMatrixTransform3D:: Setmatrixelement**](/previous-versions/windows/desktop/legacy/hh437429(v=vs.85)) .

### <a name="3d-transform-effect-group"></a>grupo de efeitos de transformação 3D

O [**IDCompositionDevice:: CreateTransform3DGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransform3dgroup) cria uma coleção de efeitos de transformação 3D que você pode aplicar a um Visual como um grupo. A matriz pode incluir qualquer número de objetos Transform e pode incluir transformações de matriz, rotação, escala e conversão. A coleção de objetos de transformação 3D resulta em uma transformação cujo valor é a multiplicação de matriz das matrizes de transformação individuais na coleção.

A ordem das transformações individuais no grupo é importante. Por exemplo, girar, ajustar a escala e mover terá um resultado diferente de mover, girar e ajustar a escala. DirectComposition respeita a ordem na qual você especifica transformações 3D em um grupo 3D de transformação da mesma maneira que faz para transformações 2D. Além disso, as transformações de perspectiva 3D resultam no nivelamento da árvore visual após a aplicação de todas as transformações 3D no Visual atual. Isso é feito para garantir que a cena pareça o mais próximo possível do 3D.

## <a name="effect-objects"></a>Objetos de efeito

Para aplicar um efeito a um Visual, primeiro você precisa criar e definir as propriedades de um objeto de efeito que representa o tipo de efeito que você deseja produzir no Visual. Em seguida, você precisa aplicar o objeto Effect à Propriedade Effect do Visual.

Para criar um objeto de efeito, use um dos seguintes métodos de interface [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) para criar um objeto de efeito para o tipo de efeito desejado. Os métodos a seguir criam objetos de efeito:

-   [**CreateMatrixTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-creatematrixtransform3d)
-   [**CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d)
-   [**CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d)
-   [**CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d)

Cada um dos métodos anteriores recupera uma interface que você pode usar para definir as propriedades do objeto de efeito recém-criado. Use os métodos de interface para definir as propriedades conforme necessário para produzir o efeito visual desejado.

A maioria das propriedades de um objeto de efeito pode ser animada. Para animar uma determinada propriedade, crie um objeto de animação e aplique-o à propriedade que você deseja animar; caso contrário, defina a propriedade como um valor estático que produz o efeito desejado. Para obter mais informações sobre as propriedades de animação, consulte [animação](animation.md).

Para aplicar um objeto de efeito ao Visual, chame o método [**IDCompositionVisual:: seteffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) . Quando você aplica um efeito a um Visual, o efeito é aplicado a toda a subárvore visual com raiz nesse Visual. Portanto, por exemplo, se você definir a opacidade de um Visual como 50 por cento, a opacidade de todos os visuais filho na subárvore Visual será reduzida em 50%. Você pode aplicar o mesmo objeto de efeito a um ou mais visuais. Se você modificar as propriedades de um objeto de efeito depois de aplicá-lo a elementos visuais, todos os visuais serão recompostos para refletir a alteração.

Usando um objeto de grupo de efeitos, você pode aplicar simultaneamente vários efeitos a um Visual. Primeiro, chame [**IDCompositionDevice:: createeffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) para criar o objeto de grupo de efeitos e, em seguida, Adicione efeitos ao grupo usando a interface [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) do objeto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 