---
title: Usando tabelas de descritores
description: As tabelas de descritores, cada uma identificando um intervalo em um heap de descritor, são associadas a Slots definidos pela assinatura raiz atual em uma lista de comandos.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104019"
---
# <a name="using-descriptor-tables"></a>Usando tabelas de descritores

As tabelas de descritores, cada uma identificando um intervalo em um heap de descritor, são associadas a Slots definidos pela assinatura raiz atual em uma lista de comandos.

-   [Indexando tabelas de descritores](#indexing-descriptor-tables)
-   [Tópicos relacionados](#related-topics)

Os sombreadores podem localizar recursos referenciados pelos descritores que compõem a tabela de descritores. Outras associações de recurso-buffers de índice, buffer de vértice, buffers de saída de fluxo, destinos de renderização e estêncil de profundidade são feitos diretamente em uma lista de comandos em vez de por meio de descritores. Para resumir:

As referências de recurso a seguir podem compartilhar a mesma tabela e heap de descritores:

-   Exibições de recursos do sombreador
-   Exibições de acesso não ordenado
-   Exibições de buffer de constantes

As seguintes referências de recurso devem estar em seu próprio heap de descritor:

-   Amostradores

Os recursos a seguir não são colocados em tabelas de descritores ou heaps, mas são associados diretamente usando listas de comandos:

-   Buffers de índice
-   Buffers de vértice
-   Buffers de saída de fluxo
-   Destinos de renderização
-   Exibições de estêncil de profundidade

## <a name="indexing-descriptor-tables"></a>Indexando tabelas de descritores

Os sombreadores não podem indexar dinamicamente os limites da tabela do descritor de um determinado site de chamada no sombreador. No entanto, a seleção de um descritor dentro de uma tabela de descritores pode ser indexada dinamicamente no código do sombreador dentro dos intervalos do mesmo tipo de descritor (como indexação em uma região contígua de SRVs).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabelas de descritores](descriptor-tables.md)
</dt> </dl>

 

 




