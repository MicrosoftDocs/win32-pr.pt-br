---
description: Transforma uma matriz (x, y, z, 1) por uma determinada matriz e projeta o resultado de volta em w = 1.
ms.assetid: 259a885d-89be-4fea-a579-dac3dd76878f
title: Função D3DXVec3TransformCoordArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoordArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: b0b7ca3c2898e07dc8b5e9ced0117e642bfdfb41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930626"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="e84c9-103">Função D3DXVec3TransformCoordArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e84c9-103">D3DXVec3TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="e84c9-104">Transforma uma matriz (x, y, z, 1) por uma determinada matriz e projeta o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="e84c9-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="e84c9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e84c9-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoordArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="e84c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e84c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e84c9-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e84c9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e84c9-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e84c9-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e84c9-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e84c9-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e84c9-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e84c9-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e84c9-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e84c9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e84c9-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="e84c9-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e84c9-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e84c9-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e84c9-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e84c9-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e84c9-115">Ponteiro para a matriz D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="e84c9-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="e84c9-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e84c9-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e84c9-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e84c9-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e84c9-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="e84c9-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e84c9-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e84c9-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e84c9-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e84c9-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e84c9-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="e84c9-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e84c9-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e84c9-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e84c9-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e84c9-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e84c9-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="e84c9-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e84c9-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e84c9-125">Return value</span></span>

<span data-ttu-id="e84c9-126">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e84c9-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e84c9-127">Ponteiro para uma estrutura D3DXVECTOR3 que é a matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="e84c9-127">Pointer to a D3DXVECTOR3 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="e84c9-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="e84c9-128">Remarks</span></span>

<span data-ttu-id="e84c9-129">Essa função transforma a matriz pV (x, y, z, 1) pela matriz pM, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="e84c9-129">This function transforms the array pV (x, y, z, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="e84c9-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="e84c9-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e84c9-131">Dessa forma, a função [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e84c9-131">In this way, the [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e84c9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e84c9-132">Requirements</span></span>



| <span data-ttu-id="e84c9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e84c9-133">Requirement</span></span> | <span data-ttu-id="e84c9-134">Valor</span><span class="sxs-lookup"><span data-stu-id="e84c9-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e84c9-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e84c9-135">Header</span></span><br/> | <dl> <span data-ttu-id="e84c9-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e84c9-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e84c9-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e84c9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e84c9-138">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e84c9-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
