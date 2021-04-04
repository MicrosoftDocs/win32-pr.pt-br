---
description: Adiciona dois vetores 2D.
ms.assetid: 82b2fdf6-1b1f-4768-8c0b-ac8faa77d7ed
title: Função D3DXVec2Add (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5087177448b01763bd94acb9b50c27c6cdf38815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930574"
---
# <a name="d3dxvec2add-function"></a><span data-ttu-id="7fbb4-103">Função D3DXVec2Add</span><span class="sxs-lookup"><span data-stu-id="7fbb4-103">D3DXVec2Add function</span></span>

<span data-ttu-id="7fbb4-104">Adiciona dois vetores 2D.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-104">Adds two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbb4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fbb4-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Add(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="7fbb4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fbb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fbb4-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7fbb4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fbb4-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7fbb4-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7fbb4-109">Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7fbb4-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7fbb4-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fbb4-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7fbb4-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7fbb4-112">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7fbb4-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7fbb4-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fbb4-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7fbb4-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7fbb4-115">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fbb4-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7fbb4-116">Return value</span></span>

<span data-ttu-id="7fbb4-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7fbb4-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7fbb4-118">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é a soma dos dois vetores.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the sum of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fbb4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fbb4-119">Remarks</span></span>

<span data-ttu-id="7fbb4-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="7fbb4-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7fbb4-121">Dessa forma, a função **D3DXVec2Add** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="7fbb4-121">In this way, the **D3DXVec2Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbb4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fbb4-122">Requirements</span></span>



| <span data-ttu-id="7fbb4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbb4-123">Requirement</span></span> | <span data-ttu-id="7fbb4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbb4-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbb4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7fbb4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7fbb4-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fbb4-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7fbb4-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7fbb4-127">Library</span></span><br/> | <dl> <span data-ttu-id="7fbb4-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fbb4-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7fbb4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fbb4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbb4-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="7fbb4-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7fbb4-131">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-131">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> <dt>

[<span data-ttu-id="7fbb4-132">**D3DXVec2Scale**</span><span class="sxs-lookup"><span data-stu-id="7fbb4-132">**D3DXVec2Scale**</span></span>](d3dxvec2scale.md)
</dt> </dl>

 

 




