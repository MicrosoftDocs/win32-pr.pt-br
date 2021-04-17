---
description: Transforma uma matriz (x, y, z, w) por uma determinada matriz.
ms.assetid: afd5cccb-e22f-4726-a84e-9eac1c1c277f
title: Função D3DXVec4TransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 5571fb19786e19a61c85741bcf6d4acb5231e977
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105751342"
---
# <a name="d3dxvec4transformarray-function-d3dx10mathh"></a><span data-ttu-id="af317-103">Função D3DXVec4TransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="af317-103">D3DXVec4TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="af317-104">Transforma uma matriz (x, y, z, w) por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="af317-104">Transforms an array (x, y, z, w) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="af317-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af317-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="af317-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af317-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af317-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="af317-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="af317-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="af317-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="af317-109">Ponteiro para a matriz [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="af317-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="af317-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af317-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af317-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af317-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af317-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="af317-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="af317-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af317-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af317-114">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="af317-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="af317-115">Ponteiro para a matriz D3DXVECTOR4 de origem.</span><span class="sxs-lookup"><span data-stu-id="af317-115">Pointer to the source D3DXVECTOR4 array.</span></span>

</dd> <dt>

<span data-ttu-id="af317-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af317-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af317-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af317-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af317-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="af317-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="af317-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af317-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af317-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="af317-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="af317-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="af317-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="af317-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="af317-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af317-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af317-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af317-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="af317-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af317-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af317-125">Return value</span></span>

<span data-ttu-id="af317-126">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="af317-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="af317-127">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é a matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="af317-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="af317-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="af317-128">Remarks</span></span>

<span data-ttu-id="af317-129">Essa função transforma a matriz pV (x, y, z, w) pela matriz pM.</span><span class="sxs-lookup"><span data-stu-id="af317-129">This function transforms the array pV (x, y, z, w) by the matrix pM.</span></span>

<span data-ttu-id="af317-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="af317-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="af317-131">Dessa forma, a função **D3DXVec4TransformArray** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="af317-131">In this way, the **D3DXVec4TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="af317-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af317-132">Requirements</span></span>



| <span data-ttu-id="af317-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="af317-133">Requirement</span></span> | <span data-ttu-id="af317-134">Valor</span><span class="sxs-lookup"><span data-stu-id="af317-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af317-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af317-135">Header</span></span><br/> | <dl> <span data-ttu-id="af317-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="af317-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af317-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="af317-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af317-138">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="af317-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
