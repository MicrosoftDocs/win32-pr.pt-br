---
description: Projeta uma matriz (x, y, z, 0) do espaço do objeto no espaço da tela.
ms.assetid: 33f0f65a-c027-4a31-83a7-f5f6b2a2f72f
title: Função D3DXVec3ProjectArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: bdbda9201d23a6c525dc054c53874c71d548e65e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298726"
---
# <a name="d3dxvec3projectarray-function-d3dx10mathh"></a><span data-ttu-id="e30a8-103">Função D3DXVec3ProjectArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e30a8-103">D3DXVec3ProjectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="e30a8-104">Projeta uma matriz (x, y, z, 0) do espaço do objeto no espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="e30a8-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="e30a8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e30a8-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_          UINT           OutStride,
  _In_    const D3DXVECTOR3    *pV,
  _In_          UINT           VStride,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld,
  _In_          UINT           n
);
```



## <a name="parameters"></a><span data-ttu-id="e30a8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e30a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e30a8-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e30a8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e30a8-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e30a8-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e30a8-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e30a8-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e30a8-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e30a8-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e30a8-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e30a8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e30a8-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="e30a8-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e30a8-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e30a8-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e30a8-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e30a8-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e30a8-115">Ponteiro para a estrutura de D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="e30a8-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="e30a8-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e30a8-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e30a8-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e30a8-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e30a8-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="e30a8-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e30a8-119">*pViewport* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e30a8-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e30a8-120">Tipo: **\* [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) const**</span><span class="sxs-lookup"><span data-stu-id="e30a8-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="e30a8-121">Ponteiro para um [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), que representa o visor.</span><span class="sxs-lookup"><span data-stu-id="e30a8-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="e30a8-122">*pProjection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e30a8-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e30a8-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e30a8-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e30a8-124">Ponteiro para uma estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , representando a matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="e30a8-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e30a8-125">*pView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e30a8-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e30a8-126">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e30a8-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e30a8-127">Ponteiro para uma estrutura D3DXMATRIX, representando a matriz de exibição.</span><span class="sxs-lookup"><span data-stu-id="e30a8-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e30a8-128">*pWorld* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e30a8-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e30a8-129">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e30a8-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e30a8-130">Ponteiro para uma estrutura D3DXMATRIX, representando a matriz mundial.</span><span class="sxs-lookup"><span data-stu-id="e30a8-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="e30a8-131">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e30a8-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e30a8-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e30a8-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e30a8-133">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="e30a8-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e30a8-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e30a8-134">Return value</span></span>

<span data-ttu-id="e30a8-135">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e30a8-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e30a8-136">Ponteiro para uma estrutura D3DXVECTOR3 que é a matriz projetada do espaço de objeto para o espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="e30a8-136">Pointer to a D3DXVECTOR3 structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="e30a8-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="e30a8-137">Remarks</span></span>

<span data-ttu-id="e30a8-138">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="e30a8-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e30a8-139">Dessa forma, a função D3DXVec3ProjectArray pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e30a8-139">In this way, the D3DXVec3ProjectArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e30a8-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e30a8-140">Requirements</span></span>



| <span data-ttu-id="e30a8-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e30a8-141">Requirement</span></span> | <span data-ttu-id="e30a8-142">Valor</span><span class="sxs-lookup"><span data-stu-id="e30a8-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e30a8-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e30a8-143">Header</span></span><br/> | <dl> <span data-ttu-id="e30a8-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e30a8-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e30a8-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="e30a8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e30a8-146">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e30a8-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
