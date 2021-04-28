---
description: Função D3DXVec2TransformNormalArray (D3dx9math. h) – transforma uma matriz (x, y, 0, 0) por uma determinada matriz.
ms.assetid: 9f5d8fdc-f3e1-41dc-be4e-9ffc6be1947f
title: Função D3DXVec2TransformNormalArray (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71706551e73ed9bd52b41aae127625cd09b6d7f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097884"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="d1e12-103">Função D3DXVec2TransformNormalArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d1e12-103">D3DXVec2TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="d1e12-104">Transforma uma matriz (x, y, 0, 0) por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="d1e12-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e12-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1e12-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d1e12-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1e12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e12-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d1e12-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e12-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1e12-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d1e12-109">Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d1e12-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d1e12-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1e12-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e12-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1e12-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1e12-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="d1e12-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d1e12-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1e12-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e12-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d1e12-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d1e12-115">Ponteiro para a matriz [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d1e12-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="d1e12-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1e12-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e12-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1e12-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1e12-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="d1e12-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d1e12-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1e12-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e12-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d1e12-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d1e12-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d1e12-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d1e12-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d1e12-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e12-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1e12-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1e12-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="d1e12-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e12-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d1e12-125">Return value</span></span>

<span data-ttu-id="d1e12-126">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1e12-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d1e12-127">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é a matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="d1e12-127">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1e12-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1e12-128">Remarks</span></span>

<span data-ttu-id="d1e12-129">Essa função transforma o vetor (*PV-*>x, *PV-*>y, 0, 0) pela matriz apontada por *PM.*</span><span class="sxs-lookup"><span data-stu-id="d1e12-129">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM.*</span></span>

<span data-ttu-id="d1e12-130">Se você quiser transformar um normal, a matriz que você passa para essa função deve ser a transpoção do inverso da matriz que você usaria para transformar um ponto.</span><span class="sxs-lookup"><span data-stu-id="d1e12-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="d1e12-131">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="d1e12-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d1e12-132">Dessa forma, a função **D3DXVec2TransformNormalArray** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d1e12-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e12-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1e12-133">Requirements</span></span>



| <span data-ttu-id="d1e12-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1e12-134">Requirement</span></span> | <span data-ttu-id="d1e12-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d1e12-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e12-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1e12-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d1e12-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1e12-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d1e12-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1e12-138">Library</span></span><br/> | <dl> <span data-ttu-id="d1e12-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1e12-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d1e12-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d1e12-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e12-141">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d1e12-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
