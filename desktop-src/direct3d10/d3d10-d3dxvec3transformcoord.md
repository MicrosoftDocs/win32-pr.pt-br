---
description: Função D3DXVec3TransformCoord (D3DX10Math. h) – transforma um vetor 3D por uma determinada matriz, projetando o resultado de volta em w = 1.
ms.assetid: e138fdc0-6999-45ab-8bcf-54f53bd9b1bf
title: Função D3DXVec3TransformCoord (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 5b3e763d87503f9ca71911ad40ccf3c6ae9ca722
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108094"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a><span data-ttu-id="a075d-103">Função D3DXVec3TransformCoord (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a075d-103">D3DXVec3TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="a075d-104">Transforma um vetor 3D por uma determinada matriz, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="a075d-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="a075d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a075d-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="a075d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a075d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a075d-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a075d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a075d-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a075d-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a075d-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="a075d-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a075d-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a075d-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a075d-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a075d-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a075d-112">Ponteiro para a estrutura de D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="a075d-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="a075d-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a075d-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a075d-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a075d-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a075d-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="a075d-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a075d-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a075d-116">Return value</span></span>

<span data-ttu-id="a075d-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a075d-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a075d-118">Ponteiro para uma estrutura D3DXVECTOR3 que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="a075d-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="a075d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a075d-119">Remarks</span></span>

<span data-ttu-id="a075d-120">Essa função transforma o vetor, VP (x, y, z, 1), pela matriz, pM, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="a075d-120">This function transforms the vector, pV (x, y, z, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="a075d-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="a075d-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a075d-122">Dessa forma, a função D3DXVec3TransformCoord pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="a075d-122">In this way, the D3DXVec3TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a075d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a075d-123">Requirements</span></span>



| <span data-ttu-id="a075d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a075d-124">Requirement</span></span> | <span data-ttu-id="a075d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a075d-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a075d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a075d-126">Header</span></span><br/> | <dl> <span data-ttu-id="a075d-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a075d-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a075d-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a075d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a075d-129">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="a075d-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
