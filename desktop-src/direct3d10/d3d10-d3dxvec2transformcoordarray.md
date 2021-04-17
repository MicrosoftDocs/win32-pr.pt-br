---
description: Transforma uma matriz (x, y, 0, 1) por uma determinada matriz e projeta o resultado de volta em w = 1.
ms.assetid: dba68678-2ab4-4f64-9975-5e9f2a20f66a
title: Função D3DXVec2TransformCoordArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoordArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aa57d96b0497fea572e580cfe6d1af2a0184f09d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811395"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="74222-103">Função D3DXVec2TransformCoordArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="74222-103">D3DXVec2TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="74222-104">Transforma uma matriz (x, y, 0, 1) por uma determinada matriz e projeta o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="74222-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="74222-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74222-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoordArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="74222-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74222-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74222-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="74222-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74222-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="74222-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="74222-109">Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="74222-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="74222-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74222-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74222-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74222-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74222-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="74222-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="74222-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74222-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74222-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="74222-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="74222-115">Ponteiro para a matriz D3DXVECTOR2 de origem.</span><span class="sxs-lookup"><span data-stu-id="74222-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="74222-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74222-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74222-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74222-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74222-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="74222-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="74222-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74222-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74222-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="74222-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="74222-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="74222-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="74222-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="74222-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74222-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74222-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74222-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="74222-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74222-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74222-125">Return value</span></span>

<span data-ttu-id="74222-126">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="74222-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="74222-127">Ponteiro para uma matriz transformada [**D3DXVECTOR4**](d3d10-d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="74222-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="74222-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="74222-128">Remarks</span></span>

<span data-ttu-id="74222-129">Essa função transforma a matriz pV (x, y, 0, 1) pela matriz pM, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="74222-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="74222-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="74222-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="74222-131">Dessa forma, a função D3DXVec2TransformCoordArray pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="74222-131">In this way, the D3DXVec2TransformCoordArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="74222-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74222-132">Requirements</span></span>



| <span data-ttu-id="74222-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="74222-133">Requirement</span></span> | <span data-ttu-id="74222-134">Valor</span><span class="sxs-lookup"><span data-stu-id="74222-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74222-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74222-135">Header</span></span><br/>  | <dl> <span data-ttu-id="74222-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="74222-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="74222-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74222-137">Library</span></span><br/> | <dl> <span data-ttu-id="74222-138"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74222-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74222-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="74222-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74222-140">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="74222-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
