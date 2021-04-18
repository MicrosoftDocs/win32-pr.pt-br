---
description: Os recursos do buffer de vértice gerenciados ou do buffer de índice não podem ser declarados dinâmicos especificando D3DUSAGE \_ dinâmico no momento da criação.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed de recursos e estratégias de alocação (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814048"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a>Application-Managed de recursos e estratégias de alocação (Direct3D 9)

Os recursos do buffer de vértice gerenciados ou do buffer de índice não podem ser declarados dinâmicos especificando D3DUSAGE \_ dinâmico no momento da criação. Isso exigiria uma cópia adicional para cada modificação no conteúdo do buffer de vértice. Os buffers de vértice dinâmicos destinam-se a renderizar a geometria dinâmica e os dados extraídos de árvores particionadas de espaço binário ou outras estruturas de dados de visibilidade. Isso pode ser feito por meio da alocação de buffers do formato desejado. Esses recursos são então incluídos para dar suporte às necessidades do aplicativo por um Gerenciador de recursos dentro do aplicativo. O número total de buffers de vértice dinâmicos é pequeno, pois um aplicativo usará simultaneamente apenas alguns passos de vértice diferentes e porque um buffer de vértice diferente é necessário apenas para um único trajeto. Ao gerenciar recursos dinâmicos dessa forma, certifique-se de que as demandas de alta frequência nos recursos não diminuem significativamente o desempenho do aplicativo.

Ao usar recursos gerenciados pelo Direct3D e por aplicativos, aloque recursos gerenciados por aplicativo na \_ memória padrão do D3DPOOL antes de criar recursos gerenciados por Direct3D. Isso permite que o Gerenciador de memória mantenha uma contagem precisa da memória disponível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



