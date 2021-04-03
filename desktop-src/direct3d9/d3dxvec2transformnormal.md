---
description: Transforma o vetor 2D normal pela matriz especificada.
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
ms.openlocfilehash: 154268b272f6cac00acb1d770d3c919cf65d6297
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930620"
---
# <a name="d3dxvec2transformnormal-function-d3dx9mathh"></a><span data-ttu-id="66a2e-103">Função D3DXVec2TransformNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="66a2e-103">D3DXVec2TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="66a2e-104">Transforma o vetor 2D normal pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="66a2e-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a2e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66a2e-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="66a2e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66a2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66a2e-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="66a2e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="66a2e-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="66a2e-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="66a2e-109">Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="66a2e-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="66a2e-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66a2e-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a2e-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="66a2e-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="66a2e-112">Ponteiro para a estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="66a2e-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="66a2e-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66a2e-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66a2e-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="66a2e-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="66a2e-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="66a2e-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66a2e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66a2e-116">Return value</span></span>

<span data-ttu-id="66a2e-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="66a2e-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="66a2e-118">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="66a2e-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="66a2e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="66a2e-119">Remarks</span></span>

<span data-ttu-id="66a2e-120">Essa função transforma o vetor (*PV-*>x, *PV-*>y, 0, 0) pela matriz apontada por *PM*.</span><span class="sxs-lookup"><span data-stu-id="66a2e-120">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="66a2e-121">Se você quiser transformar um normal, a matriz que você passa para essa função deve ser a transpoção do inverso da matriz que você usaria para transformar um ponto.</span><span class="sxs-lookup"><span data-stu-id="66a2e-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="66a2e-122">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="66a2e-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="66a2e-123">Dessa forma, a função **D3DXVec2TransformNormal** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="66a2e-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="66a2e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66a2e-124">Requirements</span></span>



| <span data-ttu-id="66a2e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a2e-125">Requirement</span></span> | <span data-ttu-id="66a2e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="66a2e-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66a2e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66a2e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="66a2e-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="66a2e-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="66a2e-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66a2e-129">Library</span></span><br/> | <dl> <span data-ttu-id="66a2e-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66a2e-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66a2e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="66a2e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a2e-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="66a2e-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="66a2e-133">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="66a2e-133">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="66a2e-134">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="66a2e-134">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> </dl>

 

 




