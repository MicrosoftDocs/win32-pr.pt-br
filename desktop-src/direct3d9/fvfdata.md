---
description: Especifica os dados de malha menos os dados de posição.
ms.assetid: 30a95ca3-84ab-475d-9654-a3853263056b
title: FVFData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52af6096357c4855d2dc34442c6cd4814b6713b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087384"
---
# <a name="fvfdata"></a><span data-ttu-id="e8009-103">FVFData</span><span class="sxs-lookup"><span data-stu-id="e8009-103">FVFData</span></span>

<span data-ttu-id="e8009-104">Especifica os dados de malha menos os dados de posição.</span><span class="sxs-lookup"><span data-stu-id="e8009-104">Specifies the mesh data minus the position data.</span></span>

``` syntax
template FVFData
{
    < B6E70A0E-8EF9-4e83-94AD-ECC8B0C04897 >
    DWORD dwFVF;
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="e8009-105">Em que:</span><span class="sxs-lookup"><span data-stu-id="e8009-105">Where:</span></span>

-   <span data-ttu-id="e8009-106">dwFVF-um código FVF.</span><span class="sxs-lookup"><span data-stu-id="e8009-106">dwFVF - A FVF code.</span></span>
-   <span data-ttu-id="e8009-107">nDWords-dados binários.</span><span class="sxs-lookup"><span data-stu-id="e8009-107">nDWords - Binary data.</span></span> <span data-ttu-id="e8009-108">O número de DWORDs.</span><span class="sxs-lookup"><span data-stu-id="e8009-108">The number of DWORDS.</span></span>
-   <span data-ttu-id="e8009-109">Data \[ nDWords \] -matriz de DWORDs que contêm os dados em cada elemento Vertex.</span><span class="sxs-lookup"><span data-stu-id="e8009-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8009-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8009-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8009-111">Modelos</span><span class="sxs-lookup"><span data-stu-id="e8009-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



