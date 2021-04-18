---
description: Determina o produto cruzado em quatro dimensões.
ms.assetid: 10b965c9-7ed7-450c-86a0-114f068c888f
title: Função D3DXVec4Cross (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91e6e5662bff503ba96d96f135f98e60cf15c8fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173040"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a><span data-ttu-id="1e34b-103">Função D3DXVec4Cross (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1e34b-103">D3DXVec4Cross function (D3dx9math.h)</span></span>

<span data-ttu-id="1e34b-104">Determina o produto cruzado em quatro dimensões.</span><span class="sxs-lookup"><span data-stu-id="1e34b-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e34b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e34b-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="1e34b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e34b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e34b-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1e34b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e34b-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e34b-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1e34b-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1e34b-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1e34b-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e34b-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e34b-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1e34b-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1e34b-112">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="1e34b-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1e34b-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e34b-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e34b-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1e34b-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1e34b-115">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="1e34b-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1e34b-116">*pV3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e34b-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e34b-117">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1e34b-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1e34b-118">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="1e34b-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e34b-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e34b-119">Return value</span></span>

<span data-ttu-id="1e34b-120">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e34b-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1e34b-121">Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o produto cruzado.</span><span class="sxs-lookup"><span data-stu-id="1e34b-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e34b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e34b-122">Remarks</span></span>

<span data-ttu-id="1e34b-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="1e34b-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1e34b-124">Dessa forma, a função **D3DXVec4Cross** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="1e34b-124">In this way, the **D3DXVec4Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e34b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e34b-125">Requirements</span></span>



| <span data-ttu-id="1e34b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e34b-126">Requirement</span></span> | <span data-ttu-id="1e34b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1e34b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e34b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e34b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1e34b-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e34b-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1e34b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e34b-130">Library</span></span><br/> | <dl> <span data-ttu-id="1e34b-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e34b-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1e34b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e34b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e34b-133">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="1e34b-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1e34b-134">**D3DXVec4Dot**</span><span class="sxs-lookup"><span data-stu-id="1e34b-134">**D3DXVec4Dot**</span></span>](d3dxvec4dot.md)
</dt> </dl>

 

 




