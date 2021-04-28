---
description: Função D3DXVec4Transform (D3DX10Math. h) – transforma um vetor 4D por uma determinada matriz.
ms.assetid: ccbf33bc-1f94-4cf8-b048-220d54516e00
title: Função D3DXVec4Transform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 737e1901a514a3940790ce83c7e9bc1f6f471371
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102914"
---
# <a name="d3dxvec4transform-function-d3dx10mathh"></a><span data-ttu-id="e6b03-103">Função D3DXVec4Transform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e6b03-103">D3DXVec4Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="e6b03-104">Transforma um vetor 4D por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="e6b03-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6b03-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6b03-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e6b03-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6b03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6b03-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e6b03-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6b03-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6b03-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="e6b03-109">Ponteiro para o [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e6b03-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e6b03-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6b03-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6b03-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6b03-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="e6b03-112">Ponteiro para a estrutura de D3DXVECTOR4 de origem.</span><span class="sxs-lookup"><span data-stu-id="e6b03-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="e6b03-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6b03-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6b03-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6b03-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e6b03-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="e6b03-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6b03-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e6b03-116">Return value</span></span>

<span data-ttu-id="e6b03-117">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6b03-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="e6b03-118">Ponteiro para uma estrutura D3DXVECTOR4 que é o vetor 4D transformado.</span><span class="sxs-lookup"><span data-stu-id="e6b03-118">Pointer to a D3DXVECTOR4 structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6b03-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6b03-119">Remarks</span></span>

<span data-ttu-id="e6b03-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="e6b03-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e6b03-121">Dessa forma, a função D3DXVec4Transform pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e6b03-121">In this way, the D3DXVec4Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6b03-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6b03-122">Requirements</span></span>



| <span data-ttu-id="e6b03-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6b03-123">Requirement</span></span> | <span data-ttu-id="e6b03-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e6b03-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b03-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6b03-125">Header</span></span><br/> | <dl> <span data-ttu-id="e6b03-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6b03-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6b03-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e6b03-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6b03-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e6b03-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
