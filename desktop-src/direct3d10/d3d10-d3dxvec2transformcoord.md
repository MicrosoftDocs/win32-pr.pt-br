---
description: Transforma um vetor 2D por uma determinada matriz, projetando o resultado de volta em w = 1.
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: Função D3DXVec2TransformCoord (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0d7e93c2b3a78160f2f1f1ad3342575b4369a057
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772932"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a><span data-ttu-id="78167-103">Função D3DXVec2TransformCoord (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="78167-103">D3DXVec2TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="78167-104">Transforma um vetor 2D por uma determinada matriz, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="78167-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="78167-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78167-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="78167-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78167-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78167-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="78167-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78167-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="78167-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="78167-109">Ponteiro para o [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="78167-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="78167-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78167-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78167-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="78167-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="78167-112">Ponteiro para a estrutura de D3DXVECTOR2 de origem.</span><span class="sxs-lookup"><span data-stu-id="78167-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="78167-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78167-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78167-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="78167-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="78167-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="78167-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78167-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78167-116">Return value</span></span>

<span data-ttu-id="78167-117">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="78167-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="78167-118">Ponteiro para uma estrutura D3DXVECTOR2 que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="78167-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="78167-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="78167-119">Remarks</span></span>

<span data-ttu-id="78167-120">Essa função transforma o vetor, VP (x, y, 0, 1), pela matriz, pM, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="78167-120">This function transforms the vector, pV (x, y, 0, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="78167-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="78167-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="78167-122">Dessa forma, a função D3DXVec2TransformCoord pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="78167-122">In this way, the D3DXVec2TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="78167-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78167-123">Requirements</span></span>



| <span data-ttu-id="78167-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="78167-124">Requirement</span></span> | <span data-ttu-id="78167-125">Valor</span><span class="sxs-lookup"><span data-stu-id="78167-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78167-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78167-126">Header</span></span><br/>  | <dl> <span data-ttu-id="78167-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="78167-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="78167-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78167-128">Library</span></span><br/> | <dl> <span data-ttu-id="78167-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78167-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78167-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="78167-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78167-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="78167-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
