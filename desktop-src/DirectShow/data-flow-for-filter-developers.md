---
description: Dados Flow para desenvolvedores de filtro
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Dados Flow para desenvolvedores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ced9507856d7a6b8aea2acaea86c20b393b8d937ab4427bf522596a29ba690
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749366"
---
# <a name="data-flow-for-filter-developers"></a>Dados Flow para desenvolvedores de filtro

Esta seção descreve detalhadamente como os dados se movem pelo grafo de filtro. Ele se concentra no transporte de memória local usando a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**ou IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) Ele destina-se a desenvolvedores que estão escrevendo seus próprios filtros personalizados. Para uma introdução geral sobre como o Microsoft DirectShow lida com o fluxo de dados, consulte Data [Flow no filtro Graph](data-flow-in-the-filter-graph.md).

Muitos dados se movem por um grafo de filtro. Ele se enquadra aproximadamente em duas categorias: dados de mídia e dados de controle. Em geral, os dados de mídia viajam downstream e os dados de controle viajam para cima. Os dados de mídia incluem os quadros de vídeo, exemplos de áudio, pacotes MPEG e assim por diante que comem um fluxo, mas também inclui comandos de liberação, notificações de fim de fluxo e outros dados que viajam com o fluxo. Os dados de controle não fazem parte do fluxo de mídia. Exemplos de dados de controle são solicitações de controle de qualidade e comandos de busca.

Esta seção contém os artigos a seguir.

-   [Entregando exemplos](delivering-samples.md)
-   [Processando dados](processing-data.md)
-   [Notificações de fim de fluxo](end-of-stream-notifications.md)
-   [Novos segmentos](new-segments.md)
-   [Liberando](flushing.md)
-   [Procurando](seeking.md)
-   [Alterações de formato dinâmico](dynamic-format-changes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de controle de qualidade](quality-control-management.md)
</dt> <dt>

[Threads e seções críticas](threads-and-critical-sections.md)
</dt> <dt>

[Escrevendo DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



