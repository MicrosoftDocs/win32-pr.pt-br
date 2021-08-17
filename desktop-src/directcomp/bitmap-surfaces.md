---
title: Objetos de bitmap
description: Este tópico descreve os tipos de conteúdo de bitmap aos quais o DirectComposition dá suporte.
ms.assetid: BC32CF76-D5E4-4B25-AFD5-42E8DABFA0D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc36253511c060b264039f27975c694272c1c916ad0067c1955fd02f00553d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089046"
---
# <a name="bitmap-objects"></a>Objetos de bitmap

> [!NOTE]
> para aplicativos no Windows 10, é recomendável usar as APIs Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

O Microsoft DirectComposition é um mecanismo de composição de bitmap. Ele permite que os desenvolvedores de aplicativos combinem vários bitmaps e os manipulem de várias maneiras para obter animações e efeitos visuais interessantes em uma interface do usuário do aplicativo. Este tópico descreve os tipos de conteúdo de bitmap aos quais o DirectComposition dá suporte.

-   [Conteúdo de bitmap](#bitmap-content)
    -   [Bitmaps de memória de vídeo](#video-memory-bitmaps)
    -   [Bitmaps de janela](#window-bitmaps)
    -   [Associando conteúdo de bitmap a um Visual](#associating-bitmap-content-with-a-visual)
    -   [Canal alfa](#alpha-channel)
-   [Tópicos relacionados](#related-topics)

## <a name="bitmap-content"></a>Conteúdo de bitmap

Os aplicativos fornecem DirectComposition com o conteúdo do bitmap para compor e animar criando objetos visuais e, em seguida, definindo a [Propriedade Content](basic-concepts.md) desses objetos. O DirectComposition não oferece nenhum serviço de rasterização. um aplicativo deve usar outra biblioteca de rasterização baseada em software ou por hardware, como [Direct2D](../direct2d/direct2d-portal.md) ou [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) , para preencher os bitmaps que devem ser compostos. Após a composição, o DirectComposition passa o conteúdo de bitmap composto para [Gerenciador de janelas da área de trabalho (DWM)](/windows/desktop/dwm/dwm-overview) para renderização na tela.

**Tipos de conteúdo de bitmap com suporte** O Microsoft DirectComposition dá suporte aos seguintes tipos de bitmaps:

-   [Bitmaps de memória de vídeo](#video-memory-bitmaps)
-   [Bitmaps de janela](#window-bitmaps)

### <a name="video-memory-bitmaps"></a>Bitmaps de memória de vídeo

Um bitmap de memória de vídeo é rasterizado no hardware usando métodos do Microsoft DirectX (incluindo o modelo de interoperabilidade DX para GDI). Ele é apoiado por superfícies compartilhadas entre processos que são visíveis para o aplicativo de chamada e para o DirectComposition. Um bitmap de memória de vídeo não está sujeito à divisão porque o aplicativo só pode ler das superfícies das quais DirectComposition texturas.

### <a name="video-content"></a>Conteúdo de vídeo

Os aplicativos podem usar DirectComposition para compor quadros de vídeo que usam cadeias de permuta sem janela do DirectX associadas a uma superfície DirectComposition. Conceitualmente, o DirectComposition trata o conteúdo de vídeo como uma sequência de bitmaps. O DirectComposition não fornece um meio de apresentar quadros de vídeo.

O DirectComposition dá suporte a cadeias de permuta sem janela do DirectX, ou seja, cadeias de permuta que não estão associadas a uma janela específica, e permite que dois aplicativos diferentes compartilhem cadeias de troca sem janelas entre limites de processo. O compartilhamento de cadeias de troca sem janela permite cenários de vídeo em que a cadeia de permuta é criada em um processo e é usada com DirectComposition em um segundo processo. As cadeias de permuta sem janela são criadas usando o método [**IDXGIFactory2:: CreateSwapChainForCompositionSurface**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .

Para obter mais informações sobre cadeias de permuta do DirectX, consulte [visão geral do dxgi](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

### <a name="stereo-content"></a>Conteúdo estéreo

Conceitualmente, uma cadeia de permuta estéreo consiste em superfícies de DXGI (infraestrutura gráfica do DirectX) da Microsoft que representam os canais esquerdo e direito para o conteúdo 3D estéreo. Quando uma cadeia de permuta estéreo é usada como o recurso de bitmap para um Visual, DirectComposition compõe em estéreo. Todo o conteúdo não estéreo (conteúdo mono) é considerado como conteúdo de canal esquerdo e direito idêntico; ou seja, o mesmo conteúdo de bitmap é usado para ambos os canais. DirectComposition compõe todo o conteúdo à esquerda e todo o conteúdo correto separadamente. Se o dispositivo de vídeo não for compatível com estéreo, o DirectComposition tratará o canal estéreo esquerdo ou direito (dependendo do aplicativo) como conteúdo mono e comporá usando apenas os dados para o recurso de bitmap.

DirectComposition não dá suporte à criação ou manipulação de conteúdo estéreo e não pode promover uma cadeia de permuta mono para um par estéreo. Um aplicativo deve executar essas tarefas antes de apresentar o conteúdo do DirectX estéreo ao DirectComposition. Além disso, um aplicativo deve fornecer os deslocamentos de canal à esquerda e à direita para percepção de profundidade; DirectComposition não pode ajustar os deslocamentos de canal à esquerda e à direita para modificar a profundidade percebida do conteúdo de estéreo do DirectX.

O conteúdo de estéreo do DirectX é composto e persistido no DWM quando o hardware com capacidade para estéreo está disponível.

### <a name="window-bitmaps"></a>Bitmaps de janela

Um "bitmap de janela" não é um bitmap real, mas é um espaço reservado que o DirectComposition substitui em tempo real com rasterizações de janelas de nível superior ou filho em camadas. Um bitmap de janela é semelhante a uma miniatura do DWM, exceto que uma miniatura pode conter contribuições de muitas janelas, como janelas não-filhas de propriedade, enquanto um bitmap de janela DirectComposition sempre é uma representação de apenas uma janela e seus filhos.

Como DirectComposition tem acesso às superfícies de redirecionamento de todas as janelas e todas as árvores visuais, ele pode reutilizar o conteúdo de uma janela em várias árvores visuais. A janela deve ser inserida em camadas porque uma janela não em camadas não tem uma superfície de redirecionamento dedicada e, portanto, sua rasterização não está sempre disponível para DirectComposition.

Para usar um bitmap de janela, um aplicativo associa um Visual a um identificador de janela (HWND). Depois disso, DirectComposition recriará o Visual sempre que o conteúdo da janela for alterado, incluindo quando o conteúdo é alterado como resultado das alterações nas árvores visuais associadas à janela. Em outras palavras, como as miniaturas do DWM, os bitmaps da janela DirectComposition são "dinâmicos".

### <a name="associating-bitmap-content-with-a-visual"></a>Associando conteúdo de bitmap a um Visual

Para todos os três tipos de bitmaps, um aplicativo pode associar o mesmo bitmap com vários visuais, o que significa que uma única alocação de memória pode ser usada para exibir o mesmo conteúdo várias vezes.

### <a name="alpha-channel"></a>Canal alfa

Todos os bitmaps têm um formato de 32 bits por pixel (BPP), que inclui oito bits para a transparência por pixel. No entanto, um aplicativo pode especificar como o DirectComposition deve consumir o canal alfa. Em particular, o DirectComposition pode respeitar o canal alfa, ou pode ignorar alfa totalmente; nesse caso, o bitmap é considerado totalmente opaco.

Um modo alfa adicional ignora o canal alfa, mas trata os valores vermelho, verde e azul como valores Alfa por canal em vez da interpretação normal desses canais como intensidades de cor. Esse modo é útil para renderização de ClearType, que requer informações de cobertura de sub-pixel. para usar o modo alfa por canal, um aplicativo deve primeiro usar [Direct2D](../direct2d/direct2d-portal.md) e [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) para gravar dados de cobertura de sub-pixel em um bitmap. Em seguida, o aplicativo deve definir o modo alfa correto e especificar uma cor de texto ao associar o bitmap a um Visual. O DirectComposition mistura a cor do texto com os dados de cobertura, que produzem a mesclagem de ClearType em relação ao plano de fundo.

Em situações em que o algoritmo ClearType não é aplicável, como se o bitmap não estiver alinhado em pixel e alinhado com eixo, ou se precisar ser desenhado em uma superfície intermediária, o DirectComposition poderá usar os dados de cobertura de subpixel no bitmap para produzir uma rasterização em escala de cinza, automaticamente e sem custo adicional.

Para obter mais informações, consulte a descrição do parâmetro *alphamode* da função [**IDCompositionDevice:: CreateSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurface) ou [**IDCompositionDevice:: CreateVirtualSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 