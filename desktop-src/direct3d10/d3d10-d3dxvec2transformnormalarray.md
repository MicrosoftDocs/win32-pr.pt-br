---
description: Transforma uma matriz (x, y, 0, 0) por uma determinada matriz.
ms.assetid: a53f998a-f2a5-4e4b-bc1c-c1f46284d78b
title: Função D3DXVec2TransformNormalArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4850961560ae810b9a21f58fbefa9b6b07227c77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781099"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="9aefd-103">Função D3DXVec2TransformNormalArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="9aefd-103">D3DXVec2TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="9aefd-104">Transforma uma matriz (x, y, 0, 0) por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="9aefd-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aefd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aefd-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="9aefd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9aefd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aefd-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9aefd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9aefd-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9aefd-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="9aefd-109">Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="9aefd-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9aefd-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aefd-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aefd-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aefd-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aefd-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="9aefd-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="9aefd-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aefd-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aefd-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9aefd-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="9aefd-115">Ponteiro para a matriz D3DXVECTOR2 de origem.</span><span class="sxs-lookup"><span data-stu-id="9aefd-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="9aefd-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aefd-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aefd-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aefd-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aefd-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="9aefd-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="9aefd-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aefd-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aefd-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9aefd-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9aefd-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="9aefd-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9aefd-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="9aefd-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aefd-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aefd-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aefd-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="9aefd-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aefd-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9aefd-125">Return value</span></span>

<span data-ttu-id="9aefd-126">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9aefd-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="9aefd-127">Ponteiro para uma estrutura D3DXVECTOR2 que é a matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="9aefd-127">Pointer to a D3DXVECTOR2 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aefd-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aefd-128">Remarks</span></span>

<span data-ttu-id="9aefd-129">Essa função transforma o vetor (pV->x, pV->y, 0, 0) pela matriz apontada por pM.</span><span class="sxs-lookup"><span data-stu-id="9aefd-129">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="9aefd-130">Se você quiser transformar um normal, a matriz que você passa para essa função deve ser a transpoção do inverso da matriz que você usaria para transformar um ponto.</span><span class="sxs-lookup"><span data-stu-id="9aefd-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="9aefd-131">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="9aefd-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9aefd-132">Dessa forma, a função **D3DXVec2TransformNormalArray** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="9aefd-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aefd-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aefd-133">Requirements</span></span>



| <span data-ttu-id="9aefd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aefd-134">Requirement</span></span> | <span data-ttu-id="9aefd-135">Valor</span><span class="sxs-lookup"><span data-stu-id="9aefd-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aefd-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9aefd-136">Header</span></span><br/>  | <dl> <span data-ttu-id="9aefd-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aefd-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9aefd-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9aefd-138">Library</span></span><br/> | <dl> <span data-ttu-id="9aefd-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aefd-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9aefd-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="9aefd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aefd-141">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="9aefd-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
