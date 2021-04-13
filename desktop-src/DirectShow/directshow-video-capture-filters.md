---
description: Filtros de captura de vídeo do DirectShow
ms.assetid: e4d1452d-ceac-4b5c-b9ba-ad4722ecff76
title: Filtros de captura de vídeo do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f18dd77bc40011fa9fc0dbab3192ea81a223f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456413"
---
# <a name="directshow-video-capture-filters"></a>Filtros de captura de vídeo do DirectShow

Os filtros de captura no DirectShow têm alguns recursos que os distinguem de outros tipos de filtros. Embora o [Construtor de gráficos de captura](capture-graph-builder.md) oculte muitos dos detalhes, é uma boa ideia ler esta seção para ter uma compreensão geral dos gráficos de captura do DirectShow.

**Fixar categorias**

Um filtro de captura geralmente tem dois ou mais Pins de saída que fornecem o mesmo tipo de dados — por exemplo, um PIN de visualização e um PIN de captura. Portanto, os tipos de mídia não são uma boa maneira de distinguir os Pins. Em vez disso, os Pins são diferenciados por sua funcionalidade, que é identificada usando um GUID, chamado de *categoria de PIN*.

Para obter uma discussão sobre como consultar Pins para sua categoria, consulte [trabalhando com categorias de PIN](working-with-pin-categories.md). No entanto, para a maioria dos aplicativos, você não precisará consultar Pins diretamente. Em vez disso, vários métodos [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) usam parâmetros que especificam a categoria de PIN na qual operar. O construtor do grafo de captura localiza automaticamente o PIN correto.

**Pins de visualização e Pins de captura**

Alguns dispositivos de captura de vídeo têm pins de saída separados para visualização e captura. O pino de visualização é usado para renderizar o vídeo na tela, enquanto o pino de captura é usado para gravar vídeo em um arquivo.

Um PIN de visualização e um PIN de captura têm as seguintes diferenças:

-   Um PIN de visualização descarta os quadros conforme necessário para manter a taxa de transferência no pino de captura.
-   Cada quadro de um PIN de captura é carimbado com o tempo do fluxo quando o quadro foi capturado. Um PIN de visualização não faz o carimbo de data/hora dos exemplos que ele fornece.

O motivo pelo qual os quadros de visualização não têm carimbos de data/hora é que o grafo de filtro apresenta uma pequena quantidade de latência no fluxo. Se o tempo de captura for usado como o tempo de apresentação, o renderizador de vídeo tratará cada exemplo como sendo um pouco tarde. Isso pode fazer com que o renderizador de vídeo descarte os quadros enquanto tenta acompanhar. Remover os carimbos de data/hora garante que o renderizador apresente cada exemplo quando ele chega, sem descartar os quadros.

A categoria de PIN para os Pins de visualização é a versão prévia da categoria de fixação \_ \_ . A categoria para Pins de captura é fixar a \_ captura de categoria \_ .

**Pins de porta de vídeo**

Uma porta de vídeo é uma conexão de hardware entre um dispositivo de vídeo (como um sintonizador de TV analógico) e a placa de vídeo. Uma porta de vídeo permite que o dispositivo envie dados de vídeo diretamente para a placa gráfica. O vídeo é exibido na tela usando uma sobreposição de hardware. Uma porta de vídeo pode ser um cabo real que conecta dois dispositivos em cartões separados; ou pode ser uma conexão com fio no mesmo cartão.

A vantagem de uma porta de vídeo é que o vídeo vai diretamente para a memória de vídeo, sem qualquer trabalho da CPU. No entanto, as portas de vídeo têm algumas desvantagens:

-   Uma porta de vídeo sempre usa a superfície de sobreposição durante a captura, independentemente se você deseja visualizar o vídeo.
-   A inversão entre quadros ocorre automaticamente, o que dificulta a sincronização da inversão com outras operações de vídeo.

Se um dispositivo de captura usar uma porta de vídeo, o filtro de captura terá um PIN de porta de vídeo em vez de um PIN de visualização. A categoria de PIN para Pins de porta de vídeo é fixar \_ categoria \_ VIDEOPORT.

Cada filtro de captura tem pelo menos um PIN de captura. Além disso, ele pode ter um PIN de visualização ou um PIN de porta de vídeo, mas nunca ambos. Os filtros podem ter vários Pins de captura e Pins de visualização, cada um fornecendo um tipo de mídia separado. Assim, um único filtro pode ter um pino de captura de vídeo, um pino de visualização de vídeo, um PIN de captura de áudio e um pino de visualização de áudio. (No entanto, não há nada equivalente a uma porta de vídeo para áudio.)

**Filtros WDM de upstream**

Os dispositivos Windows Driver Model (WDM) podem exigir alguns filtros adicionais upstream do filtro de captura. Esses filtros incluem o seguinte:

-   [Filtro de sintonizador de TV](tv-tuner-filter.md). Controles de ajuste para sintonizadores de TV analógicos.
-   [Filtro de áudio de TV](tv-audio-filter.md). Controla as configurações de áudio para sintonizadores de TV analógicos.
-   [Filtro Crossbar de vídeo analógico](analog-video-crossbar-filter.md). Roteia sinais de vídeo e áudio por meio do dispositivo de hardware. Por exemplo, um dispositivo pode ter várias entradas, como S-Video e vídeo composto. O filtro Crossbar permite que o aplicativo selecione a entrada.

Embora esses sejam filtros separados no DirectShow, normalmente representam o mesmo dispositivo de hardware. Cada filtro controla uma função diferente do dispositivo. Os filtros são conectados por Pins, mas nenhum dado de mídia é movido entre as conexões de PIN. Portanto, os Pins nesses filtros não se conectam estabelecendo um tipo de mídia. Em vez disso, eles usam valores GUID chamados *médias*. Os GUIDs médios são definidos exclusivamente para um determinado dispositivo minidriver. Por exemplo, o filtro de sintonizador de TV e o filtro de captura de vídeo para a mesma placa de TV terão suporte para a mesma mídia, o que permite que o aplicativo crie o grafo corretamente.

Na prática, contanto que você esteja usando **ICaptureGraphBuilder2** para criar gráficos de captura, esses filtros são adicionados ao grafo automaticamente. Para obter uma discussão mais detalhada, consulte [filtros de driver de classe WDM](wdm-class-driver-filters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a captura de vídeo no DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



