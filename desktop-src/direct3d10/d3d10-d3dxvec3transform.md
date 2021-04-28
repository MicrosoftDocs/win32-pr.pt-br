---
description: Função D3DXVec3Transform (D3DX10Math. h) – transforma o vetor (x, y, z, 1) por uma determinada matriz.
ms.assetid: 88b26d94-2550-4126-bf91-b06391ec5c75
title: Função D3DXVec3Transform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9b5cd69ce603f56e4837818cac6ee18fe3ab1e53
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108134"
---
# <a name="d3dxvec3transform-function-d3dx10mathh"></a><span data-ttu-id="19713-103">Função D3DXVec3Transform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="19713-103">D3DXVec3Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="19713-104">Transforma o vetor (x, y, z, 1) por uma determinada matriz.</span><span class="sxs-lookup"><span data-stu-id="19713-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="19713-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19713-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="19713-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19713-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19713-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="19713-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19713-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="19713-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="19713-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="19713-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="19713-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19713-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19713-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="19713-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="19713-112">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md)de origem.</span><span class="sxs-lookup"><span data-stu-id="19713-112">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="19713-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19713-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19713-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="19713-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="19713-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="19713-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19713-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="19713-116">Return value</span></span>

<span data-ttu-id="19713-117">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="19713-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="19713-118">Ponteiro para uma estrutura D3DXVECTOR4 que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="19713-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="19713-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="19713-119">Remarks</span></span>

<span data-ttu-id="19713-120">Essa função transforma o vetor, VP (x, y, z, 1), pela matriz pM.</span><span class="sxs-lookup"><span data-stu-id="19713-120">This function transforms the vector, pV (x, y, z, 1), by the matrix pM.</span></span>

<span data-ttu-id="19713-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="19713-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="19713-122">Dessa forma, a função D3DXVec3Transform pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="19713-122">In this way, the D3DXVec3Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="19713-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19713-123">Requirements</span></span>



| <span data-ttu-id="19713-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="19713-124">Requirement</span></span> | <span data-ttu-id="19713-125">Valor</span><span class="sxs-lookup"><span data-stu-id="19713-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19713-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19713-126">Header</span></span><br/> | <dl> <span data-ttu-id="19713-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="19713-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19713-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="19713-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19713-129">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="19713-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
