---
description: Descreve uma declaração de vértice.
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: DeclData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a26d667f853db3044db3155c55eb4a6d941c6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456473"
---
# <a name="decldata"></a><span data-ttu-id="fda24-103">DeclData</span><span class="sxs-lookup"><span data-stu-id="fda24-103">DeclData</span></span>

<span data-ttu-id="fda24-104">Descreve uma declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="fda24-104">Describes a vertex declaration.</span></span>

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="fda24-105">Em que:</span><span class="sxs-lookup"><span data-stu-id="fda24-105">Where:</span></span>

-   <span data-ttu-id="fda24-106">nElements-número de elementos de declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="fda24-106">nElements - Number of vertex declaration elements.</span></span>
-   <span data-ttu-id="fda24-107">Elements \[ nElements \] -matriz de elementos de declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="fda24-107">Elements\[nElements\] - Array of vertex declaration elements.</span></span>
-   <span data-ttu-id="fda24-108">nDWords-número de DWORDs.</span><span class="sxs-lookup"><span data-stu-id="fda24-108">nDWords - Number of DWORDS.</span></span>
-   <span data-ttu-id="fda24-109">Data \[ nDWords \] -matriz de DWORDs que contêm os dados em cada elemento Vertex.</span><span class="sxs-lookup"><span data-stu-id="fda24-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="fda24-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="fda24-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda24-111">Modelos</span><span class="sxs-lookup"><span data-stu-id="fda24-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



