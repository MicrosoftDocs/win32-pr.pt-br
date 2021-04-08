---
description: Todos os ponteiros retornados pelas funções de infraestrutura de pares devem ser liberados usando PeerGraphFreeData ou PeerFreeData.
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: Liberando dados de pares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1addb0533d5d05e329e19bfe27a89f5616473a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011027"
---
# <a name="freeing-peer-data"></a><span data-ttu-id="bb69c-103">Liberando dados de pares</span><span class="sxs-lookup"><span data-stu-id="bb69c-103">Freeing Peer Data</span></span>

<span data-ttu-id="bb69c-104">Todos os ponteiros retornados pelas funções de infraestrutura de pares devem ser liberados usando [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) ou [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span><span class="sxs-lookup"><span data-stu-id="bb69c-104">All pointers that the Peer Infrastructure functions return must be freed by using [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span> <span data-ttu-id="bb69c-105">Essas funções devem ser chamadas somente para estruturas que são retornadas diretamente por uma função de infraestrutura de mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="bb69c-105">These functions must only be called for structures that are directly returned by a Peer Infrastructure function.</span></span> <span data-ttu-id="bb69c-106">Não chame uma função FreeData diferente para liberar ponteiros aninhados, por exemplo, não chame uma função FreeData nos ponteiros em uma estrutura de [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="bb69c-106">Do not call a different FreeData function to free nested pointers, for example, do not call a FreeData function on the pointers in a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span>

## <a name="example-of-freeing-data"></a><span data-ttu-id="bb69c-107">Exemplo de liberação de dados</span><span class="sxs-lookup"><span data-stu-id="bb69c-107">Example of Freeing Data</span></span>

<span data-ttu-id="bb69c-108">O trecho de código a seguir mostra como recuperar as propriedades associadas a um grafo e, em seguida, liberar os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="bb69c-108">The following code snippet shows you how to retrieve the properties associated with a graph, and then free the data that is returned.</span></span>


```C++
PEER_GRAPH_PROPERTIES  * pGraphProperties = NULL;
HRESULT hr = PeerGraphGetProperties(hGraph, &pGraphProperties);
if (SUCCEEDED(hr) && (NULL != pGraphProperties))
{
  // use pGraphProperties
  wprintf(L"%d\n", pGraphProperties->pwzGraphId);

  // release the data
  PeerGraphFreeData(pGraphProperties);
}
```



 

 



