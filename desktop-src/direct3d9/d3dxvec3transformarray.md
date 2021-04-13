---
description: Transforma uma matriz (x, y, z, 1) por uma determinada matriz.
ms.assetid: fd7ab674-5e42-4265-afad-ae5a00dabcdb
title: Função D3DXVec3TransformArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0b515c98be82aa47801b333c4b25680e0e464b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298524"
---
# <a name="d3dxvec3transformarray-function-d3dx9mathh"></a><span data-ttu-id="090d4-103">Função D3DXVec3TransformArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="090d4-103">D3DXVec3TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="090d4-104">Transforma uma matriz (x, y, z, 1) por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="090d4-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="090d4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="090d4-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="090d4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="090d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090d4-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="090d4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="090d4-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="090d4-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="090d4-109">Ponteiro para a matriz [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="090d4-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="090d4-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="090d4-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="090d4-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="090d4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="090d4-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="090d4-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="090d4-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="090d4-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="090d4-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="090d4-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="090d4-115">Ponteiro para a matriz [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="090d4-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="090d4-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="090d4-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="090d4-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="090d4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="090d4-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="090d4-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="090d4-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="090d4-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="090d4-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="090d4-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="090d4-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="090d4-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="090d4-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="090d4-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="090d4-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="090d4-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="090d4-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="090d4-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090d4-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="090d4-125">Return value</span></span>

<span data-ttu-id="090d4-126">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="090d4-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="090d4-127">Ponteiro para uma matriz transformada [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="090d4-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="090d4-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="090d4-128">Remarks</span></span>

<span data-ttu-id="090d4-129">Essa função transforma a matriz *PV* (x, y, z, 1) pela matriz *PM*.</span><span class="sxs-lookup"><span data-stu-id="090d4-129">This function transforms the array *pV* (x, y, z, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="090d4-130">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="090d4-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="090d4-131">Dessa forma, a função **D3DXVec3TransformArray** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="090d4-131">In this way, the **D3DXVec3TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="090d4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="090d4-132">Requirements</span></span>



| <span data-ttu-id="090d4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="090d4-133">Requirement</span></span> | <span data-ttu-id="090d4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="090d4-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="090d4-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="090d4-135">Header</span></span><br/>  | <dl> <span data-ttu-id="090d4-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="090d4-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="090d4-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="090d4-137">Library</span></span><br/> | <dl> <span data-ttu-id="090d4-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="090d4-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="090d4-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="090d4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090d4-140">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="090d4-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
