---
description: Função D3DXVec2TransformNormal (D3dx9math. h) – transforma o vetor 2D normal pela matriz especificada.
ms.assetid: aa9adf6d-5aae-4acf-bbd9-f5c14d90470e
title: Função D3DXVec2TransformNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8ed31300027fcb2e827988809cce1c50dbf77de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097904"
---
# <a name="d3dxvec2transformnormal-function-d3dx9mathh"></a><span data-ttu-id="6bddd-103">Função D3DXVec2TransformNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6bddd-103">D3DXVec2TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="6bddd-104">Transforma o vetor 2D normal pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="6bddd-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bddd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6bddd-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="6bddd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bddd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bddd-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6bddd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bddd-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="6bddd-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6bddd-109">Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="6bddd-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6bddd-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bddd-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bddd-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6bddd-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6bddd-112">Ponteiro para a estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="6bddd-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6bddd-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bddd-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bddd-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6bddd-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6bddd-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="6bddd-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bddd-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6bddd-116">Return value</span></span>

<span data-ttu-id="6bddd-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="6bddd-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6bddd-118">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="6bddd-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bddd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bddd-119">Remarks</span></span>

<span data-ttu-id="6bddd-120">Essa função transforma o vetor (*PV-*>x, *PV-*>y, 0, 0) pela matriz apontada por *PM*.</span><span class="sxs-lookup"><span data-stu-id="6bddd-120">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="6bddd-121">Se você quiser transformar um normal, a matriz que você passa para essa função deve ser a transpoção do inverso da matriz que você usaria para transformar um ponto.</span><span class="sxs-lookup"><span data-stu-id="6bddd-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="6bddd-122">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="6bddd-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6bddd-123">Dessa forma, a função **D3DXVec2TransformNormal** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="6bddd-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bddd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bddd-124">Requirements</span></span>



| <span data-ttu-id="6bddd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bddd-125">Requirement</span></span> | <span data-ttu-id="6bddd-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6bddd-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bddd-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6bddd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6bddd-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bddd-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6bddd-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bddd-129">Library</span></span><br/> | <dl> <span data-ttu-id="6bddd-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bddd-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6bddd-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6bddd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bddd-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="6bddd-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6bddd-133">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="6bddd-133">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="6bddd-134">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="6bddd-134">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> </dl>

 

 




