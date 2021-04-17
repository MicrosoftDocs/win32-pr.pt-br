---
description: Esse modelo é instanciado em uma base por malha, mantendo informações sobre quais vértices na malha são duplicados uns dos outros.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d62278c206032c9a2dfed6ce9b2cd36c5e7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105764088"
---
# <a name="vertexduplicationindices"></a>VertexDuplicationIndices

Esse modelo é instanciado em uma base por malha, mantendo informações sobre quais vértices na malha são duplicados uns dos outros. Duplicatas resultam quando um vértice fica em um grupo de suavização ou em um limite de material. A finalidade deste modelo é permitir que o carregador determine quais vértices que apresentam parâmetros periféricos diferentes são, na verdade, os mesmos vértices no modelo. Determinados aplicativos (simplificação de malha, por exemplo) podem fazer uso dessas informações.

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

Em que:

-   nIndices-número de índices de vértice. Este é o número de vértices na malha.
-   nOriginalVertices-número de vértices na malha antes de qualquer duplicação ocorrer.
-   Os índices de valor \[ n \] contêm o índice de vértices que o vértice \[ n \] na matriz de vértices para a malha teria tido se nenhuma duplicação tivesse ocorrido. Os índices nessa matriz são os mesmos, portanto, indicam vértices duplicados.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



