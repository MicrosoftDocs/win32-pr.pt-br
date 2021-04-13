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
# <a name="xskinmeshheader"></a><span data-ttu-id="abe61-104">XSkinMeshHeader</span><span class="sxs-lookup"><span data-stu-id="abe61-104">XSkinMeshHeader</span></span>

<span data-ttu-id="abe61-105">Esse modelo é instanciado em uma base por malha somente em malhas que contêm informações de aparência exportadas.</span><span class="sxs-lookup"><span data-stu-id="abe61-105">This template is instantiated on a per-mesh basis only in meshes that contain exported skinning information.</span></span> <span data-ttu-id="abe61-106">A finalidade deste modelo é fornecer informações sobre a natureza das informações de revestimento que foram exportadas.</span><span class="sxs-lookup"><span data-stu-id="abe61-106">The purpose of this template is to provide information about the nature of the skinning information that was exported.</span></span>

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

<span data-ttu-id="abe61-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="abe61-107">Where:</span></span>

-   <span data-ttu-id="abe61-108">nMaxSkinWeightsPerVertex – número máximo de transformações que afetam um vértice na malha.</span><span class="sxs-lookup"><span data-stu-id="abe61-108">nMaxSkinWeightsPerVertex - Maximum number of transforms that affect a vertex in the mesh.</span></span>
-   <span data-ttu-id="abe61-109">nMaxSkinWeightsPerFace – número máximo de transformações exclusivas que afetam os três vértices de qualquer face.</span><span class="sxs-lookup"><span data-stu-id="abe61-109">nMaxSkinWeightsPerFace - Maximum number of unique transforms that affect the three vertices of any face.</span></span>
-   <span data-ttu-id="abe61-110">nBones-número de Bones que afetam os vértices nesta malha.</span><span class="sxs-lookup"><span data-stu-id="abe61-110">nBones - Number of bones that affect vertices in this mesh.</span></span>

## <a name="see-also"></a><span data-ttu-id="abe61-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="abe61-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe61-112">Modelos</span><span class="sxs-lookup"><span data-stu-id="abe61-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



