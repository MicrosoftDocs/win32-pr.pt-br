---
description: Horas do Relógio
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Horas do Relógio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0075dc2d8c2273c8ade612244f0f7d551996756e55000043ffe3bc952227fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402066"
---
# <a name="clock-times"></a>Horas do Relógio

DirectShow define dois horários de relógio relacionados: hora de referência e hora de fluxo.

-   *A hora de* referência é a hora absoluta retornada pelo relógio de referência. (Consulte [Relógios de Referência](reference-clocks.md).)
-   *O tempo de* fluxo é definido em relação ao momento em que o grafo começou a ser executado pela última vez.
    -   Enquanto o grafo está em execução, o tempo de fluxo é igual à hora de referência menos a hora de início.
    -   Enquanto o grafo está em pausa, o tempo de fluxo permanece no momento do fluxo quando ele foi pausado.
    -   Após uma operação de busca, o tempo de fluxo é redefinido como zero.
    -   Enquanto o grafo é interrompido, o tempo de fluxo é indefinido.

Quando um exemplo de mídia tem um carimbo de data/hora *t*, isso significa que o exemplo deve ser renderizado no tempo de *fluxo t*. Por esse motivo, a hora do fluxo também é chamada *de hora de apresentação.*

Quando um aplicativo chama [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para executar o grafo de filtro, o Gerenciador de Graph filtros chama [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) em cada filtro. Para compensar a pequena quantidade de tempo que leva para que os filtros comecem a ser executados, o Gerenciador Graph Filtro especifica uma hora de início um pouco no futuro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hora e relógios em DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Carimbos de Data/Hora](time-stamps.md)
</dt> </dl>

 

 



