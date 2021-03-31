---
description: Determina se um raio intersecciona o volume da caixa delimitadora de uma esfera.
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
ms.openlocfilehash: 09116e13582bbb75bc15ed04360ce02c4983f986
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664067"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a><span data-ttu-id="93775-103">Função D3DXSphereBoundProbe (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="93775-103">D3DXSphereBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="93775-104">Determina se um raio intersecciona o volume da caixa delimitadora de uma esfera.</span><span class="sxs-lookup"><span data-stu-id="93775-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="93775-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93775-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="93775-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93775-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93775-107">*pCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93775-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93775-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="93775-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="93775-109">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a coordenada central da esfera.</span><span class="sxs-lookup"><span data-stu-id="93775-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="93775-110">*RADIUS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93775-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93775-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93775-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93775-112">Raio da esfera.</span><span class="sxs-lookup"><span data-stu-id="93775-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="93775-113">*pRayPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93775-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93775-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="93775-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="93775-115">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a coordenada de origem do raio.</span><span class="sxs-lookup"><span data-stu-id="93775-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="93775-116">*pRayDirection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93775-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93775-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="93775-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="93775-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , especificando a direção do raio.</span><span class="sxs-lookup"><span data-stu-id="93775-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="93775-119">Esse vetor não deve ser (0, 0, 0), mas não precisa ser normalizado.</span><span class="sxs-lookup"><span data-stu-id="93775-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93775-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93775-120">Return value</span></span>

<span data-ttu-id="93775-121">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93775-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93775-122">Retornará **true** se Ray Interseccionar o volume da caixa delimitadora da esfera.</span><span class="sxs-lookup"><span data-stu-id="93775-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="93775-123">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="93775-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="93775-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="93775-124">Remarks</span></span>

<span data-ttu-id="93775-125">**D3DXSphereBoundProbe** determina se Ray cruza o volume da caixa delimitadora da esfera, não apenas a superfície da esfera.</span><span class="sxs-lookup"><span data-stu-id="93775-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="93775-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93775-126">Requirements</span></span>



| <span data-ttu-id="93775-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="93775-127">Requirement</span></span> | <span data-ttu-id="93775-128">Valor</span><span class="sxs-lookup"><span data-stu-id="93775-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93775-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93775-129">Header</span></span><br/>  | <dl> <span data-ttu-id="93775-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="93775-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="93775-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93775-131">Library</span></span><br/> | <dl> <span data-ttu-id="93775-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93775-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93775-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="93775-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93775-134">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="93775-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
