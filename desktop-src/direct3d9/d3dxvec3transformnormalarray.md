---
description: Função D3DXVec3TransformNormalArray (D3dx9math. h) – transforma uma matriz (x, y, z, 0) por uma determinada matriz.
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: Função D3DXVec3TransformNormalArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74da959002bfbd0c488e630f09c89e848708b1b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097724"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="d4547-103">Função D3DXVec3TransformNormalArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d4547-103">D3DXVec3TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="d4547-104">Transforma uma matriz (x, y, z, 0) por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="d4547-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4547-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4547-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="d4547-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4547-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4547-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d4547-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4547-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4547-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d4547-109">Ponteiro para a matriz [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d4547-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d4547-110">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4547-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4547-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4547-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4547-112">Stride entre os vetores no fluxo de dados de saída.</span><span class="sxs-lookup"><span data-stu-id="d4547-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d4547-113">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4547-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4547-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4547-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d4547-115">Ponteiro para a matriz [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d4547-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="d4547-116">*VStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4547-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4547-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4547-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4547-118">Stride entre os vetores no fluxo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="d4547-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d4547-119">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4547-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4547-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4547-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d4547-121">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d4547-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d4547-122">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d4547-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4547-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4547-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4547-124">Número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="d4547-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4547-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d4547-125">Return value</span></span>

<span data-ttu-id="d4547-126">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4547-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d4547-127">Ponteiro para uma matriz [**D3DXVECTOR3**](d3dxvector3.md) que é a matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="d4547-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4547-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4547-128">Remarks</span></span>

<span data-ttu-id="d4547-129">Essa função transforma o vetor (*PV*->x, *PV*->y, *PV*->z, 0) pela matriz apontada por *PM*.</span><span class="sxs-lookup"><span data-stu-id="d4547-129">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="d4547-130">Se você quiser transformar um normal, a matriz que você passa para essa função deve ser a transpoção do inverso da matriz que você usaria para transformar um ponto.</span><span class="sxs-lookup"><span data-stu-id="d4547-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="d4547-131">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="d4547-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d4547-132">Dessa forma, a função **D3DXVec3TransformNormalArray** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d4547-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4547-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4547-133">Requirements</span></span>



| <span data-ttu-id="d4547-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4547-134">Requirement</span></span> | <span data-ttu-id="d4547-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d4547-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4547-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4547-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d4547-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4547-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d4547-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4547-138">Library</span></span><br/> | <dl> <span data-ttu-id="d4547-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4547-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4547-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d4547-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4547-141">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d4547-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
