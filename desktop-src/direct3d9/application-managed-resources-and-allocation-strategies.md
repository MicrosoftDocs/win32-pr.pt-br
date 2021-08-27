---
description: Recursos de buffer de vértice gerenciado ou buffer de índice não podem ser declarados dinâmicos especificando D3DUSAGE \_ DYNAMIC no momento da criação.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed recursos e estratégias de alocação (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86eabccde7fef025c952c869a30fdeff8cf5316ceb0316b513692175d8581a01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119426"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a>Application-Managed recursos e estratégias de alocação (Direct3D 9)

Recursos de buffer de vértice gerenciado ou buffer de índice não podem ser declarados dinâmicos especificando D3DUSAGE \_ DYNAMIC no momento da criação. Isso exigiria uma cópia adicional para cada modificação no conteúdo do buffer de vértice. Buffers de vértice dinâmico são destinados à renderização de geometria dinâmica e dados retirados de árvores particionadas de espaço binário ou outras estruturas de dados de visibilidade. Isso pode ser feito alocando previamente buffers do formato desejado. Esses recursos são então organizados para dar suporte às necessidades do aplicativo por um gerenciador de recursos dentro do aplicativo. O número total de buffers de vértice dinâmico é pequeno porque um aplicativo usará simultaneamente apenas algumas passadas de vértice diferentes e porque um buffer de vértice diferente é necessário apenas para passadas exclusivas. Ao gerenciar recursos dinâmicos dessa maneira, verifique se as demandas de alta frequência nos recursos não diminuem significativamente o desempenho do aplicativo.

Ao usar recursos gerenciados pelo Direct3D e aplicativos, aloce recursos gerenciados pelo aplicativo na memória DEFAULT do D3DPOOL antes de criar recursos gerenciados pelo \_ Direct3D. Isso permite que o gerenciador de memória mantenha uma contagem precisa de memória disponível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



