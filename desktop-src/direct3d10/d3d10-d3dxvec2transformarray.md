---
description: Função D3DXVec2TransformArray (D3DX10Math. h) – transforma uma matriz (x, y, 0, 1) por uma determinada matriz.
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
ms.openlocfilehash: cec42fcbe53d3a8aa160f6864af70cbf441a19ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108364"
---
# <a name="d3dxvec2transformarray-function-d3dx10mathh"></a><span data-ttu-id="fcc26-103">Função D3DXVec2TransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="fcc26-103">D3DXVec2TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="fcc26-104">Transforma uma matriz (x, y, 0, 1) por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="fcc26-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc26-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcc26-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="fcc26-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcc26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcc26-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fcc26-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc26-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcc26-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="fcc26-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="fcc26-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fcc26-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcc26-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc26-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcc26-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcc26-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="fcc26-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="fcc26-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcc26-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc26-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcc26-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="fcc26-115">Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md)de origem.</span><span class="sxs-lookup"><span data-stu-id="fcc26-115">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="fcc26-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcc26-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc26-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcc26-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcc26-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="fcc26-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="fcc26-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcc26-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc26-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcc26-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fcc26-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="fcc26-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fcc26-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="fcc26-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc26-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcc26-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcc26-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="fcc26-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcc26-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fcc26-125">Return value</span></span>

<span data-ttu-id="fcc26-126">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcc26-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="fcc26-127">Ponteiro para uma estrutura D3DXVECTOR4 que é a matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="fcc26-127">Pointer to a D3DXVECTOR4 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcc26-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcc26-128">Remarks</span></span>

<span data-ttu-id="fcc26-129">Essa função transforma a matriz pV (x, y, 0, 1) pela matriz pM.</span><span class="sxs-lookup"><span data-stu-id="fcc26-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="fcc26-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="fcc26-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="fcc26-131">Dessa forma, a função [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="fcc26-131">In this way, the [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc26-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcc26-132">Requirements</span></span>



| <span data-ttu-id="fcc26-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcc26-133">Requirement</span></span> | <span data-ttu-id="fcc26-134">Valor</span><span class="sxs-lookup"><span data-stu-id="fcc26-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc26-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fcc26-135">Header</span></span><br/>  | <dl> <span data-ttu-id="fcc26-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcc26-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="fcc26-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcc26-137">Library</span></span><br/> | <dl> <span data-ttu-id="fcc26-138"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcc26-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fcc26-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fcc26-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc26-140">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="fcc26-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
