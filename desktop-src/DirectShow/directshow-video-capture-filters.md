---
description: DirectShow Filtros de captura de vídeo
ms.assetid: e4d1452d-ceac-4b5c-b9ba-ad4722ecff76
title: DirectShow Filtros de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cafe2815376ddb2a099c309228ba1bf24ae9315f305edb7312b88dd1196f82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966326"
---
# <a name="directshow-video-capture-filters"></a>DirectShow Filtros de captura de vídeo

Os filtros de captura DirectShow têm alguns recursos que os distinguem de outros tipos de filtros. Embora o [Capture Graph Builder](capture-graph-builder.md) oculta muitos dos detalhes, é uma boa ideia ler esta seção, para ter uma compreensão geral dos DirectShow de captura.

**Fixar categorias**

Um filtro de captura geralmente tem dois ou mais pinos de saída que entregam o mesmo tipo de dados, por exemplo, um pino de visualização e um pino de captura. Portanto, os tipos de mídia não são uma boa maneira de distinguir os pinos. Em vez disso, os pinos são diferenciados por sua funcionalidade, que é identificada usando um GUID, chamada de *categoria de pino*.

Para ver uma discussão sobre como consultar pins para sua categoria, consulte [Trabalhando com categorias de pino.](working-with-pin-categories.md) No entanto, para a maioria dos aplicativos, você não precisa consultar os pinos diretamente. Em vez disso, [**vários métodos ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) levam parâmetros que especificam a categoria de pino na qual operar. O Capture Graph Builder localiza automaticamente o pino correto.

**Pinos de visualização e pinos de captura**

Alguns dispositivos de captura de vídeo têm pinos de saída separados para visualização e captura. O pino de visualização é usado para renderizar vídeo na tela, enquanto o pin de captura é usado para gravar vídeo em um arquivo.

Um pin de visualização e um pin de captura têm as seguintes diferenças:

-   Um pino de visualização descarta quadros conforme necessário para manter a taxa de transferência no pino de captura.
-   Cada quadro de um pin de captura tem carimbo de data/hora com a hora do fluxo em que o quadro foi capturado. Um pin de visualização não marca o carimbo de data/hora dos exemplos que ele fornece.

O motivo pelo qual os quadros de visualização não têm carimbos de data/hora é que o grafo de filtro introduz uma pequena quantidade de latência no fluxo. Se o tempo de captura for usado como o tempo de apresentação, o renderador de vídeo tratará cada exemplo como um pouco atrasado. Isso pode fazer com que o renderador de vídeo solte quadros enquanto tenta se recuperar. A remoção dos carimbos de data/hora garante que o renderista apresente cada amostra quando chegar, sem remover quadros.

A categoria de pino para pinos de visualização é PIN \_ CATEGORY \_ PREVIEW. A categoria para pinos de captura é PIN \_ CATEGORY \_ CAPTURE.

**Pinos de porta de vídeo**

Uma porta de vídeo é uma conexão de hardware entre um dispositivo de vídeo (como um ajuste de TV análogo) e a placa de vídeo. Uma porta de vídeo permite que o dispositivo envie dados de vídeo diretamente para a placa gráfica. O vídeo é exibido na tela usando uma sobreposição de hardware. Uma porta de vídeo pode ser um cabo real que conecta dois dispositivos em cartões separados; ou pode ser uma conexão com fio no mesmo cartão.

A vantagem de uma porta de vídeo é que o vídeo entra diretamente na memória de vídeo, sem nenhum trabalho da CPU. No entanto, as portas de vídeo têm algumas desvantagens:

-   Uma porta de vídeo sempre usa a superfície de sobreposição durante a captura, independentemente de você querer visualizar o vídeo.
-   A invertia entre quadros ocorre automaticamente, o que dificulta a sincronização da inverta com outras operações de vídeo.

Se um dispositivo de captura usar uma porta de vídeo, o filtro de captura terá um pino de porta de vídeo em vez de um pino de visualização. A categoria de pino para pinos de porta de vídeo é PIN \_ CATEGORY \_ VIDEOPORT.

Cada filtro de captura tem pelo menos um pino de captura. Além disso, ele pode ter um pin de visualização ou um pino de porta de vídeo, mas nunca ambos. Os filtros podem ter vários pinos de captura e pinos de visualização, cada um fornecendo um tipo de mídia separado. Portanto, um único filtro pode ter um pino de captura de vídeo, um pino de visualização de vídeo, um pino de captura de áudio e um pino de visualização de áudio. (No entanto, não há nada equivalente a uma porta de vídeo para áudio.)

**Filtros WDM upstream**

Windows Dispositivos WDM (Modelo de Driver) podem exigir alguns filtros adicionais upstream do filtro de captura. Esses filtros incluem o seguinte:

-   [Filtro do tv tuner](tv-tuner-filter.md). Controla o ajuste para os tuners de TV análogos.
-   [Filtro de áudio de TV](tv-audio-filter.md). Controla as configurações de áudio para os ajustares de TV análogos.
-   [Filtro de barra cruzada de vídeo análogo](analog-video-crossbar-filter.md). Encaminha sinais de áudio e vídeo por meio do dispositivo de hardware. Por exemplo, um dispositivo pode ter várias entradas, como S-Video e vídeo composto. O filtro de barra cruzada permite que o aplicativo selecione a entrada.

Embora esses sejam filtros separados DirectShow, eles normalmente representam o mesmo dispositivo de hardware. Cada filtro controla uma função diferente do dispositivo. Os filtros são conectados por pinos, mas nenhum dado de mídia se move entre as conexões de pino. Portanto, os pinos nesses filtros não se conectam estabelecendo um tipo de mídia. Em vez disso, eles usam valores GUID chamados *médios.* GuiDs médios são definidos exclusivamente para um determinado minidriver de dispositivo. Por exemplo, o filtro Tv Tuner e o filtro captura de vídeo para a mesma placa de TV darão suporte à mesma mídia, o que permite que o aplicativo crie o grafo corretamente.

Na prática, desde que você use **ICaptureGraphBuilder2** para criar seus grafos de captura, esses filtros são adicionados ao grafo automaticamente. Para obter uma discussão mais detalhada, consulte [Filtros de driver de classe WDM](wdm-class-driver-filters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a Captura de Vídeo DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



