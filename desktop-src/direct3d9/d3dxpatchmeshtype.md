---
description: Tipos de patch de malha.
ms.assetid: 229d01b2-781c-48a8-93f2-9dd9dbd67f3e
title: Enumeração D3DXPATCHMESHTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHMESHTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d6a663e983b339d79ec89bf1b4ddfe7b4eaa9f1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762159"
---
# <a name="d3dxpatchmeshtype-enumeration"></a><span data-ttu-id="3736e-103">Enumeração D3DXPATCHMESHTYPE</span><span class="sxs-lookup"><span data-stu-id="3736e-103">D3DXPATCHMESHTYPE enumeration</span></span>

<span data-ttu-id="3736e-104">Tipos de patch de malha.</span><span class="sxs-lookup"><span data-stu-id="3736e-104">Mesh patch types.</span></span>

## <a name="syntax"></a><span data-ttu-id="3736e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3736e-105">Syntax</span></span>


```C++
typedef enum D3DXPATCHMESHTYPE { 
  D3DXPATCHMESH_RECT         = 0x001,
  D3DXPATCHMESH_TRI          = 0x002,
  D3DXPATCHMESH_NPATCH       = 0x003,
  D3DXPATCHMESH_FORCE_DWORD  = 0x7fffffff
} D3DXPATCHMESHTYPE, *LPD3DXPATCHMESHTYPE;
```



## <a name="constants"></a><span data-ttu-id="3736e-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3736e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3736e-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="3736e-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH\_RECT**</span></span>
</dt> <dd>

<span data-ttu-id="3736e-108">Tipo de malha de patch de retângulo.</span><span class="sxs-lookup"><span data-stu-id="3736e-108">Rectangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="3736e-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH \_ Tri**</span><span class="sxs-lookup"><span data-stu-id="3736e-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH\_TRI**</span></span>
</dt> <dd>

<span data-ttu-id="3736e-110">Tipo de malha patch de triângulo.</span><span class="sxs-lookup"><span data-stu-id="3736e-110">Triangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="3736e-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH \_ NPATCH**</span><span class="sxs-lookup"><span data-stu-id="3736e-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH\_NPATCH**</span></span>
</dt> <dd>

<span data-ttu-id="3736e-112">Tipo de malha N-patch.</span><span class="sxs-lookup"><span data-stu-id="3736e-112">N-patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="3736e-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3736e-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="3736e-114">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="3736e-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="3736e-115">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3736e-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="3736e-116">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="3736e-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3736e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3736e-117">Remarks</span></span>

<span data-ttu-id="3736e-118">Os patches de triângulo têm três lados e são descritos em [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="3736e-118">Triangle patches have three sides and are described in [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span> <span data-ttu-id="3736e-119">Os patches de retângulo são quatro lado e são descritos em [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="3736e-119">Rectangle patches are four-sided and are described in [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3736e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-120">Requirements</span></span>



| <span data-ttu-id="3736e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3736e-121">Requirement</span></span> | <span data-ttu-id="3736e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3736e-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3736e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3736e-123">Header</span></span><br/> | <dl> <span data-ttu-id="3736e-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3736e-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3736e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3736e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3736e-126">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="3736e-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="3736e-127">Usando primitivos de Higher-Order (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3736e-127">Using Higher-Order Primitives (Direct3D 9)</span></span>](using-higher-order-primitives.md)
</dt> </dl>

 

 




