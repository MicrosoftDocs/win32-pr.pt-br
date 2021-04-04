---
description: Transforma uma matriz (x, y, 0, 1) por uma determinada matriz.
ms.assetid: 66c8909c-6c20-4b32-9546-fcf2d0e824fa
title: Função D3DXVec2TransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c5aef5ecaa720e8c859d37f03ce88223187d16f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837937"
---
# <a name="d3dxvec2transformarray-function-d3dx10mathh"></a><span data-ttu-id="66f7c-103">Função D3DXVec2TransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="66f7c-103">D3DXVec2TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="66f7c-104">Transforma uma matriz (x, y, 0, 1) por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="66f7c-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f7c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66f7c-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="66f7c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66f7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66f7c-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="66f7c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="66f7c-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="66f7c-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="66f7c-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="66f7c-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="66f7c-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66f7c-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f7c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66f7c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66f7c-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="66f7c-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="66f7c-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66f7c-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f7c-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="66f7c-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="66f7c-115">Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md)de origem.</span><span class="sxs-lookup"><span data-stu-id="66f7c-115">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="66f7c-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66f7c-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f7c-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66f7c-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66f7c-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="66f7c-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="66f7c-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66f7c-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f7c-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="66f7c-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="66f7c-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="66f7c-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="66f7c-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="66f7c-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f7c-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66f7c-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66f7c-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="66f7c-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66f7c-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66f7c-125">Return value</span></span>

<span data-ttu-id="66f7c-126">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="66f7c-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="66f7c-127">Ponteiro para uma estrutura D3DXVECTOR4 que é a matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="66f7c-127">Pointer to a D3DXVECTOR4 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="66f7c-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="66f7c-128">Remarks</span></span>

<span data-ttu-id="66f7c-129">Essa função transforma a matriz pV (x, y, 0, 1) pela matriz pM.</span><span class="sxs-lookup"><span data-stu-id="66f7c-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="66f7c-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="66f7c-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="66f7c-131">Dessa forma, a função [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="66f7c-131">In this way, the [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f7c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66f7c-132">Requirements</span></span>



| <span data-ttu-id="66f7c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f7c-133">Requirement</span></span> | <span data-ttu-id="66f7c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="66f7c-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66f7c-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66f7c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="66f7c-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f7c-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="66f7c-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66f7c-137">Library</span></span><br/> | <dl> <span data-ttu-id="66f7c-138"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66f7c-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66f7c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="66f7c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f7c-140">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="66f7c-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
