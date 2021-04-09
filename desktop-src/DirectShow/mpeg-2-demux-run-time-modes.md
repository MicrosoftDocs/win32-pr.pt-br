---
description: Modos de Run-Time Demux MPEG-2
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: Modos de Run-Time Demux MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087838"
---
# <a name="mpeg-2-demux-run-time-modes"></a>Modos de Run-Time Demux MPEG-2

O [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) ("Demux") pode operar no modo de Push ou no modo de pull. No modo de push, os dados são provenientes de uma fonte dinâmica, como uma difusão de rede. No modo de pull, os dados vêm de um arquivo local.

-   O modo de pull está disponível no Windows XP e posterior, somente para fluxos de programa. Em plataformas de nível inferior, use o filtro [divisor MPEG-2](mpeg-2-splitter.md) .
-   O modo de Push está disponível em todas as plataformas, para fluxos de programa e fluxos de transporte.

O Demux, portanto, dá suporte a três modos possíveis: fluxos de programa no modo de pull, fluxos de programa no modo de push e fluxos de transporte no modo de push. O Demux determina qual modo usar em tempo de execução. O modo é determinado quando o PIN de entrada se conecta ou quando o primeiro PIN de saída é configurado, o que acontecer primeiro:

-   Quando o PIN de entrada se conecta: no Windows XP e posterior, o Demux consulta o filtro upstream para a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ; Se o filtro upstream expõe essa interface, o Demux se configura para fluxos de programa no modo de pull. Caso contrário, o Demux usará o modo de push e o tipo de mídia determinará o tipo de fluxo (fluxo do programa ou fluxo de transporte). Consulte [**tipos de mídia do demultiplexador MPEG-2**](mpeg-2-demultiplexer-media-types.md) para obter uma lista de tipos de entrada.
-   Quando o primeiro PIN de saída estiver configurado: se você criar um PIN de saída e consultá-lo para [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), o Demux se configurará para fluxos de transporte no modo de push. Se você consultar o PIN para [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), o Demux se configurará para fluxos de programa, também no modo de push. Todas as consultas subsequentes para a outra interface falham, porque o Demux não pode operar em dois modos de uma vez.

Depois que o Demux tiver se configurado para um modo específico, ele permanecerá nesse modo. Para usar um modo diferente, você deve criar uma nova instância do Demux.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



