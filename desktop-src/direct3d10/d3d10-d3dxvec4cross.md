---
description: Função D3DXVec4Cross (D3DX10Math. h) – determina o produto cruzado em quatro dimensões.
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: Função D3DXVec4Cross (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: e52cc1adb1e48f65599b1bf7179f7953823f1e1c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102944"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a><span data-ttu-id="f3eac-103">Função D3DXVec4Cross (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f3eac-103">D3DXVec4Cross function (D3DX10Math.h)</span></span>

<span data-ttu-id="f3eac-104">Determina o produto cruzado em quatro dimensões.</span><span class="sxs-lookup"><span data-stu-id="f3eac-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3eac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3eac-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="f3eac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3eac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3eac-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f3eac-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eac-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3eac-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="f3eac-109">Ponteiro para o [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="f3eac-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f3eac-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eac-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f3eac-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="f3eac-112">Ponteiro para uma estrutura de D3DXVECTOR4 de origem.</span><span class="sxs-lookup"><span data-stu-id="f3eac-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f3eac-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eac-114">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f3eac-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="f3eac-115">Ponteiro para uma estrutura de D3DXVECTOR4 de origem.</span><span class="sxs-lookup"><span data-stu-id="f3eac-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-116">*pV3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f3eac-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eac-117">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f3eac-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="f3eac-118">Ponteiro para uma estrutura de D3DXVECTOR4 de origem.</span><span class="sxs-lookup"><span data-stu-id="f3eac-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3eac-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f3eac-119">Return value</span></span>

<span data-ttu-id="f3eac-120">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3eac-120">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="f3eac-121">Ponteiro para uma estrutura D3DXVECTOR4 que é o produto cruzado.</span><span class="sxs-lookup"><span data-stu-id="f3eac-121">Pointer to a D3DXVECTOR4 structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3eac-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3eac-122">Remarks</span></span>

<span data-ttu-id="f3eac-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="f3eac-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f3eac-124">Dessa forma, a função D3DXVec4Cross pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="f3eac-124">In this way, the D3DXVec4Cross function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3eac-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3eac-125">Requirements</span></span>



| <span data-ttu-id="f3eac-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3eac-126">Requirement</span></span> | <span data-ttu-id="f3eac-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f3eac-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3eac-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3eac-128">Header</span></span><br/> | <dl> <span data-ttu-id="f3eac-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3eac-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3eac-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f3eac-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3eac-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f3eac-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
