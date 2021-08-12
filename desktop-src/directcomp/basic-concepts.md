---
title: Conceitos básicos (DirectComposition)
description: Este tópico fornece uma visão geral dos conceitos básicos do Microsoft DirectComposition.
ms.assetid: F442BDCA-C913-4438-BFFA-D3F28B68EE85
keywords:
- Conceitos do DirectComposition
- Conceitos básicos do DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2dadcea55ec18089380d7dbe17d99e5dba92b06dd15774c43cd604f28f991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282001"
---
# <a name="basic-concepts"></a>Conceitos básicos

> [!NOTE]
> Para aplicativos Windows 10, recomendamos o uso de APIs Windows.UI.Composition em vez de DirectComposition. Para obter mais informações, consulte [Modernizar seu aplicativo da área de trabalho usando a camada visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico fornece uma visão geral dos conceitos básicos do Microsoft DirectComposition. Ele contém as seções a seguir:

-   [Composição](#composition-target-window)
-   [Visuais](#visuals)
    -   [Árvore visual](#visual-tree)
    -   [Propriedades de um objeto visual](#properties-of-a-visual-object)
-   [Objeto de dispositivo](#device-object)
-   [Janela de destino de composição](#composition-target-window)
-   [Composição transacional](#transactional-composition)
    -   [Separação em lotes](#batching)
    -   [Sincronização](#synchronization)
    -   [Árvores visuais entre dispositivos](#cross-device-visual-trees)
-   [Tópicos relacionados](#related-topics)

## <a name="composition"></a>Composição

DirectComposition define  uma composição como uma coleção de bitmaps que são combinados e manipulados aplicando várias transformações, efeitos e animações para produzir um resultado visual em uma interface do usuário do aplicativo. DirectComposition funciona apenas com conteúdo de bitmap; ele não dá suporte a vetores ou texto. DirectComposition não fornece conteúdo de bitmap. Em vez disso, ele fornece interfaces nas quais os usuários podem desenhar com D2D, DXGI ou carregar seu próprio conteúdo de textura.

Um aplicativo DirectComposition cria dois conjuntos de objetos para compor uma cena: bitmaps compostos juntos e visuais que definem as relações espaciais entre os bitmaps. Para obter mais informações sobre os objetos de bitmap com suporte pelo DirectComposition, consulte [Objetos bitmap](bitmap-surfaces.md).

## <a name="visuals"></a>Visuais

*Os visuais* (ou *objetos visuais*) são os elementos fundamentais do DirectComposition. Eles são os blocos de construção básicos que você usa para criar composições e animações na interface do usuário do aplicativo.

Em termos de programação, um visual é um objeto que tem um conjunto de propriedades e expõe uma interface que você usa para definir o valor das propriedades. A propriedade Content de um visual associa um bitmap específico ao visual, enquanto outras propriedades controlam como DirectComposition posiciona e manipula o visual conforme ele é renderizado na tela.

Para obter mais informações, [consulte Propriedades de um Visual](#properties-of-a-visual-object).

### <a name="visual-tree"></a>Árvore visual

DirectComposition cria uma composição de uma coleção hierárquica de objetos visuais chamada árvore *visual*. O visual na raiz de uma árvore é chamado de *visual raiz* e pode ter um ou mais visuais filho *associados* a ele. Um visual filho pode ter um ou mais visuais filho próprios. Qualquer visual que tenha visuais filho associados é chamado de *visual* pai e todos os visuais filho que compartilham o mesmo pai são chamados de *visuais irmãos.* Um visual específico, juntamente com todos os seus visuais filho e descendentes, é chamado de *subárvore visual*.

O local de um visual na árvore ajuda a determinar sua posição de tela e a ordem z em relação aos outros visuais na composição. O visual raiz é posicionado em relação ao canto superior esquerdo da área do cliente da janela de destino em que a composição é renderizada. Todos os visuais filho são posicionados em relação ao canto superior esquerdo do visual pai (ou o visual especificado pela propriedade TransformParent) e sempre aparecem na frente do pai na ordem z.

A ilustração a seguir mostra uma composição de visuais e a estrutura da árvore visual usada para produzir a composição. O Visual 1 é o visual raiz e também é o pai dos Visuais filho 2 e 3, que são visuais irmãos. O Visual 3 tem dois visuais filho próprios, Os Visuais 4 e 5. Juntos, os Visuais 3 a 5 comem uma subárvore visual.

![uma composição de visuais e a árvore visual correspondente](images/visuals-and-corresponding-tree.png)

Um visual pai mantém uma lista ordenada de seus visuais filho. Quando os visuais irmãos são posicionados de modo que eles se sobreponham, DirectComposition define a ordem z dos irmãos com base na ordem em que aparecem na lista de filhos do visual pai. Um irmão que aparece posteriormente na lista é colocado na frente de todos os irmãos que aparecem anteriormente na lista. A ilustração a seguir mostra a ordem z dos visuais filho sobrepostos.

![a ordem z dos visuais filho sobrepostos](images/overlapping-child-visuals.png)

### <a name="properties-of-a-visual-object"></a>Propriedades de um objeto visual

Um objeto visual expõe um conjunto de propriedades que permitem definir o conteúdo do bitmap para o visual e controlar como o DirectComposition posiciona e manipula o conteúdo visual. As seções a seguir descrevem cada propriedade em detalhes.

-   [Propriedade de conteúdo](#content-property)
-   [Propriedade Clip](#clip-property)
-   [Propriedade BorderMode](#bordermode-property)
-   [Propriedade BitmapInterpolationMode](#bitmapinterpolationmode-property)
-   [Propriedade CompositeMode](#compositemode-property)
-   [Propriedades OffsetX e OffsetY](#offsetx-and-offsety-properties)
-   [Propriedade Effect](#effect-property)
-   [Propriedade Transform](#transform-property)
-   [Propriedade TransformParent](#transformparent-property)

### <a name="content-property"></a>Propriedade de conteúdo

A propriedade Content de um visual especifica o conteúdo do bitmap associado ao visual. Esse é o bitmap que o DirectComposition usa quando você inclui o visual em uma composição.

Você pode definir a propriedade Content de um visual chamando o [**método IDCompositionVisual::SetContent.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent)

Para obter mais informações sobre os tipos de conteúdo de bitmap com suporte pelo DirectComposition, consulte [Objetos bitmap](bitmap-surfaces.md).

### <a name="clip-property"></a>Propriedade Clip

A propriedade Clip de um visual especifica uma área retangular chamada região *de recorte* (ou retângulo *de recorte*). Quando um visual é renderizado, somente a parte do visual que está dentro da região de recorte é exibida, enquanto qualquer conteúdo que se estende para fora da região de recorte é recortado (ou seja, não exibido). O DirectComposition dá suporte a regiões de recorte que têm cantos arredondados ou quadrados.

Você pode definir a propriedade Clip de um visual chamando o [**método IDCompositionVisual::SetClip.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))

Para obter mais informações, consulte [Recorte](clipping.md).

### <a name="bordermode-property"></a>Propriedade BorderMode

A propriedade BorderMode especifica como compor as bordas de bitmaps e clipes associados a esse visual ou com visuais na subárvore com raiz neste visual.

O modo de borda afeta como as bordas de um bitmap são compostas quando o bitmap é transformado de modo que as bordas não sejam alinhadas por eixo com coordenadas de inteiro. Ele também afeta como o conteúdo é recortado nos cantos de um clipe que tem cantos arredondados e na borda de um clipe transformado de modo que as bordas não estejam alinhadas ao eixo com coordenadas de inteiro.

Para obter mais informações, [**consulte IDCompositionVisual::SetBorderMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbordermode).

### <a name="bitmapinterpolationmode-property"></a>Propriedade BitmapInterpolationMode

A propriedade BitmapInterpolationMode informa ao DirectComposition como compor um bitmap quando ele é transformado de modo que não haja correspondência um-para-um entre pixels no bitmap e pixels na tela.

Você pode definir a propriedade BitmapInterpolationMode de um visual chamando o [**método IDCompositionVisual::SetBitmapInterpolationMode.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbitmapinterpolationmode)

### <a name="compositemode-property"></a>Propriedade CompositeMode

A propriedade CompositeMode informa Ao DirectComposition como combinar o conteúdo de bitmap de um visual com o destino de renderização. Para ver uma descrição dos modos compostos com suporte, consulte [**DCOMPOSITION \_ COMPOSITE \_ MODE**](/windows/desktop/api/DcompTypes/ne-dcomptypes-dcomposition_composite_mode).

Você pode definir a propriedade CompositeMode de um visual chamando o [**método IDCompositionVisual::SetCompositeMode.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcompositemode)

### <a name="offsetx-and-offsety-properties"></a>Propriedades OffsetX e OffsetY

As propriedades OffsetX e OffsetY dizem ao DirectComposition onde posicionar um visual horizontal e verticalmente. Eles definem a posição fixa bidimensional da qual todas as transformaçãos e efeitos para o visual são calculados.

Para um visual raiz, as propriedades OffsetX e OffsetY definem a coordenada x e a coordenada y de um ponto em relação ao canto superior esquerdo da janela que hospeda o visual. Para um visual filho, as coordenadas são relativas ao canto superior esquerdo do pai ou, se a propriedade [TransformParent](#transformparent-property) for especificada, o canto superior esquerdo do visual especificado. Quando um visual é renderizado, ele é posicionado de forma que o canto superior esquerdo do visual coincide com as coordenadas especificadas.

Você pode definir as propriedades OffsetX e OffsetY de um visual chamando os métodos [**IDCompositionVisual::SetOffsetX**](/previous-versions/windows/desktop/legacy/hh449126(v=vs.85)) e [**SetOffsetY.**](/previous-versions/windows/desktop/legacy/hh449131(v=vs.85))

### <a name="effect-property"></a>Propriedade Effect

A propriedade Effect permite especificar um efeito ou um grupo de efeitos que modificará como um visual e sua subárvore são compostos. Por exemplo, você pode especificar efeitos que controlam a opacidade de um visual, combinar o visual com outro bitmap de várias maneiras e aplicar as transformação de perspectiva ao visual.

Você pode definir a propriedade Effect de um visual chamando o [**método IDCompositionVisual::SetEffect.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect)

Para obter mais informações, veja [Efeitos](effects.md).

### <a name="transform-property"></a>Propriedade Transform

A propriedade Transform especifica uma transformação bidimensional (2D) ou um grupo de transformações 2D, para DirectComposition executar no Visual. Uma transformação (ou transformação) é uma operação que modifica o sistema de coordenadas de um Visual relativo ao seu pai ou em relação ao Visual especificado pela [Propriedade TransformParent](#transformparent-property). Você pode usar transformações para alterar a posição, o tamanho ou a natureza de um Visual, movendo-o para outro local (tradução), tornando-o maior ou menor (dimensionando), virando-o (rotação), distorcendo sua forma (distorção) e assim por diante.

Você define a propriedade Transform de um Visual chamando o método [**IDCompositionVisual:: SetTransform**](/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)) .

Para obter mais informações, consulte [Transformações](transforms.md).

### <a name="transformparent-property"></a>Propriedade TransformParent

O sistema de coordenadas de um Visual é modificado pelas propriedades OffsetX, OffsetY e Transform. Normalmente, essas propriedades definem o sistema de coordenadas de um Visual em relação ao seu pai imediato. Para usar algum elemento visual diferente do pai como base para o sistema de coordenadas de um Visual filho, use a propriedade TransformParent para especificar um visual diferente como "pai" para fins de transformação.

Você define a propriedade TransformParent de um Visual chamando o método [**IDCompositionVisual:: SetTransformParent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransformparent) .

## <a name="device-object"></a>Objeto de dispositivo

Para usar o DirectComposition, você deve criar e manipular uma variedade de objetos COM (Component Object Model). O primeiro objeto que você precisa criar é o objeto de *dispositivo* DirectComposition porque ele serve como o alocador para a criação de todos os outros objetos usados em uma composição.

Você cria um objeto de dispositivo chamando a função [**DCompositionCreateDevice**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) , que retorna um ponteiro de interface [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) . Essa interface expõe um conjunto de métodos que você usa para criar objetos visuais, objetos de clipe, objetos de animação, objetos de transformação, objetos de efeito e assim por diante.

O objeto de dispositivo atende a outra finalidade, além de ser um alocador para a criação de outros objetos. Ele expõe um método chamado [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) que passa uma árvore visual para DirectComposition para processamento. Para obter mais informações, consulte [composição transacional](#transactional-composition).

Lembre-se de que, embora você possa criar várias instâncias do objeto de dispositivo em seu aplicativo, todos os objetos que você usa em uma composição específica devem ser criados pelo mesmo objeto de dispositivo — com uma exceção: você pode combinar objetos visuais de diferentes objetos de dispositivo na mesma árvore visual. Quando você faz isso, o DirectComposition trata a árvore visual normalmente, exceto que as alterações em um objeto visual específico na árvore entram em vigor somente quando o método [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) é chamado no objeto de dispositivo que criou o objeto visual.

A capacidade de usar visuais de diferentes dispositivos na mesma árvore visual permite que vários threads criem e manipulem uma única árvore visual mantendo dois dispositivos independentes que podem ser usados para confirmar as alterações de forma assíncrona. Para obter mais informações, consulte [árvores visuais de dispositivos cruzados](#cross-device-visual-trees).

## <a name="composition-target-window"></a>Janela de destino da composição

Uma árvore visual deve ser associada a uma janela antes que qualquer um dos visuais da árvore possa ser exibido na tela. A janela, chamada de *janela de destino de composição*, pode ser uma janela de nível superior ou uma janela filho. Além disso, a janela de destino de composição pode ser uma janela em camadas; ou seja, ele pode ter o estilo de janela em [**\_ \_ camadas WS ex**](/windows/desktop/winmsg/extended-window-styles) .

O DirectComposition permite que um aplicativo associe um máximo de duas árvores visuais a cada janela. As árvores visuais incluem uma que é composta sobre a própria janela, mas por trás de todas as janelas filhas da janela, e outra que é composta na parte superior da janela e sobre as janelas filhas. Em outras palavras, cada janela tem quatro camadas conceituais e todas as camadas são recortadas na região visível da janela de destino. A ilustração a seguir mostra as quatro camadas conceituais de uma janela.

![as camadas conceituais de uma janela](images/directcomposition-layers.png)

## <a name="transactional-composition"></a>Composição transacional

O DirectComposition usa um modelo transacional em que você cria um conjunto em lote de alterações em um Visual e, em seguida, "confirma" o conjunto como DirectComposition para o processamento de todos de uma vez. Você pode modificar o mesmo objeto visual DirectComposition e confirmar as alterações várias vezes. Quando o Gerenciador de Janelas da Área de Trabalho (DWM) pega lotes, ele pega todos os lotes pendentes e os aplica ao próximo quadro na ordem em que foram confirmados.

Todas as alterações em uma única confirmação têm a garantia de serem aplicadas a um único quadro. Como o DWM coleta lotes uma vez por quadro, você pode modificar qualquer objeto específico apenas uma vez por quadro. As confirmações subsequentes que modificam objetos diferentes também podem ser aplicadas ao quadro atual, mas DirectComposition não garante que as alterações ocorrerão no mesmo quadro.

Os métodos [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) e [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) permitem sincronizar atualizações de renderização com atualizações visuais. Por exemplo, você pode chamar **IDCompositionSurface:: BeginDraw**, atualizar as propriedades de OffsetX e de clipe de um Visual, chamar [**IDCompositionDevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit), desenhar conteúdo com o Microsoft DirectX e, em seguida, chamar **IDCompositionSurface:: EndDraw**. Nesse caso, o Microsoft DirectComposition garante que o conteúdo de bitmap e as propriedades visuais sejam atualizados ao mesmo tempo.

### <a name="batching"></a>Separação em lotes

Você pode confirmar várias alterações no mesmo elemento visual ou várias alterações em elementos visuais diferentes, dentro do mesmo quadro. Ao fazer várias alterações no mesmo visual dentro do mesmo quadro, tenha em mente os seguintes pontos:

-   Se você fizer várias alterações na mesma propriedade de um Visual, somente a última alteração será aplicada. Por exemplo, se você definir a opacidade como 0, depois para 0,5 e, finalmente, para 1,0, apenas uma opacidade de 1,0 será aplicada ao Visual.
-   Se você alterar várias propriedades do mesmo visual, DirectComposition aplicará as alterações primeiro ao Visual e, em seguida, a qualquer elemento visual filho. As propriedades são aplicadas na ordem a seguir, independentemente da ordem em que você as especificar:

    1.  Deslocamento
    2.  Transformar
    3.  Recortar
    4.  Efeito

    A ilustração a seguir mostra o resultado da aplicação de todas as quatro propriedades em um Visual.

    ![resultado da aplicação de todas as quatro propriedades a um Visual](images/order-of-properties.png)

    Lembre-se de que todas as alterações são aplicadas ao Visual de uma vez no contexto do mesmo quadro. Isso significa que, da perspectiva do usuário, as alterações no Visual ocorrem instantaneamente.

-   Para a propriedade Transform, você pode usar [**IDCompositionDevice:: CreateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) para criar um grupo de transformações para aplicar a um Visual de uma só vez. DirectComposition aplica as transformações na ordem especificada.
-   Para a Propriedade Effect, você pode usar [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) para aplicar um grupo de efeitos. DirectComposition aplica os efeitos na ordem que você especificar. Além disso, as transformações de perspectiva 3D resultam em achatamento da árvore visual depois que todas as transformações 3D no Visual atual tiverem sido aplicadas. Isso ajuda a garantir que o Visual resultante pareça o mais próximo possível do 3D.

### <a name="synchronization"></a>Sincronização

Seu aplicativo pode chamar DirectComposition de vários threads ao mesmo tempo. A ordem de execução é garantida para chamadas sequenciais, mas não para chamadas simultâneas. Por exemplo, se o thread A modificar um Visual e o thread B confirmar o lote ao mesmo tempo, ele não será definido se essa alteração Visual for incluída no lote confirmado ou se ele iniciará um novo lote. Por outro lado, se seu aplicativo usar outros mecanismos de sincronização para garantir que um método seja chamado antes do outro, o DirectComposition honrará a ordem de chamada e os processará como se ambas as chamadas fossem emitidas nessa ordem a partir de um único thread.

### <a name="cross-device-visual-trees"></a>Árvores visuais de dispositivos cruzados

Os objetos DirectComposition não são associados a thread; Você pode usar vários threads para modificar o mesmo conjunto de objetos. No entanto, esteja ciente dos problemas a seguir ao compartilhar o mesmo objeto de dispositivo.

-   Ambos os threads precisam ser capazes de chamar [**IDCompositionDevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). Se apenas um dos threads chamar **IDCompositionDevice:: Commit**, o outro thread não poderá confirmar nenhuma de suas alterações para DirectComposition.
-   O comportamento transacional pode ser perdido se um thread chamar [**IDCompositionDevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) enquanto o outro thread ainda estiver fazendo alterações que se destinam a fazer parte da mesma transação.

Se você precisar confirmar várias transações simultâneas em DirectComposition, deverá usar vários objetos de dispositivo, possivelmente de vários threads. Nesse cenário, a mesma árvore visual é compartilhada por ambos os objetos de dispositivo, e cada objeto de dispositivo confirma suas próprias transações.

A ilustração a seguir mostra uma árvore visual que é compartilhada por dois objetos de dispositivo. Os elementos visuais 1, 2, 4 e 5 pertencem a um dispositivo ou outro, mas o Visual 3 é compartilhado por ambos os dispositivos e, portanto, pode ser usado para conectar duas subárvores em uma única e maior árvores visuais. O compartilhamento da árvore visual permite que os dois dispositivos sejam manipulados de dois threads diferentes de forma assíncrona.

![uma árvore visual compartilhada por dois dispositivos](images/shared-visual-tree-1.png)

Para ilustrar a utilidade de compartilhar uma árvore visual entre dois dispositivos, considere uma arquitetura que permita a entrada por toque de baixa latência. A arquitetura pode usar dois threads, um que manipula a maioria das tarefas de interface do usuário e um segundo thread dedicado ao processamento de eventos de entrada de toque. O thread de toque atualiza a transformação de um Visual específico com base no gesto de entrada do usuário. Ao atualizar a transformação, o thread de toque pode fazer com que toda a subárvore sob esse visual siga o dedo do usuário, escale ou reduza verticalmente à medida que o usuário executa um gesto multitoque e assim por diante. O thread da interface do usuário retém a propriedade da maior parte da árvore de composição, com o thread de toque que possui apenas os poucos visuais marcados para resposta de toque assíncrono. A ilustração a seguir mostra uma versão simplificada dessa árvore de composição:

![uma árvore visual compartilhada entre um thread de interface do usuário e um thread de toque](images/shared-visual-tree-2.png)

Normalmente, o thread da interface do usuário modifica apenas os visuais que ele possui exclusivamente e o thread de toque modifica apenas o Visual compartilhado. A única exceção ocorre ao criar ou destruir uma subárvore habilitada para toque.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)
</dt> <dt>

[**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)
</dt> <dt>

[**IDCompositonDevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
</dt> <dt>

[Conceitos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 