---
description: Função D3DXVec2TransformNormal (D3DX10Math. h) – transforma o vetor 2D normal pela matriz especificada.
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: Função D3DXVec2TransformNormal (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 403562ab779ebf532e1c1ebcec4ce21a2beadd7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108294"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a><span data-ttu-id="52aaf-103">Função D3DXVec2TransformNormal (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="52aaf-103">D3DXVec2TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="52aaf-104">Transforma o vetor 2D normal pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="52aaf-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="52aaf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52aaf-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="52aaf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52aaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52aaf-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="52aaf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52aaf-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="52aaf-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="52aaf-109">Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="52aaf-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="52aaf-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52aaf-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52aaf-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="52aaf-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="52aaf-112">Ponteiro para a estrutura de D3DXVECTOR2 de origem.</span><span class="sxs-lookup"><span data-stu-id="52aaf-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="52aaf-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52aaf-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52aaf-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="52aaf-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="52aaf-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="52aaf-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52aaf-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="52aaf-116">Return value</span></span>

<span data-ttu-id="52aaf-117">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="52aaf-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="52aaf-118">Ponteiro para uma estrutura D3DXVECTOR2 que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="52aaf-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="52aaf-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="52aaf-119">Remarks</span></span>

<span data-ttu-id="52aaf-120">Essa função transforma o vetor (pV->x, pV->y, 0, 0) pela matriz apontada por pM.</span><span class="sxs-lookup"><span data-stu-id="52aaf-120">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="52aaf-121">Se você quiser transformar um normal, a matriz que você passa para essa função deve ser a transpoção do inverso da matriz que você usaria para transformar um ponto.</span><span class="sxs-lookup"><span data-stu-id="52aaf-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="52aaf-122">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="52aaf-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="52aaf-123">Dessa forma, a função **D3DXVec2TransformNormal** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="52aaf-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="52aaf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52aaf-124">Requirements</span></span>



| <span data-ttu-id="52aaf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="52aaf-125">Requirement</span></span> | <span data-ttu-id="52aaf-126">Valor</span><span class="sxs-lookup"><span data-stu-id="52aaf-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52aaf-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52aaf-127">Header</span></span><br/>  | <dl> <span data-ttu-id="52aaf-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="52aaf-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="52aaf-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52aaf-129">Library</span></span><br/> | <dl> <span data-ttu-id="52aaf-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52aaf-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52aaf-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="52aaf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52aaf-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="52aaf-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
