---
description: Especifica opções de simplificação para uma malha.
ms.assetid: f03170bd-7d2a-4839-9aec-c29426b95437
title: Enumeração D3DXMESHSIMP (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHSIMP
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: faf4244d115076b6b04cd04697acf789172d9b11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091963"
---
# <a name="d3dxmeshsimp-enumeration"></a><span data-ttu-id="1798f-103">Enumeração D3DXMESHSIMP</span><span class="sxs-lookup"><span data-stu-id="1798f-103">D3DXMESHSIMP enumeration</span></span>

<span data-ttu-id="1798f-104">Especifica opções de simplificação para uma malha.</span><span class="sxs-lookup"><span data-stu-id="1798f-104">Specifies simplification options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1798f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1798f-105">Syntax</span></span>


```C++
enum _D3DXMESHSIMP {
  D3DXMESHSIMP_VERTEX  = 1, 
  D3DXMESHSIMP_FACE    = 2 

};
```



## <a name="constants"></a><span data-ttu-id="1798f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1798f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1798f-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**\_Vértice D3DXMESHSIMP**</span><span class="sxs-lookup"><span data-stu-id="1798f-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**D3DXMESHSIMP\_VERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="1798f-108">A malha será simplificada pelo número de vértices especificado no parâmetro MinValue.</span><span class="sxs-lookup"><span data-stu-id="1798f-108">The mesh will be simplified by the number of vertices specified in the MinValue parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1798f-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**\_Rosto D3DXMESHSIMP**</span><span class="sxs-lookup"><span data-stu-id="1798f-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP\_FACE**</span></span>
</dt> <dd>

<span data-ttu-id="1798f-110">A malha será simplificada pelo número de faces especificado no parâmetro MinValue.</span><span class="sxs-lookup"><span data-stu-id="1798f-110">The mesh will be simplified by the number of faces specified in the MinValue parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1798f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1798f-111">Requirements</span></span>



| <span data-ttu-id="1798f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1798f-112">Requirement</span></span> | <span data-ttu-id="1798f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1798f-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1798f-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1798f-114">Header</span></span><br/> | <dl> <span data-ttu-id="1798f-115"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1798f-115"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1798f-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="1798f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1798f-117">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="1798f-117">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="1798f-118">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="1798f-118">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 




