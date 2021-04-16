---
description: Atingir
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: Atingir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104549941"
---
# <a name="seeking"></a>Atingir

Os filtros dão suporte à busca por meio da interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . O aplicativo consulta o Gerenciador de gráfico de filtro para **IMediaSeeking** e o usa para emitir comandos de busca. O Gerenciador de gráfico de filtro distribui cada comando de busca para todos os filtros de processador no grafo. Cada renderizador passa o comando upstream, por meio dos Pins de saída dos filtros upstream, até alcançar um filtro que possa executar a busca. Normalmente, um filtro de origem ou um filtro de analisador, como o [divisor AVI](avi-splitter-filter.md), executa a operação de busca.

Quando um filtro executa uma operação de busca, ele libera todos os dados pendentes. O resultado é minimizar a latência de comandos de busca, pois os dados existentes são liberados do grafo. Após um comando de busca, o tempo de fluxo é redefinido como zero.

O diagrama a seguir ilustra a sequência de eventos.

![sequência de eventos](images/seeking.png)

Se um filtro do analisador tiver mais de um pino de saída, ele normalmente designará um deles para aceitar comandos de busca. Os outros Pins rejeitam ou ignoram os comandos de busca recebidos. Dessa forma, o analisador mantém todos os seus fluxos sincronizados. No entanto, todos os Pins de saída devem implementar [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) e [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) para retornar os recursos de busca do filtro. Isso garante que o Gerenciador de gráfico de filtro retorne o valor correto para o aplicativo.

A interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) foi preterida para filtros. Os clientes de automação ainda precisam usar essa interface no Gerenciador de gráficos de filtro, porque **IMediaSeeking** não é compatível com a automação, mas o Gerenciador de grafo de filtro converte todas as chamadas **IMediaPosition** em chamadas **IMediaSeeking** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Liberação](flushing.md)
</dt> <dt>

[Tempo e relógios no DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



