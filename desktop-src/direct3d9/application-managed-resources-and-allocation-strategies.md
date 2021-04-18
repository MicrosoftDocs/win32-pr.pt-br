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
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a><span data-ttu-id="8583d-103">Application-Managed de recursos e estratégias de alocação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8583d-103">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>

<span data-ttu-id="8583d-104">Os recursos do buffer de vértice gerenciados ou do buffer de índice não podem ser declarados dinâmicos especificando D3DUSAGE \_ dinâmico no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="8583d-104">Managed vertex-buffer or index-buffer resources cannot be declared dynamic by specifying D3DUSAGE\_DYNAMIC at creation time.</span></span> <span data-ttu-id="8583d-105">Isso exigiria uma cópia adicional para cada modificação no conteúdo do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="8583d-105">This would require an additional copy for every modification to the vertex buffer contents.</span></span> <span data-ttu-id="8583d-106">Os buffers de vértice dinâmicos destinam-se a renderizar a geometria dinâmica e os dados extraídos de árvores particionadas de espaço binário ou outras estruturas de dados de visibilidade.</span><span class="sxs-lookup"><span data-stu-id="8583d-106">Dynamic vertex buffers are intended for rendering dynamic geometry and data pulled in from binary space partitioned trees or other visibility data structures.</span></span> <span data-ttu-id="8583d-107">Isso pode ser feito por meio da alocação de buffers do formato desejado.</span><span class="sxs-lookup"><span data-stu-id="8583d-107">This can be accomplished by pre-allocating buffers of the desired format.</span></span> <span data-ttu-id="8583d-108">Esses recursos são então incluídos para dar suporte às necessidades do aplicativo por um Gerenciador de recursos dentro do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8583d-108">These resources are then parceled out to support application needs by a resource manager within the application.</span></span> <span data-ttu-id="8583d-109">O número total de buffers de vértice dinâmicos é pequeno, pois um aplicativo usará simultaneamente apenas alguns passos de vértice diferentes e porque um buffer de vértice diferente é necessário apenas para um único trajeto.</span><span class="sxs-lookup"><span data-stu-id="8583d-109">The total number of dynamic vertex buffers is small because an application will use simultaneously only a few different vertex strides and because a different vertex buffer is required only for unique strides.</span></span> <span data-ttu-id="8583d-110">Ao gerenciar recursos dinâmicos dessa forma, certifique-se de que as demandas de alta frequência nos recursos não diminuem significativamente o desempenho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8583d-110">When managing dynamic resources in this way, ensure that high-frequency demands on the resources do not significantly decrease the application's performance.</span></span>

<span data-ttu-id="8583d-111">Ao usar recursos gerenciados pelo Direct3D e por aplicativos, aloque recursos gerenciados por aplicativo na \_ memória padrão do D3DPOOL antes de criar recursos gerenciados por Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8583d-111">When using resources managed by both Direct3D and applications, allocate application-managed resources in D3DPOOL\_DEFAULT memory prior to creating Direct3D-managed resources.</span></span> <span data-ttu-id="8583d-112">Isso permite que o Gerenciador de memória mantenha uma contagem precisa da memória disponível.</span><span class="sxs-lookup"><span data-stu-id="8583d-112">This enables the memory manager to maintain an accurate count of available memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8583d-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8583d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8583d-114">Recursos do Direct3D</span><span class="sxs-lookup"><span data-stu-id="8583d-114">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



