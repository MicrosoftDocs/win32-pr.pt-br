---
description: FaceAdjacency-este modelo é instanciado por malha, mantendo informações sobre quais vértices na malha são duplicados uns dos outros.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0508b822f45c6796a793dc4b17caeaa1e30b4c3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090504"
---
# <a name="faceadjacency"></a>FaceAdjacency

Esse modelo é instanciado em uma base por malha, mantendo informações sobre quais vértices na malha são duplicados uns dos outros. Duplicatas resultam quando um vértice fica em um grupo de suavização ou em um limite de material. A finalidade deste modelo é permitir que o carregador determine quais vértices que apresentam parâmetros periféricos diferentes são, na verdade, os mesmos vértices no modelo. Determinados aplicativos (simplificação de malha, por exemplo) podem fazer uso dessas informações.

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

Em que:

-   nIndices-número de índices na malha.
-   índices \[ nIndices \] -matriz de índices.

## <a name="see-also"></a>Consulte também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



