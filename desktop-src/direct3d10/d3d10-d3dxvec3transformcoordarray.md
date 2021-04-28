---
description: Função D3DXVec3TransformCoordArray (D3DX10Math. h) – transforma uma matriz (x, y, z, 1) por uma determinada matriz e projeta o resultado de volta em w = 1.
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
ms.openlocfilehash: c4a1edfd89b127d0782d3bab23c2390775422c69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103104"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="fbac4-103">Função D3DXVec3TransformCoordArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="fbac4-103">D3DXVec3TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="fbac4-104">Transforma uma matriz (x, y, z, 1) por uma determinada matriz e projeta o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="fbac4-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbac4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbac4-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="fbac4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbac4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbac4-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fbac4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbac4-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fbac4-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fbac4-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="fbac4-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fbac4-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fbac4-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbac4-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbac4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbac4-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="fbac4-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="fbac4-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fbac4-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbac4-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fbac4-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fbac4-115">Ponteiro para a matriz D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="fbac4-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="fbac4-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fbac4-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbac4-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbac4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbac4-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="fbac4-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="fbac4-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fbac4-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbac4-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fbac4-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fbac4-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="fbac4-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fbac4-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="fbac4-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbac4-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbac4-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbac4-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="fbac4-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbac4-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fbac4-125">Return value</span></span>

<span data-ttu-id="fbac4-126">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fbac4-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fbac4-127">Ponteiro para uma estrutura D3DXVECTOR3 que é a matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="fbac4-127">Pointer to a D3DXVECTOR3 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbac4-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbac4-128">Remarks</span></span>

<span data-ttu-id="fbac4-129">Essa função transforma a matriz pV (x, y, z, 1) pela matriz pM, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="fbac4-129">This function transforms the array pV (x, y, z, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="fbac4-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="fbac4-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="fbac4-131">Dessa forma, a função [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="fbac4-131">In this way, the [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbac4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbac4-132">Requirements</span></span>



| <span data-ttu-id="fbac4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbac4-133">Requirement</span></span> | <span data-ttu-id="fbac4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="fbac4-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbac4-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbac4-135">Header</span></span><br/> | <dl> <span data-ttu-id="fbac4-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbac4-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbac4-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fbac4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbac4-138">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="fbac4-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
