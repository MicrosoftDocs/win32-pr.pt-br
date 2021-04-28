---
description: Função D3DXVec3TransformNormal (D3dx9math. h) – transforma o vetor 3D normal pela matriz especificada.
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: Função D3DXVec3TransformNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50fb09a4619be9c3dbcff98bc939d6f99ad33bd4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115614"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a><span data-ttu-id="7ed2d-103">Função D3DXVec3TransformNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7ed2d-103">D3DXVec3TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="7ed2d-104">Transforma o vetor 3D normal pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="7ed2d-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ed2d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ed2d-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="7ed2d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ed2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ed2d-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7ed2d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ed2d-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ed2d-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7ed2d-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="7ed2d-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7ed2d-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ed2d-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ed2d-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ed2d-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7ed2d-112">Ponteiro para a estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="7ed2d-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7ed2d-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ed2d-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ed2d-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ed2d-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7ed2d-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="7ed2d-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ed2d-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7ed2d-116">Return value</span></span>

<span data-ttu-id="7ed2d-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ed2d-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7ed2d-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="7ed2d-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ed2d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ed2d-119">Remarks</span></span>

<span data-ttu-id="7ed2d-120">Essa função transforma o vetor (*PV*->x, *PV*->y, *PV*->z, 0) pela matriz apontada por *PM*.</span><span class="sxs-lookup"><span data-stu-id="7ed2d-120">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="7ed2d-121">Se você quiser transformar um normal, a matriz que você passa para essa função deve ser a transpoção do inverso da matriz que você usaria para transformar um ponto.</span><span class="sxs-lookup"><span data-stu-id="7ed2d-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="7ed2d-122">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="7ed2d-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7ed2d-123">Dessa forma, a função **D3DXVec3TransformNormal** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="7ed2d-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ed2d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ed2d-124">Requirements</span></span>



| <span data-ttu-id="7ed2d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ed2d-125">Requirement</span></span> | <span data-ttu-id="7ed2d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7ed2d-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed2d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ed2d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7ed2d-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ed2d-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7ed2d-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ed2d-129">Library</span></span><br/> | <dl> <span data-ttu-id="7ed2d-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ed2d-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7ed2d-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7ed2d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed2d-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="7ed2d-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




