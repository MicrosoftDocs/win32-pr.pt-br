---
description: Horas de relógio
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Horas de relógio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370093"
---
# <a name="clock-times"></a>Horas de relógio

O DirectShow define dois tempos de relógio relacionados: tempo de referência e tempo de transmissão.

-   A *hora de referência* é o tempo absoluto retornado pelo relógio de referência. (Consulte [relógios de referência](reference-clocks.md).)
-   O *tempo de transmissão* é definido em relação ao momento em que o grafo foi iniciado pela última vez.
    -   Enquanto o grafo está em execução, o fluxo de tempo é igual ao tempo de referência menos a hora de início.
    -   Enquanto o grafo está em pausa, o tempo de transmissão permanece no momento da transmissão quando ele estava em pausa.
    -   Após uma operação de busca, o tempo de fluxo é redefinido como zero.
    -   Enquanto o grafo é interrompido, o tempo de transmissão é indefinido.

Quando um exemplo de mídia tem um carimbo de data/hora *t*, isso significa que o exemplo deve ser renderizado em tempo *t* do fluxo. Por esse motivo, o tempo de fluxo também é chamado de *tempo de apresentação*.

Quando um aplicativo chama [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para executar o gráfico de filtro, o Gerenciador de gráfico de filtro chama [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) em cada filtro. Para compensar a ligeira quantidade de tempo que leva para que os filtros comecem a ser executados, o Gerenciador de grafo de filtro especifica uma hora de início um pouco no futuro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tempo e relógios no DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Carimbos de Data/Hora](time-stamps.md)
</dt> </dl>

 

 



