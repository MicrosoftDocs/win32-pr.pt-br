---
description: Transforma um vetor 2D por uma determinada matriz, projetando o resultado de volta em w = 1.
ms.assetid: 0c0efdf8-77df-4f4a-86ce-89e11555f4dc
title: Função D3DXVec2TransformCoord (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc047075cd2f9f6aba6903f85ea6960e78e0ba1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760793"
---
# <a name="d3dxvec2transformcoord-function-d3dx9mathh"></a><span data-ttu-id="d0728-103">Função D3DXVec2TransformCoord (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d0728-103">D3DXVec2TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="d0728-104">Transforma um vetor 2D por uma determinada matriz, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="d0728-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0728-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0728-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d0728-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0728-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0728-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d0728-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0728-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0728-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d0728-109">Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d0728-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d0728-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0728-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0728-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d0728-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d0728-112">Ponteiro para a estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d0728-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d0728-113">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0728-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0728-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d0728-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d0728-115">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="d0728-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0728-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0728-116">Return value</span></span>

<span data-ttu-id="d0728-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0728-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d0728-118">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o vetor transformado.</span><span class="sxs-lookup"><span data-stu-id="d0728-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0728-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0728-119">Remarks</span></span>

<span data-ttu-id="d0728-120">Essa função transforma o vetor, *VP* (x, y, 0, 1), pela matriz, *PM*, projetando o resultado de volta em w = 1.</span><span class="sxs-lookup"><span data-stu-id="d0728-120">This function transforms the vector, *pV* (x, y, 0, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="d0728-121">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="d0728-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d0728-122">Dessa forma, a função **D3DXVec2TransformCoord** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d0728-122">In this way, the **D3DXVec2TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0728-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0728-123">Requirements</span></span>



| <span data-ttu-id="d0728-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0728-124">Requirement</span></span> | <span data-ttu-id="d0728-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d0728-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0728-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0728-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d0728-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0728-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d0728-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0728-128">Library</span></span><br/> | <dl> <span data-ttu-id="d0728-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0728-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d0728-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0728-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0728-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d0728-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d0728-132">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="d0728-132">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="d0728-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="d0728-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




