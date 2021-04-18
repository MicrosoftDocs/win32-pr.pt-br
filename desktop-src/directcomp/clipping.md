---
title: Recorte (DirectComposition)
description: Este tópico descreve o suporte do Microsoft DirectComposition para elementos visuais de recorte.
ms.assetid: B6E0D8F5-B6B9-40CC-B079-850AC8F2D538
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4feb537dfb41053dd1099eca7f122b3284dce95
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369184"
---
# <a name="clipping-directcomposition"></a>Recorte (DirectComposition)

> [!NOTE]
> Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

O recorte fornece uma maneira de revelar apenas uma parte de uma árvore visual ou Visual limitando a renderização do Visual ou da árvore a uma área retangular específica. Este tópico descreve o suporte do Microsoft DirectComposition para elementos visuais de recorte. Ele inclui as seguintes seções:

-   [Retângulo do clipe](#clip-rectangle)
-   [Objeto de clipe](#clip-object)
-   [Retângulo de clipe animado](#animated-clip-rectangle)
-   [Tópicos relacionados](#related-topics)

## <a name="clip-rectangle"></a>Retângulo do clipe

Um objeto visual tem uma propriedade clip que define uma região retangular, ou um *retângulo*, dentro do conteúdo de bitmap do Visual. Quando o Visual é renderizado para a tela, somente a parte do conteúdo do bitmap que está dentro do retângulo é desenhada na tela, enquanto o conteúdo que se estende para fora do retângulo é recortado (não desenhado). Por padrão, a propriedade Clip inclui todo o conteúdo do bitmap.

A propriedade de clipe do Visual aplica-se a todos os visuais filho e descendentes. Em outras palavras, qualquer conteúdo filho ou descendente que esteja fora dos limites do retângulo do clipe pai também será recortado.

DirectComposition aplica a propriedade Clip antes de aplicar as propriedades de transformação OffsetX, OffsetY e 2D, mas depois de aplicar as propriedades Effect e Transform 3D. Isso significa que as transformações 2D, OffsetX e OffsetY, afetarão o conteúdo visual e o retângulo. Enquanto as transformações e os efeitos 3D não se aplicarão ao retângulo do clipe.

Por exemplo, ao aplicar uma transformação offset ou 2D, o clipe retângulo é afetado pela matriz de transformação. Portanto, adicionar um deslocamento e uma rotação 2D (45 graus), juntamente com um retângulo de canto arredondado, resultará em:

![diagrama de mostrar o efeito de uma transformação 2D em um retângulo.](images/clipping2dtransform.png)

Ao aplicar uma transformação 3D "no" retângulo do clipe, o retângulo do clipe não é afetado pela matriz de transformação. Mesmo ao aplicar uma rotação em todo o eixo Z (efetivamente igual ao exemplo anterior), o seguinte diagrama é o resultado:

![diagrama mostrando que uma transformação 3D não afeta o clipe de retângulo (gira o Visual no clipe).](images/clipping3dtransform.png)

Observe que o Visual girado no clipe porque a matriz 3D não é aplicada ao próprio clipe.

Se a propriedade Clip for definida como um retângulo vazio, o Visual será completamente recortado; ou seja, o Visual é incluído na árvore visual, mas não processa nada. Se você não quiser incluir um Visual específico em uma composição, remova o Visual da árvore visual em vez de definir um retângulo de clipe vazio. Remover os resultados visuais em melhor desempenho.

Você define a propriedade Clip de um Visual usando o método [**IDCompositionVisual:: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) . Esse método inclui sobrecargas que permitem que você defina o valor da propriedade Clip para um retângulo estático ou para um objeto de clipe. Use um retângulo estático se você não precisar alterar as dimensões do retângulo do clipe durante o tempo de vida do Visual. Se você precisar alterar as dimensões ou animar o retângulo, use um objeto de clipe.

## <a name="clip-object"></a>Objeto de clipe

Um objeto de clipe é um objeto de Component Object Model (COM) que representa um retângulo de clipe. Você cria um objeto de clipe usando o método [**IDCompositionDevice:: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) e, em seguida, usa a interface [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) do objeto para definir as propriedades do objeto. Um objeto de clipe recém-criado tem os valores mínimos possíveis para as propriedades Left e Top, e os valores máximos possíveis para as propriedades Right e Bottom, tornando-o efetivamente um objeto de clipe não op. Em outras palavras, o objeto representa um retângulo de clipe que inclui todo o conteúdo de bitmap de um Visual.

Um objeto de clipe inclui um conjunto de propriedades que permitem que você especifique os cantos arredondados para o objeto de clipe. As propriedades permitem que você defina o raio x e y de cada canto do objeto de recorte.

## <a name="animated-clip-rectangle"></a>Retângulo de clipe animado

Você pode animar um clip-retângulo aplicando objetos de animação às propriedades esquerda, superior, direita e inferior de um objeto de clipe. Use o método sobrecarregado [**IDCompositionVisual:: SetClip (IDCompositionClip)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) para aplicar o retângulo de clipe animado à propriedade Clip de um Visual.

Para obter mais informações sobre objetos de animação, consulte [animação](animation.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de DirectComposition](directcomposition-concepts.md)
</dt> <dt>

[Como recortar com um objeto de clipe de retângulo](how-to--set-the-clip-rectangle-for-a-visual.md)
</dt> </dl>

 

 
