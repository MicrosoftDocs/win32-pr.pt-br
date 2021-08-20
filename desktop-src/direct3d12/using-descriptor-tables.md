---
title: Como usar tabelas de descritores
description: As tabelas de descritor, cada uma identificando um intervalo em um heap de descritor, são vinculadas a slots definidos pela assinatura raiz atual em uma lista de comandos.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f94c83adb655e9d2d13ba3f482aa225a5021a18dbd8fcecb165ad13df47b4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911920"
---
# <a name="using-descriptor-tables"></a>Como usar tabelas de descritores

As tabelas de descritor, cada uma identificando um intervalo em um heap de descritor, são vinculadas a slots definidos pela assinatura raiz atual em uma lista de comandos.

-   [Indexando tabelas de descritor](#indexing-descriptor-tables)
-   [Tópicos relacionados](#related-topics)

Os sombreadores podem localizar recursos referenciados pelos descritores que comem a tabela do descritor. Outras vinculações de recursos – Buffers de Índice, Buffer de Vértice, Buffers de Saída de Fluxo, Destinos de Renderização e Estêncil de Profundidade são feitas diretamente em uma lista de comandos em vez de por meio de descritores. Para resumir:

As seguintes referências de recurso podem compartilhar a mesma tabela de descritor e heap:

-   Exibições de recursos do sombreador
-   Exibições de acesso não organizado
-   Exibições de buffer constante

As seguintes referências de recurso devem estar em seu próprio heap de descritor:

-   Amostradores

Os recursos a seguir não são colocados em tabelas de descritor ou heaps, mas são vinculados diretamente usando listas de comandos:

-   Buffers de índice
-   Buffers de vértice
-   Buffers de saída de fluxo
-   Renderizar destinos
-   Exibições de estêncil de profundidade

## <a name="indexing-descriptor-tables"></a>Indexando tabelas de descritor

Os sombreadores não podem indexar dinamicamente entre os limites da tabela do descritor de um determinado site de chamada no sombreador. No entanto, a seleção de um descritor em uma tabela de descritor pode ser indexada dinamicamente no código do sombreador dentro de intervalos do mesmo tipo de descritor (como indexação em uma região contígua de SRVs).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabelas de descritores](descriptor-tables.md)
</dt> </dl>

 

 




