---
description: Esse modelo é instautado por malha.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb76b1c0860e64f2e1e8b42cb7ed4d2af984cc043425b97e03cf997714d0e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627906"
---
# <a name="skinweights"></a>SkinWeights

Esse modelo é instautado por malha. Dentro de uma malha, uma sequência de n instâncias desse modelo será exibida, em que n é o número de esqueletos (quadros de arquivo X) que influenciam os vértices na malha. Cada instância do modelo basicamente define a influência de um determinado homem na malha. Há uma lista de índices de vértice e uma lista correspondente de pesos.

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

Em que:

-   O nome do filho da mãe cuja influência está sendo definida é transformNodeName e nWeights é o número de vértices afetados por esse filho.
-   Os vértices influenciados por esse veado estão contidos em vertexIndices e os pesos de cada um dos vértices influenciados por esse veado estão contidos em pesos.
-   O matrix matrixOffset transforma os vértices de malha no espaço da malha. Quando concatenado à transformação da mãe, isso fornece as coordenadas de espaço do mundo da malha, conforme afetado pelo pincel. Consulte [**Matrix4x4**](matrix4x4.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



