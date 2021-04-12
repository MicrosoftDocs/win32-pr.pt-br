---
description: Transforma um vetor 2D por uma determinada matriz.
ms.assetid: 4b57eb7f-fae9-48ac-a806-510da75d25a6
title: Função D3DXVec2Transform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 513623e0004d8ede1fc2d142b2c7f8a7c226d5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370961"
---
# <a name="d3dxvec2transform-function-d3dx10mathh"></a><span data-ttu-id="57f45-103">Função D3DXVec2Transform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="57f45-103">D3DXVec2Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="57f45-104">Transforma um vetor 2D por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="57f45-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="57f45-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57f45-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="57f45-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57f45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57f45-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="57f45-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="57f45-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="57f45-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="57f45-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="57f45-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="57f45-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="57f45-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57f45-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="57f45-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="57f45-112">Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md)de origem.</span><span class="sxs-lookup"><span data-stu-id="57f45-112">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="57f45-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="57f45-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57f45-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="57f45-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="57f45-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="57f45-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57f45-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57f45-116">Return value</span></span>

<span data-ttu-id="57f45-117">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="57f45-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="57f45-118">Ponteiro para uma estrutura D3DXVECTOR4 que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="57f45-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="57f45-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="57f45-119">Remarks</span></span>

<span data-ttu-id="57f45-120">Essa função transforma o vetor pV (x, y, 0, 1) pela matriz pM.</span><span class="sxs-lookup"><span data-stu-id="57f45-120">This function transforms the vector pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="57f45-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="57f45-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="57f45-122">Dessa forma, a função D3DXVec2Transform pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="57f45-122">In this way, the D3DXVec2Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="57f45-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57f45-123">Requirements</span></span>



| <span data-ttu-id="57f45-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="57f45-124">Requirement</span></span> | <span data-ttu-id="57f45-125">Valor</span><span class="sxs-lookup"><span data-stu-id="57f45-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57f45-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57f45-126">Header</span></span><br/>  | <dl> <span data-ttu-id="57f45-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="57f45-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="57f45-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57f45-128">Library</span></span><br/> | <dl> <span data-ttu-id="57f45-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57f45-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="57f45-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="57f45-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f45-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="57f45-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
