---
description: Esse modelo é instanciado em uma base por malha.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759239a3a7ec8ebb608cf9ede6624105cee321b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500258"
---
# <a name="skinweights"></a>SkinWeights

Esse modelo é instanciado em uma base por malha. Em uma malha, uma sequência de n instâncias desse modelo será exibida, em que n é o número de Bones (X quadros de arquivo) que influenciam os vértices na malha. Cada instância do modelo basicamente define a influência de um Bone específico na malha. Há uma lista de índices de vértice e uma lista correspondente de pesos.

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

-   O nome do Bone cuja influência está sendo definida é transformNodeName e nWeights é o número de vértices afetados por esse Bone.
-   Os vértices influenciados por esse Bone estão contidos em vertexIndices, e os pesos para cada um dos vértices influenciados por esse Bone estão contidos em pesos.
-   A matriz matrixOffset transforma os vértices de malha no espaço do Bone. Quando concatenada com a transformação do Bone, isso fornece as coordenadas de espaço do mundo da malha, conforme afetado pelo Bone. Consulte [**Matrix4x4**](matrix4x4.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



