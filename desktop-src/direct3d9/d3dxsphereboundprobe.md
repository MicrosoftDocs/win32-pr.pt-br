---
description: Determina se um raio intersecciona o volume da caixa delimitadora de uma esfera.
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: Função D3DXSphereBoundProbe (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbab8a49165a87f73037ae25230d67b02222fc15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789928"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a><span data-ttu-id="da70a-103">Função D3DXSphereBoundProbe (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="da70a-103">D3DXSphereBoundProbe function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="da70a-104">Determina se um raio intersecciona o volume da caixa delimitadora de uma esfera.</span><span class="sxs-lookup"><span data-stu-id="da70a-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="da70a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da70a-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="da70a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da70a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da70a-107">*pCenter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da70a-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da70a-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="da70a-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="da70a-109">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando a coordenada central da esfera.</span><span class="sxs-lookup"><span data-stu-id="da70a-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="da70a-110">*RADIUS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da70a-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da70a-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da70a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da70a-112">Raio da esfera.</span><span class="sxs-lookup"><span data-stu-id="da70a-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="da70a-113">*pRayPosition* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da70a-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da70a-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="da70a-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="da70a-115">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando a coordenada de origem do raio.</span><span class="sxs-lookup"><span data-stu-id="da70a-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="da70a-116">*pRayDirection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da70a-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da70a-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="da70a-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="da70a-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando a direção do raio.</span><span class="sxs-lookup"><span data-stu-id="da70a-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="da70a-119">Esse vetor não deve ser (0, 0, 0), mas não precisa ser normalizado.</span><span class="sxs-lookup"><span data-stu-id="da70a-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da70a-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da70a-120">Return value</span></span>

<span data-ttu-id="da70a-121">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da70a-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da70a-122">Retornará **true** se Ray Interseccionar o volume da caixa delimitadora da esfera.</span><span class="sxs-lookup"><span data-stu-id="da70a-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="da70a-123">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="da70a-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="da70a-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="da70a-124">Remarks</span></span>

<span data-ttu-id="da70a-125">**D3DXSphereBoundProbe** determina se Ray cruza o volume da caixa delimitadora da esfera, não apenas a superfície da esfera.</span><span class="sxs-lookup"><span data-stu-id="da70a-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="da70a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da70a-126">Requirements</span></span>



| <span data-ttu-id="da70a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="da70a-127">Requirement</span></span> | <span data-ttu-id="da70a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="da70a-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da70a-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da70a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="da70a-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="da70a-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="da70a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="da70a-131">Library</span></span><br/> | <dl> <span data-ttu-id="da70a-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da70a-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da70a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="da70a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da70a-134">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="da70a-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
