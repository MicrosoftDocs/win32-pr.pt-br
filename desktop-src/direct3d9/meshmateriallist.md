---
description: Usado em um objeto de malha para especificar qual material se aplica a quais faces. O membro nMaterials especifica quantos materiais estão presentes e os materiais especificam qual material deve ser aplicado.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b746802dc3ef54a8feacc8ddfdaa0db1e45112b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105798187"
---
# <a name="meshmateriallist"></a><span data-ttu-id="9ef5e-104">MeshMaterialList</span><span class="sxs-lookup"><span data-stu-id="9ef5e-104">MeshMaterialList</span></span>

<span data-ttu-id="9ef5e-105">Usado em um objeto de malha para especificar qual material se aplica a quais faces.</span><span class="sxs-lookup"><span data-stu-id="9ef5e-105">Used in a mesh object to specify which material applies to which faces.</span></span> <span data-ttu-id="9ef5e-106">O membro nMaterials especifica quantos materiais estão presentes e os materiais especificam qual material deve ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="9ef5e-106">The nMaterials member specifies how many materials are present, and materials specify which material to apply.</span></span>

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

<span data-ttu-id="9ef5e-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="9ef5e-107">Where:</span></span>

-   <span data-ttu-id="9ef5e-108">nMaterials-um DWORD.</span><span class="sxs-lookup"><span data-stu-id="9ef5e-108">nMaterials - A DWORD.</span></span> <span data-ttu-id="9ef5e-109">O número de materiais.</span><span class="sxs-lookup"><span data-stu-id="9ef5e-109">The number of materials.</span></span>
-   <span data-ttu-id="9ef5e-110">nFaceIndexes-um DWORD.</span><span class="sxs-lookup"><span data-stu-id="9ef5e-110">nFaceIndexes - A DWORD.</span></span> <span data-ttu-id="9ef5e-111">O número de índices.</span><span class="sxs-lookup"><span data-stu-id="9ef5e-111">The number of indices.</span></span>
-   <span data-ttu-id="9ef5e-112">faceIndexes \[ nFaceIndexes \] – uma matriz de DWORDs que contém os índices de face.</span><span class="sxs-lookup"><span data-stu-id="9ef5e-112">faceIndexes\[nFaceIndexes\] - An array of DWORDs containing the face indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ef5e-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ef5e-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef5e-114">Modelos</span><span class="sxs-lookup"><span data-stu-id="9ef5e-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



