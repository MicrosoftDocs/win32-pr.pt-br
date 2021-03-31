---
description: Transforma uma matriz (x, y, 0, 1) por uma determinada matriz.
ms.assetid: ba8c1983-bd65-4249-9451-69d813e4a3a4
title: Função D3DXVec2TransformArray (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf95c4b8ffd9fd2804b4168609e60ff7278d1209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663993"
---
# <a name="d3dxvec2transformarray-function-d3dx9mathh"></a><span data-ttu-id="009f7-103">Função D3DXVec2TransformArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="009f7-103">D3DXVec2TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="009f7-104">Transforma uma matriz (x, y, 0, 1) por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="009f7-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="009f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="009f7-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="009f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="009f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="009f7-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="009f7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="009f7-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="009f7-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="009f7-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="009f7-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="009f7-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="009f7-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009f7-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009f7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009f7-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="009f7-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="009f7-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="009f7-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009f7-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="009f7-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="009f7-115">Ponteiro para a estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="009f7-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="009f7-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="009f7-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009f7-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009f7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009f7-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="009f7-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="009f7-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="009f7-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009f7-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="009f7-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="009f7-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="009f7-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="009f7-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="009f7-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009f7-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009f7-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009f7-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="009f7-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="009f7-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="009f7-125">Return value</span></span>

<span data-ttu-id="009f7-126">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="009f7-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="009f7-127">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é a matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="009f7-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="009f7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="009f7-128">Remarks</span></span>

<span data-ttu-id="009f7-129">Essa função transforma a matriz *PV* (x, y, 0, 1) pela matriz *PM*.</span><span class="sxs-lookup"><span data-stu-id="009f7-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="009f7-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="009f7-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="009f7-131">Dessa forma, a função [**D3DXVec2Transform**](d3dxvec2transform.md) pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="009f7-131">In this way, the [**D3DXVec2Transform**](d3dxvec2transform.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="009f7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="009f7-132">Requirements</span></span>



| <span data-ttu-id="009f7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="009f7-133">Requirement</span></span> | <span data-ttu-id="009f7-134">Valor</span><span class="sxs-lookup"><span data-stu-id="009f7-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="009f7-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="009f7-135">Header</span></span><br/>  | <dl> <span data-ttu-id="009f7-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="009f7-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="009f7-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="009f7-137">Library</span></span><br/> | <dl> <span data-ttu-id="009f7-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="009f7-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="009f7-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="009f7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="009f7-140">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="009f7-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="009f7-141">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="009f7-141">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="009f7-142">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="009f7-142">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 
