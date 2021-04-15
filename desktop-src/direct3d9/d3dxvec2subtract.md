---
description: Subtrai dois vetores 2D.
ms.assetid: e5a693e9-b143-41d5-923d-3f3f71461a42
title: Função D3DXVec2Subtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c12f41da7594f3eff9743eed7a1b0780f36c5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506471"
---
# <a name="d3dxvec2subtract-function"></a><span data-ttu-id="b8b79-103">Função D3DXVec2Subtract</span><span class="sxs-lookup"><span data-stu-id="b8b79-103">D3DXVec2Subtract function</span></span>

<span data-ttu-id="b8b79-104">Subtrai dois vetores 2D.</span><span class="sxs-lookup"><span data-stu-id="b8b79-104">Subtracts two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b79-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8b79-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Subtract(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="b8b79-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8b79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8b79-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b8b79-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b79-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8b79-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="b8b79-109">Ponteiro para a estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="b8b79-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b8b79-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b8b79-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b79-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="b8b79-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="b8b79-112">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="b8b79-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b8b79-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b8b79-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b79-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="b8b79-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="b8b79-115">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="b8b79-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8b79-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8b79-116">Return value</span></span>

<span data-ttu-id="b8b79-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8b79-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="b8b79-118">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que é a diferença de dois vetores.</span><span class="sxs-lookup"><span data-stu-id="b8b79-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8b79-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8b79-119">Remarks</span></span>

<span data-ttu-id="b8b79-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="b8b79-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b8b79-121">Dessa forma, a função **D3DXVec2Subtract** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="b8b79-121">In this way, the **D3DXVec2Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b79-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8b79-122">Requirements</span></span>



| <span data-ttu-id="b8b79-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8b79-123">Requirement</span></span> | <span data-ttu-id="b8b79-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b8b79-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b79-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8b79-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b8b79-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8b79-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b8b79-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8b79-127">Library</span></span><br/> | <dl> <span data-ttu-id="b8b79-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8b79-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b8b79-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8b79-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b79-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b8b79-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b8b79-131">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="b8b79-131">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
</dt> <dt>

[<span data-ttu-id="b8b79-132">**D3DXVec2Scale**</span><span class="sxs-lookup"><span data-stu-id="b8b79-132">**D3DXVec2Scale**</span></span>](d3dxvec2scale.md)
</dt> </dl>

 

 




