---
description: Esse modelo é instanciado em uma base por malha somente em malhas que contêm informações de aparência exportadas. A finalidade deste modelo é fornecer informações sobre a natureza das informações de revestimento que foram exportadas.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306f8c183086846fca020040af00b9ccef2665cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370283"
---
# <a name="xskinmeshheader"></a>XSkinMeshHeader

Esse modelo é instanciado em uma base por malha somente em malhas que contêm informações de aparência exportadas. A finalidade deste modelo é fornecer informações sobre a natureza das informações de revestimento que foram exportadas.

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

Em que:

-   nMaxSkinWeightsPerVertex – número máximo de transformações que afetam um vértice na malha.
-   nMaxSkinWeightsPerFace – número máximo de transformações exclusivas que afetam os três vértices de qualquer face.
-   nBones-número de Bones que afetam os vértices nesta malha.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



