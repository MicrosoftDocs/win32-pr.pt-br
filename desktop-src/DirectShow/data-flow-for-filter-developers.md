---
description: Fluxo de dados para os desenvolvedores de filtro
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Fluxo de dados para os desenvolvedores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010058"
---
# <a name="data-flow-for-filter-developers"></a>Fluxo de dados para os desenvolvedores de filtro

Esta seção descreve detalhadamente como os dados são movidos pelo grafo de filtro. Ele se concentra no transporte de memória local usando a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ou [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Ele é destinado a desenvolvedores que estão escrevendo seus próprios filtros personalizados. Para obter uma introdução geral sobre como o Microsoft DirectShow lida com o fluxo de dados, consulte [fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md).

Muitos dados se movem por um grafo de filtro. Ele se encaixa basicamente em duas categorias: dados de mídia e dados de controle. Em geral, os dados de mídia viajam por downstream e controlam upstream. Os dados de mídia incluem quadros de vídeo, amostras de áudio, pacotes MPEG e assim por diante que compõem um fluxo, mas também incluem comandos de liberação, notificações de fim de fluxo e outros dados que trafegam com o fluxo. Os dados de controle não fazem parte do fluxo de mídia. Exemplos de dados de controle são solicitações de controle de qualidade e comandos de busca.

Esta seção contém os artigos a seguir.

-   [Entregando exemplos](delivering-samples.md)
-   [Processando dados](processing-data.md)
-   [Notificações de fim de fluxo](end-of-stream-notifications.md)
-   [Novos segmentos](new-segments.md)
-   [Liberação](flushing.md)
-   [Atingir](seeking.md)
-   [Alterações de formato dinâmico](dynamic-format-changes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de controle de qualidade](quality-control-management.md)
</dt> <dt>

[Threads e seções críticas](threads-and-critical-sections.md)
</dt> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



