---
description: Transforma uma matriz (x, y, 0, 1) por uma determinada matriz e projeta o resultado de volta em w = 1.
ms.assetid: 23c88bed-344b-4b3a-bb92-e50cbe96daf9
title: Função D3DXVec2TransformCoordArray (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e924f9c008efe76490f9f51903a1c31f254e0001
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760506"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx9mathh"></a><span data-ttu-id="78164-103">Função D3DXVec2TransformCoordArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="78164-103">D3DXVec2TransformCoordArray function (D3dx9math.h)</span></span>

<span data-ttu-id="78164-104">Transforma uma matriz (x, y, 0, 1) por uma determinada matriz e projeta o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="78164-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="78164-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78164-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="78164-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78164-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78164-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="78164-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78164-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="78164-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="78164-109">Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="78164-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="78164-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78164-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78164-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78164-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78164-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="78164-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="78164-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78164-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78164-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="78164-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="78164-115">Ponteiro para a matriz [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="78164-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="78164-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78164-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78164-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78164-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78164-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="78164-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="78164-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78164-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78164-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="78164-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="78164-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="78164-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="78164-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="78164-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78164-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78164-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78164-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="78164-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78164-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78164-125">Return value</span></span>

<span data-ttu-id="78164-126">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="78164-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="78164-127">Ponteiro para uma matriz transformada [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="78164-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="78164-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="78164-128">Remarks</span></span>

<span data-ttu-id="78164-129">Essa função transforma a matriz *PV* (x, y, 0, 1) pela matriz *PM*, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="78164-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*, projecting the result back into w = 1.</span></span>

<span data-ttu-id="78164-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="78164-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="78164-131">Dessa forma, a função **D3DXVec2TransformCoordArray** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="78164-131">In this way, the **D3DXVec2TransformCoordArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="78164-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78164-132">Requirements</span></span>



| <span data-ttu-id="78164-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="78164-133">Requirement</span></span> | <span data-ttu-id="78164-134">Valor</span><span class="sxs-lookup"><span data-stu-id="78164-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78164-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78164-135">Header</span></span><br/>  | <dl> <span data-ttu-id="78164-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="78164-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="78164-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78164-137">Library</span></span><br/> | <dl> <span data-ttu-id="78164-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78164-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78164-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="78164-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78164-140">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="78164-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
