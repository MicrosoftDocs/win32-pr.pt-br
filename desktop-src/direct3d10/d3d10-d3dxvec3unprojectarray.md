---
description: Projeta uma matriz (x, y, z, 0) do espaço da tela no espaço do objeto.
ms.assetid: 02db5b32-7fa3-4cde-bd63-0d8b3dfc31e7
title: Função D3DXVec3UnprojectArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: c7293339145253f817e8ed8b6812906b49792193
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105757182"
---
# <a name="d3dxvec3unprojectarray-function-d3dx10mathh"></a><span data-ttu-id="1587a-103">Função D3DXVec3UnprojectArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1587a-103">D3DXVec3UnprojectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="1587a-104">Projeta uma matriz (x, y, z, 0) do espaço da tela no espaço do objeto.</span><span class="sxs-lookup"><span data-stu-id="1587a-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="1587a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1587a-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
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



## <a name="parameters"></a><span data-ttu-id="1587a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1587a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1587a-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1587a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1587a-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1587a-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1587a-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1587a-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1587a-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1587a-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1587a-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1587a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1587a-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="1587a-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="1587a-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1587a-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1587a-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1587a-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1587a-115">Ponteiro para a estrutura de D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="1587a-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="1587a-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1587a-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1587a-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1587a-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1587a-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="1587a-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="1587a-119">*pViewport* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1587a-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1587a-120">Tipo: **\* [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) const**</span><span class="sxs-lookup"><span data-stu-id="1587a-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="1587a-121">Ponteiro para um [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), que representa o visor.</span><span class="sxs-lookup"><span data-stu-id="1587a-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="1587a-122">*pProjection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1587a-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1587a-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1587a-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1587a-124">Ponteiro para uma estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , representando a matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="1587a-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="1587a-125">*pView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1587a-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1587a-126">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1587a-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1587a-127">Ponteiro para uma estrutura D3DXMATRIX, representando a matriz de exibição.</span><span class="sxs-lookup"><span data-stu-id="1587a-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="1587a-128">*pWorld* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1587a-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1587a-129">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1587a-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1587a-130">Ponteiro para uma estrutura D3DXMATRIX, representando a matriz mundial.</span><span class="sxs-lookup"><span data-stu-id="1587a-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="1587a-131">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="1587a-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1587a-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1587a-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1587a-133">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="1587a-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1587a-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1587a-134">Return value</span></span>

<span data-ttu-id="1587a-135">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1587a-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1587a-136">Ponteiro para uma estrutura D3DXVECTOR3 que é a matriz projetada do espaço da tela para o espaço de objeto.</span><span class="sxs-lookup"><span data-stu-id="1587a-136">Pointer to a D3DXVECTOR3 structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="1587a-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="1587a-137">Remarks</span></span>

<span data-ttu-id="1587a-138">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="1587a-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1587a-139">Dessa forma, a função [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="1587a-139">In this way, the [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1587a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1587a-140">Requirements</span></span>



| <span data-ttu-id="1587a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1587a-141">Requirement</span></span> | <span data-ttu-id="1587a-142">Valor</span><span class="sxs-lookup"><span data-stu-id="1587a-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1587a-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1587a-143">Header</span></span><br/> | <dl> <span data-ttu-id="1587a-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1587a-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1587a-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="1587a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1587a-146">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="1587a-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
