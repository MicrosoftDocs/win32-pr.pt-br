---
description: Todos os ponteiros retornados pelas funções de infraestrutura de pares devem ser liberados usando PeerGraphFreeData ou PeerFreeData.
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: Liberando dados de pares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9492fec9a22da8252188a75d6d4cee73d2055d29f47e25fc7d55a26cc7909c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794573"
---
# <a name="freeing-peer-data"></a>Liberando dados de pares

Todos os ponteiros retornados pelas funções de infraestrutura de pares devem ser liberados usando [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) ou [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata). Essas funções devem ser chamadas somente para estruturas que são retornadas diretamente por uma função de infraestrutura de mesmo nível. Não chame uma função FreeData diferente para liberar ponteiros aninhados, por exemplo, não chame uma função FreeData nos ponteiros em uma estrutura de [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record) .

## <a name="example-of-freeing-data"></a>Exemplo de liberação de dados

O trecho de código a seguir mostra como recuperar as propriedades associadas a um grafo e, em seguida, liberar os dados retornados.


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



 

 



