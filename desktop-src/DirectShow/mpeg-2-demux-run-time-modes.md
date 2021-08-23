---
description: Modos de Run-Time MPEG-2
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: Modos de Run-Time MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0bffe5f58a18ae9e935985e8dae8dc340c3895bd2dc1a2a89965355832e701f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072960"
---
# <a name="mpeg-2-demux-run-time-modes"></a>Modos de Run-Time MPEG-2

O [Demultiplexer MPEG-2](mpeg-2-demultiplexer.md) ("demux") pode operar no modo de push ou no modo de pull. No modo de push, os dados vêm de uma fonte ao vivo, como uma difusão de rede. No modo de pull, os dados vêm de um arquivo local.

-   O modo de pull está disponível no Windows XP e posterior, somente para fluxos de programas. Em plataformas de nível inferior, use o [filtro Divisor MPEG-2.](mpeg-2-splitter.md)
-   O modo de push está disponível em todas as plataformas para fluxos de programas e fluxos de transporte.

Portanto, o demux dá suporte a três modos possíveis: fluxos de programas no modo de pull, fluxos de programa no modo de push e fluxos de transporte no modo de push. O demux determina qual modo usar em tempo de operação. O modo é determinado quando o pino de entrada se conecta ou quando o primeiro pino de saída é configurado, o que ocorrer primeiro:

-   Quando o pino de entrada se conecta: no Windows XP e posterior, o demux consulta o filtro upstream para a interface [**IAsyncReader;**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) se o filtro upstream expõe essa interface, o demux configura-se para fluxos de programa no modo de pull. Caso contrário, o demux usa o modo de push e o tipo de mídia determina o tipo de fluxo (fluxo de programa ou fluxo de transporte). Consulte [**MpEG-2 Demultiplexer Media Types**](mpeg-2-demultiplexer-media-types.md) para ver uma lista de tipos de entrada.
-   Quando o primeiro pino de saída é configurado: se você criar um pino de saída e o consultar para [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), o demux configurará a si mesmo para fluxos de transporte no modo de push. Se você consultar o pin para [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), o demux se configurará para fluxos de programa, também no modo de push. As consultas subsequentes para a outra interface falham, porque o demux não pode operar em dois modos ao mesmo tempo.

Depois que o demux tiver se configurado para um modo específico, ele permanecerá nesse modo. Para usar um modo diferente, você deve criar uma nova instância do demux.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



