---
description: Função D3DXSphereBoundProbe (D3DX10math. h) – determina se um raio intersecciona o volume da caixa delimitadora de uma esfera.
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: Função D3DXSphereBoundProbe (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fb5a329e39631dff626ff1c7945ad4b05f9dcd58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108464"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a><span data-ttu-id="50e66-103">Função D3DXSphereBoundProbe (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="50e66-103">D3DXSphereBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="50e66-104">Determina se um raio intersecciona o volume da caixa delimitadora de uma esfera.</span><span class="sxs-lookup"><span data-stu-id="50e66-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50e66-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="50e66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50e66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e66-107">*pCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50e66-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e66-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="50e66-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="50e66-109">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a coordenada central da esfera.</span><span class="sxs-lookup"><span data-stu-id="50e66-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="50e66-110">*RADIUS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50e66-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e66-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50e66-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50e66-112">Raio da esfera.</span><span class="sxs-lookup"><span data-stu-id="50e66-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="50e66-113">*pRayPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50e66-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e66-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="50e66-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="50e66-115">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a coordenada de origem do raio.</span><span class="sxs-lookup"><span data-stu-id="50e66-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="50e66-116">*pRayDirection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50e66-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50e66-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="50e66-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="50e66-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a direção do raio.</span><span class="sxs-lookup"><span data-stu-id="50e66-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="50e66-119">Esse vetor não deve ser (0, 0, 0), mas não precisa ser normalizado.</span><span class="sxs-lookup"><span data-stu-id="50e66-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e66-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="50e66-120">Return value</span></span>

<span data-ttu-id="50e66-121">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50e66-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50e66-122">Retornará **true** se Ray Interseccionar o volume da caixa delimitadora da esfera.</span><span class="sxs-lookup"><span data-stu-id="50e66-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="50e66-123">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="50e66-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="50e66-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="50e66-124">Remarks</span></span>

<span data-ttu-id="50e66-125">**D3DXSphereBoundProbe** determina se Ray cruza o volume da caixa delimitadora da esfera, não apenas a superfície da esfera.</span><span class="sxs-lookup"><span data-stu-id="50e66-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e66-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50e66-126">Requirements</span></span>



| <span data-ttu-id="50e66-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="50e66-127">Requirement</span></span> | <span data-ttu-id="50e66-128">Valor</span><span class="sxs-lookup"><span data-stu-id="50e66-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50e66-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50e66-129">Header</span></span><br/>  | <dl> <span data-ttu-id="50e66-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="50e66-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="50e66-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50e66-131">Library</span></span><br/> | <dl> <span data-ttu-id="50e66-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50e66-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50e66-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="50e66-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e66-134">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="50e66-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
