---
title: Superfície de composição
description: Este tópico descreve os tipos de tipos de superfícies aos quais o Microsoft DirectComposition dá suporte.
ms.assetid: E19B4F0E-1CFA-4E93-BB6A-BFB701BC72CA
keywords:
- superfície de composição
- Superfície lógica DirectComposition
- Superfície virtual DirectComposition
- Atualizando uma superfície lógica
- superfície lógica, atualizando
- aparando uma superfície virtual
- superfície virtual, corte
- cortar superfície virtual
- Redimensionando uma superfície virtual
- Surace virtual, redimensionamento
- redimensionar superfície virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4bd30bfbd1de91444b7076184db597cd7a8c82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007725"
---
# <a name="composition-surface"></a>Superfície de composição

> [!NOTE]
> Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico descreve os tipos de tipos de superfícies aos quais o Microsoft DirectComposition dá suporte.

-   [Superfície lógica DirectComposition](#directcomposition-logical-surface)
    -   [Atualizando uma superfície lógica](#updating-a-logical-surface)
    -   [Suspendendo atualizações para uma superfície lógica](#suspending-updates-to-a-logical-surface)
    -   [Retomando atualizações para uma superfície lógica](#resuming-updates-to-a-logical-surface)
    -   [Finalizando atualizações para uma superfície lógica](#suspending-updates-to-a-logical-surface)
    -   [Exemplo de uso de uma superfície lógica](#example-of-using-a-logical-surface)
-   [Superfície virtual DirectComposition](#directcomposition-virtual-surface)
    -   [Redimensionando uma superfície virtual](#resizing-a-virtual-surface)
    -   [Aparando uma superfície virtual](#trimming-a-virtual-surface)
-   [Tópicos relacionados](#related-topics)

## <a name="directcomposition-logical-surface"></a>Superfície lógica DirectComposition

DirectComposition expõe o objeto [**IDCompositionSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface) para representar uma superfície de composição lógica. O DirectComposition expõe APIs que você pode usar para criar, atualizar e excluir essas superfícies lógicas. Cada superfície pode ser associada a um ou mais visuais. Um aplicativo é responsável por gerenciar o tempo de vida de superfícies lógicas.

### <a name="updating-a-logical-surface"></a>Atualizando uma superfície lógica

Um aplicativo pode atualizar uma superfície lógica chamando [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) e especificando o tamanho e o deslocamento do retângulo na superfície lógica que o aplicativo deseja atualizar. DirectComposition aloca um retângulo do tamanho especificado e, em seguida, retorna a superfície e o deslocamento correspondente que o aplicativo precisa para desenhar ou atualizar. Os limites do retângulo de atualização são limitados pelo tamanho da superfície. Por exemplo, o retângulo de atualização para uma superfície de pixel de 40 por 100 pode ser até (0, 0, 40100). Além disso, a região atualizável é imposta por um retângulo de proteção. Como pode haver apenas um retângulo de proteção por vez, apenas uma superfície lógica pode ser atualizada de cada vez. **BeginDraw** retornará um código de erro se [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) ou [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) não tiver sido chamado após uma chamada anterior para **BeginDraw**. Um aplicativo pode adicionar uma chamada confirmada para **BeginDraw** a um lote, mas ele não tem efeito até que **EndDraw** seja chamado e confirmado.

### <a name="suspending-updates-to-a-logical-surface"></a>Suspendendo atualizações para uma superfície lógica

Um aplicativo que precisa atualizar superfícies diferentes pode chamar [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) na atualização atual e, em seguida, chamar [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) para iniciar uma nova atualização. O Microsoft DirectComposition permite várias atualizações, mas apenas uma pode estar ativa por vez. Isso significa que você precisa chamar **SuspendDraw** ou [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) em uma superfície antes de chamar **BeginDraw** no próximo. Ao contrário de **EndDraw**, um lote confirmado pode conter uma superfície que está em um estado **SuspendDraw** , mas essas atualizações não serão mostradas na tela até que **EndDraw** seja chamado.

### <a name="resuming-updates-to-a-logical-surface"></a>Retomando atualizações para uma superfície lógica

Um aplicativo pode retomar uma atualização para uma superfície que está em um estado [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) chamando [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw). Esse método pode ser chamado somente em uma superfície suspensa.

### <a name="ending-updates-to-a-logical-surface"></a>Finalizando atualizações para uma superfície lógica

Chamar [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) e [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) é a única maneira de ver as alterações de atualização de bitmap na tela. Cada chamada para **EndDraw** deve ter uma chamada correspondente para [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) para remover o retângulo de proteção. A superfície lógica retém todas as atualizações até que a **confirmação** seja chamada. Você também pode chamar **EndDraw** em uma superfície que está no estado [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) porque **EndDraw** é um currículo/final implícito. Depois de chamar **EndDraw**, o conteúdo atualizado é apresentado à tela e descartado para que a memória da atualização possa ser reutilizada para uma atualização posterior.

### <a name="example-of-using-a-logical-surface"></a>Exemplo de uso de uma superfície lógica

O exemplo a seguir descreve as etapas que um aplicativo tomaria se ele criasse uma árvore visual que consiste em dois visuais e, em seguida, precisava atualizar regiões específicas das duas superfícies lógicas associadas aos visuais:

1.  Crie um dispositivo DirectComposition.
2.  Crie a árvore visual que consiste em um nó raiz e os visuais 1 e 2.
3.  Crie superfícies lógicas 1 e 2.
4.  Chame [**setContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) para associar uma superfície lógica com visuais 1 e 2.
5.  Chame [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) em um subretângulo da superfície lógica 1.
6.  Atualize a superfície no deslocamento retornado por DirectComposition.
7.  Etapas opcionais:
    1.  Chame [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) na superfície lógica 1.
    2.  Chame [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) no subrect da superfície lógica 2.
    3.  Atualize a superfície no deslocamento retornado por DirectComposition.
    4.  Chame [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) na superfície lógica 2.
    5.  Chame [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) na superfície lógica 1.
8.  Atualize a superfície no deslocamento retornado por DirectComposition.
9.  Chame [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) na superfície lógica 1.
10. Chame [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit).

## <a name="directcomposition-virtual-surface"></a>Superfície virtual DirectComposition

DirectComposition expõe a interface [**IDCompositionVirtualSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvirtualsurface) para representar uma superfície virtual, que é uma coleção de superfícies lógicas (blocos) organizados em uma grade fixa com blocos de um tamanho fixo. O aplicativo especifica o tamanho da textura virtual no momento da criação. O tamanho estabelece os limites para a superfície virtual. A superfície pode ser associada a um ou mais visuais.

Quando uma superfície virtual é inicializada, ela não é apoiada por alocações reais. Em outras palavras, ele não contém nenhum bit. DirectComposition aloca blocos (ou seja, objetos superfície de composição) depois que o aplicativo inicia a atualização da superfície. O aplicativo atualiza a superfície virtual chamando [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) e especificando a região de interesse em relação às coordenadas da superfície virtual. Em seguida, DirectComposition aloca os blocos necessários para manter a atualização e retorna a superfície de composição e o deslocamento para atualização.

Assim como ocorre com superfícies lógicas, você pode chamar [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) e [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) em uma superfície virtual. Além disso, o DirectComposition expõe métodos que você pode usar para redimensionar e aparar uma superfície virtual existente.

### <a name="resizing-a-virtual-surface"></a>Redimensionando uma superfície virtual

O método [**redimensionar**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-resize) altera os limites da superfície virtual, o que significa que quaisquer novas atualizações ou alocações devem estar nos limites definidos pelo novo tamanho. Um aplicativo usa **redimensionamento** para informar ao DirectComposition que uma determinada região da superfície virtual não é mais necessária e pode ser recuperada. Se **redimensionar** reduzir a superfície virtual, o aplicativo não poderá mais atualizar as regiões fora dos novos limites.

A ilustração a seguir mostra uma superfície virtual 3-por-3 redimensionada para 2-by-2. A região vermelha representa os blocos que são descartados como parte da operação de redimensionamento e a memória é recuperada pelo DirectComposition. Após o redimensionamento, o aplicativo não poderá fazer atualizações na região vermelha sem redimensionar a superfície virtual novamente.

![Redimensionando uma superfície virtual ](images/resize-virtual-surface.png)

A operação de redimensionamento entra em vigor imediatamente. DirectComposition não aguarda o aplicativo chamar [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) para fazer as atualizações de redimensionamento. Por exemplo, suponha que um aplicativo faça a seguinte sequência de chamadas.


```
pVirtualSurface->Resize(0, 0);
pVirtualSurface->Resize(INT_MAX, INT_MAX);
pDevice->Commit();
```



Neste exemplo, o aplicativo perde todo o conteúdo no primeiro redimensionamento. O segundo redimensionamento não tem nenhum efeito, embora ele tenha sido chamado antes da [**confirmação**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). Nesse caso, nada aparece na tela.

### <a name="trimming-a-virtual-surface"></a>Aparando uma superfície virtual

O método [**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) identifica a região da superfície virtual que o aplicativo precisa. Ele não redimensiona os limites da superfície virtual, mas informa DirectComposition quais superfícies lógicas precisam ser alocadas no momento.

Na ilustração a seguir, o quadrado verde é o visor do aplicativo. Inicialmente, o aplicativo é renderizado para os seis primeiros blocos (azul) da superfície virtual (cinza claro) que estão no visor. Como a página representada pela superfície virtual rola, o aplicativo precisa renderizar os últimos seis blocos. O aplicativo chama [**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) para indicar que a região definida pelos últimos seis blocos é onde o conteúdo é, e o resto não é necessário no momento. DirectComposition pode optar por reciclar as superfícies lógicas que originalmente representaram os seis primeiros blocos (cinza escuro).

![aparando uma superfície virtual](images/trim-virtual-surface.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 