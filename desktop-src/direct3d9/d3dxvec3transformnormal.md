---
description: Transforma o vetor 3D normal pela matriz especificada.
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
ms.openlocfilehash: 8dd0bf3fa2083d2cf0cc0cea72343f4774a586f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173149"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a><span data-ttu-id="620ce-103">Função D3DXVec3TransformNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="620ce-103">D3DXVec3TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="620ce-104">Transforma o vetor 3D normal pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="620ce-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="620ce-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="620ce-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="620ce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="620ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="620ce-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="620ce-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="620ce-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="620ce-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="620ce-109">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="620ce-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="620ce-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="620ce-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="620ce-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="620ce-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="620ce-112">Ponteiro para a estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="620ce-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="620ce-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="620ce-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="620ce-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="620ce-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="620ce-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="620ce-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="620ce-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="620ce-116">Return value</span></span>

<span data-ttu-id="620ce-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="620ce-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="620ce-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="620ce-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="620ce-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="620ce-119">Remarks</span></span>

<span data-ttu-id="620ce-120">Essa função transforma o vetor (*PV*->x, *PV*->y, *PV*->z, 0) pela matriz apontada por *PM*.</span><span class="sxs-lookup"><span data-stu-id="620ce-120">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="620ce-121">Se você quiser transformar um normal, a matriz que você passa para essa função deve ser a transpoção do inverso da matriz que você usaria para transformar um ponto.</span><span class="sxs-lookup"><span data-stu-id="620ce-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="620ce-122">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="620ce-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="620ce-123">Dessa forma, a função **D3DXVec3TransformNormal** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="620ce-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="620ce-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="620ce-124">Requirements</span></span>



| <span data-ttu-id="620ce-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="620ce-125">Requirement</span></span> | <span data-ttu-id="620ce-126">Valor</span><span class="sxs-lookup"><span data-stu-id="620ce-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="620ce-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="620ce-127">Header</span></span><br/>  | <dl> <span data-ttu-id="620ce-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="620ce-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="620ce-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="620ce-129">Library</span></span><br/> | <dl> <span data-ttu-id="620ce-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="620ce-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="620ce-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="620ce-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="620ce-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="620ce-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




