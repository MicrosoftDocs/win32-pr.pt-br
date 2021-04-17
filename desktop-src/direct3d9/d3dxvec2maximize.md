---
description: Retorna um vetor 2D que é composto pelos maiores componentes de dois vetores 2D.
ms.assetid: 5eb5141b-d611-4c6b-a3e3-c7ad8f223657
title: Função D3DXVec2Maximize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffd5fbc98e653a6bbaffa7d3cec16b13695365b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370947"
---
# <a name="d3dxvec2maximize-function"></a><span data-ttu-id="826fd-103">Função D3DXVec2Maximize</span><span class="sxs-lookup"><span data-stu-id="826fd-103">D3DXVec2Maximize function</span></span>

<span data-ttu-id="826fd-104">Retorna um vetor 2D que é composto pelos maiores componentes de dois vetores 2D.</span><span class="sxs-lookup"><span data-stu-id="826fd-104">Returns a 2D vector that is made up of the largest components of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="826fd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="826fd-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Maximize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="826fd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="826fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="826fd-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="826fd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="826fd-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="826fd-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="826fd-109">Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="826fd-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="826fd-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="826fd-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826fd-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="826fd-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="826fd-112">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="826fd-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="826fd-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="826fd-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826fd-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="826fd-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="826fd-115">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="826fd-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="826fd-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="826fd-116">Return value</span></span>

<span data-ttu-id="826fd-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="826fd-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="826fd-118">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é composta pelos maiores componentes dos dois vetores.</span><span class="sxs-lookup"><span data-stu-id="826fd-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="826fd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="826fd-119">Remarks</span></span>

<span data-ttu-id="826fd-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="826fd-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="826fd-121">Dessa forma, a função **D3DXVec2Maximize** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="826fd-121">In this way, the **D3DXVec2Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="826fd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="826fd-122">Requirements</span></span>



| <span data-ttu-id="826fd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="826fd-123">Requirement</span></span> | <span data-ttu-id="826fd-124">Valor</span><span class="sxs-lookup"><span data-stu-id="826fd-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="826fd-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="826fd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="826fd-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="826fd-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="826fd-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="826fd-127">Library</span></span><br/> | <dl> <span data-ttu-id="826fd-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="826fd-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="826fd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="826fd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826fd-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="826fd-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="826fd-131">**D3DXVec2Minimize**</span><span class="sxs-lookup"><span data-stu-id="826fd-131">**D3DXVec2Minimize**</span></span>](d3dxvec2minimize.md)
</dt> </dl>

 

 




