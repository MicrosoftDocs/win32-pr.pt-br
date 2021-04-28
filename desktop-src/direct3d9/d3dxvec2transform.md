---
description: Função D3DXVec2Transform (D3dx9math. h) – transforma um vetor 2D por uma determinada matriz.
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: Função D3DXVec2Transform (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b9b0f5ae0e3fda05cd8bdd92ee73b826f81b970
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097944"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a><span data-ttu-id="d59a4-103">Função D3DXVec2Transform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d59a4-103">D3DXVec2Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="d59a4-104">Transforma um vetor 2D por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="d59a4-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d59a4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d59a4-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d59a4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d59a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d59a4-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d59a4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d59a4-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d59a4-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d59a4-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d59a4-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d59a4-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d59a4-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d59a4-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d59a4-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d59a4-112">Ponteiro para a estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d59a4-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d59a4-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d59a4-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d59a4-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d59a4-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d59a4-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d59a4-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d59a4-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d59a4-116">Return value</span></span>

<span data-ttu-id="d59a4-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d59a4-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d59a4-118">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="d59a4-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d59a4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d59a4-119">Remarks</span></span>

<span data-ttu-id="d59a4-120">Essa função transforma o vetor *PV* (x, y, 0, 1) pela matriz *PM*.</span><span class="sxs-lookup"><span data-stu-id="d59a4-120">This function transforms the vector *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="d59a4-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="d59a4-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d59a4-122">Dessa forma, a função **D3DXVec2Transform** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d59a4-122">In this way, the **D3DXVec2Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d59a4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d59a4-123">Requirements</span></span>



| <span data-ttu-id="d59a4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d59a4-124">Requirement</span></span> | <span data-ttu-id="d59a4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d59a4-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d59a4-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d59a4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d59a4-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d59a4-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d59a4-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d59a4-128">Library</span></span><br/> | <dl> <span data-ttu-id="d59a4-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d59a4-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d59a4-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d59a4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d59a4-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d59a4-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d59a4-132">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="d59a4-132">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="d59a4-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="d59a4-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




