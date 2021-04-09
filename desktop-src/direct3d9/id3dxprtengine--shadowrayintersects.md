---
description: Usa o rastreamento de raio eficiente em simulações de computação radiante (PRT) para determinar se um raio cruza uma malha. Normalmente usado para determinar se um determinado ponto está em sombra.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'Método ID3DXPRTEngine:: ShadowRayIntersects (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012117"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a><span data-ttu-id="2b220-104">Método ID3DXPRTEngine:: ShadowRayIntersects</span><span class="sxs-lookup"><span data-stu-id="2b220-104">ID3DXPRTEngine::ShadowRayIntersects method</span></span>

<span data-ttu-id="2b220-105">Usa o rastreamento de raio eficiente em simulações de computação radiante (PRT) para determinar se um raio cruza uma malha.</span><span class="sxs-lookup"><span data-stu-id="2b220-105">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="2b220-106">Normalmente usado para determinar se um determinado ponto está em sombra.</span><span class="sxs-lookup"><span data-stu-id="2b220-106">Typically used to determine whether a given point is in shadow.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b220-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b220-107">Syntax</span></span>


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a><span data-ttu-id="2b220-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b220-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b220-109">*pRayPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b220-109">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b220-110">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b220-110">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b220-111">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando o ponto em que o raio começa.</span><span class="sxs-lookup"><span data-stu-id="2b220-111">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="2b220-112">*pRayDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b220-112">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b220-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b220-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b220-114">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , especificando a direção normalizada do raio.</span><span class="sxs-lookup"><span data-stu-id="2b220-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b220-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b220-115">Return value</span></span>

<span data-ttu-id="2b220-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b220-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b220-117">Retornará **true** se Ray Interseccionar a malha atual; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="2b220-117">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b220-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b220-118">Remarks</span></span>

<span data-ttu-id="2b220-119">Use [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) para definir distâncias mínimas e máximas de interseção com Ray.</span><span class="sxs-lookup"><span data-stu-id="2b220-119">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="2b220-120">Esse método é executado mais rápido que [**ID3DXPRTEngine:: ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="2b220-120">This method executes faster than [**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b220-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b220-121">Requirements</span></span>



| <span data-ttu-id="2b220-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b220-122">Requirement</span></span> | <span data-ttu-id="2b220-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2b220-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b220-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b220-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2b220-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b220-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2b220-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b220-126">Library</span></span><br/> | <dl> <span data-ttu-id="2b220-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b220-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2b220-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b220-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b220-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="2b220-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="2b220-130">**ID3DXPRTEngine::ClosestRayIntersects**</span><span class="sxs-lookup"><span data-stu-id="2b220-130">**ID3DXPRTEngine::ClosestRayIntersects**</span></span>](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[<span data-ttu-id="2b220-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span><span class="sxs-lookup"><span data-stu-id="2b220-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
