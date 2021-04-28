---
description: Função D3DXVec2TransformCoord (D3DX10Math. h) – transforma um vetor 2D por uma determinada matriz, projetando o resultado de volta em w = 1.
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: Função D3DXVec2TransformCoord (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 95321d377ad5af29075764e2c2d9386abf5b1441
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108334"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a><span data-ttu-id="1cccf-103">Função D3DXVec2TransformCoord (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1cccf-103">D3DXVec2TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="1cccf-104">Transforma um vetor 2D por uma determinada matriz, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="1cccf-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cccf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cccf-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="1cccf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cccf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cccf-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1cccf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cccf-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cccf-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1cccf-109">Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1cccf-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1cccf-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cccf-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cccf-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cccf-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1cccf-112">Ponteiro para a estrutura de D3DXVECTOR2 de origem.</span><span class="sxs-lookup"><span data-stu-id="1cccf-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="1cccf-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cccf-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cccf-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cccf-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1cccf-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="1cccf-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cccf-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1cccf-116">Return value</span></span>

<span data-ttu-id="1cccf-117">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cccf-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1cccf-118">Ponteiro para uma estrutura D3DXVECTOR2 que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="1cccf-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cccf-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cccf-119">Remarks</span></span>

<span data-ttu-id="1cccf-120">Essa função transforma o vetor, VP (x, y, 0, 1), pela matriz, pM, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="1cccf-120">This function transforms the vector, pV (x, y, 0, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="1cccf-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="1cccf-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1cccf-122">Dessa forma, a função D3DXVec2TransformCoord pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="1cccf-122">In this way, the D3DXVec2TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cccf-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cccf-123">Requirements</span></span>



| <span data-ttu-id="1cccf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cccf-124">Requirement</span></span> | <span data-ttu-id="1cccf-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1cccf-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cccf-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1cccf-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1cccf-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cccf-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1cccf-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1cccf-128">Library</span></span><br/> | <dl> <span data-ttu-id="1cccf-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cccf-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1cccf-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1cccf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cccf-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="1cccf-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
