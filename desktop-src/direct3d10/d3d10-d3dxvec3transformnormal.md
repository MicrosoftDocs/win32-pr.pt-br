---
description: Transforma o vetor 3D normal pela matriz especificada.
ms.assetid: 8068b80f-6222-4f23-8b1c-2ff5592fa898
title: Função D3DXVec3TransformNormal (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 602f366d3d7ccbcd37804226323d5584eed034f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298709"
---
# <a name="d3dxvec3transformnormal-function-d3dx10mathh"></a><span data-ttu-id="d99e1-103">Função D3DXVec3TransformNormal (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d99e1-103">D3DXVec3TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="d99e1-104">Transforma o vetor 3D normal pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="d99e1-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d99e1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d99e1-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d99e1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d99e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d99e1-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d99e1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d99e1-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d99e1-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d99e1-109">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d99e1-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d99e1-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d99e1-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99e1-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d99e1-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d99e1-112">Ponteiro para a estrutura de D3DXVECTOR3 de origem.</span><span class="sxs-lookup"><span data-stu-id="d99e1-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="d99e1-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d99e1-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99e1-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d99e1-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d99e1-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d99e1-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d99e1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d99e1-116">Return value</span></span>

<span data-ttu-id="d99e1-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d99e1-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d99e1-118">Ponteiro para uma estrutura D3DXVECTOR3 que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="d99e1-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d99e1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d99e1-119">Remarks</span></span>

<span data-ttu-id="d99e1-120">Essa função transforma o vetor (pV->x, pV->y, pV->z, 0) pela matriz apontada por pM.</span><span class="sxs-lookup"><span data-stu-id="d99e1-120">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="d99e1-121">Se você quiser transformar um normal, a matriz que você passa para essa função deve ser a transpoção do inverso da matriz que você usaria para transformar um ponto.</span><span class="sxs-lookup"><span data-stu-id="d99e1-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="d99e1-122">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="d99e1-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d99e1-123">Dessa forma, a função **D3DXVec3TransformNormal** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d99e1-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d99e1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d99e1-124">Requirements</span></span>



| <span data-ttu-id="d99e1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d99e1-125">Requirement</span></span> | <span data-ttu-id="d99e1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d99e1-126">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d99e1-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d99e1-127">Header</span></span><br/> | <dl> <span data-ttu-id="d99e1-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d99e1-128"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d99e1-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d99e1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d99e1-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d99e1-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
