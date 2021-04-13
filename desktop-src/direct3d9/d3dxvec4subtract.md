---
description: Subtrai dois vetores 4D.
ms.assetid: 3bc55b38-818e-40eb-859e-495ee28fc4ae
title: Função D3DXVec4Subtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1110930d8e37cf04f7de5129c2a72db4ecc4ac8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298876"
---
# <a name="d3dxvec4subtract-function"></a><span data-ttu-id="e3a5c-103">Função D3DXVec4Subtract</span><span class="sxs-lookup"><span data-stu-id="e3a5c-103">D3DXVec4Subtract function</span></span>

<span data-ttu-id="e3a5c-104">Subtrai dois vetores 4D.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-104">Subtracts two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a5c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3a5c-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Subtract(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="e3a5c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a5c-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e3a5c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a5c-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3a5c-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e3a5c-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e3a5c-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3a5c-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a5c-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3a5c-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e3a5c-112">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e3a5c-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3a5c-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a5c-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3a5c-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e3a5c-115">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a5c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3a5c-116">Return value</span></span>

<span data-ttu-id="e3a5c-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3a5c-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e3a5c-118">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é a diferença de dois vetores.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a5c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a5c-119">Remarks</span></span>

<span data-ttu-id="e3a5c-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="e3a5c-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e3a5c-121">Dessa forma, a função **D3DXVec4Subtract** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e3a5c-121">In this way, the **D3DXVec4Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a5c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3a5c-122">Requirements</span></span>



| <span data-ttu-id="e3a5c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a5c-123">Requirement</span></span> | <span data-ttu-id="e3a5c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e3a5c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a5c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3a5c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e3a5c-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a5c-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e3a5c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3a5c-127">Library</span></span><br/> | <dl> <span data-ttu-id="e3a5c-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3a5c-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3a5c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3a5c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a5c-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e3a5c-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e3a5c-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="e3a5c-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="e3a5c-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="e3a5c-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




