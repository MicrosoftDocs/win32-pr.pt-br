---
description: Horas de relógio
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Horas de relógio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0075dc2d8c2273c8ade612244f0f7d551996756e55000043ffe3bc952227fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402066"
---
# <a name="clock-times"></a>Horas de relógio

DirectShow define dois tempos de relógio relacionados: tempo de referência e tempo de transmissão.

-   A *hora de referência* é o tempo absoluto retornado pelo relógio de referência. (Consulte [relógios de referência](reference-clocks.md).)
-   O *tempo de transmissão* é definido em relação ao momento em que o grafo foi iniciado pela última vez.
    -   Enquanto o grafo está em execução, o fluxo de tempo é igual ao tempo de referência menos a hora de início.
    -   Enquanto o grafo está em pausa, o tempo de transmissão permanece no momento da transmissão quando ele estava em pausa.
    -   Após uma operação de busca, o tempo de fluxo é redefinido como zero.
    -   Enquanto o grafo é interrompido, o tempo de transmissão é indefinido.

Quando um exemplo de mídia tem um carimbo de data/hora *t*, isso significa que o exemplo deve ser renderizado em tempo *t* do fluxo. Por esse motivo, o tempo de fluxo também é chamado de *tempo de apresentação*.

quando um aplicativo chama [**IMediaControl:: run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para executar o gráfico de filtro, o filtro Graph Manager chama [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) em cada filtro. para compensar a ligeira quantidade de tempo que leva para que os filtros comecem a ser executados, o filtro Graph Manager especifica uma hora de início um pouco no futuro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tempo e relógios no DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Carimbos de Data/Hora](time-stamps.md)
</dt> </dl>

 

 



