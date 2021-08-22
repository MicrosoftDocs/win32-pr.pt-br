---
description: Esse modelo é instariado por malha somente em malhas que contêm informações de decodagem exportadas. A finalidade desse modelo é fornecer informações sobre a natureza das informações de reação que foram exportadas.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c86127e46809cd1415b191a769b25e09535405e6500e511df6248e6174888d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796850"
---
# <a name="xskinmeshheader"></a>XSkinMeshHeader

Esse modelo é instariado por malha somente em malhas que contêm informações de decodagem exportadas. A finalidade desse modelo é fornecer informações sobre a natureza das informações de reação que foram exportadas.

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

-   nMaxSkinWeightsPerVertex – Número máximo de transformação que afetam um vértice na malha.
-   nMaxSkinWeightsPerFace – Número máximo de transformações exclusivas que afetam os três vértices de qualquer face.
-   nBones – número de esqueletos que afetam os vértices nesta malha.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



