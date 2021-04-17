---
description: Determina o produto cruzado em quatro dimensões.
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
ms.openlocfilehash: 8e3e2a612740a207ea4dc44243ce24ebbab7fc08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105794569"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a><span data-ttu-id="b4a42-103">Função D3DXVec4Cross (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b4a42-103">D3DXVec4Cross function (D3DX10Math.h)</span></span>

<span data-ttu-id="b4a42-104">Determina o produto cruzado em quatro dimensões.</span><span class="sxs-lookup"><span data-stu-id="b4a42-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a42-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4a42-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="b4a42-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4a42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4a42-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b4a42-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a42-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4a42-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b4a42-109">Ponteiro para o [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="b4a42-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b4a42-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4a42-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a42-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="b4a42-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b4a42-112">Ponteiro para uma estrutura de D3DXVECTOR4 de origem.</span><span class="sxs-lookup"><span data-stu-id="b4a42-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4a42-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4a42-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a42-114">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="b4a42-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b4a42-115">Ponteiro para uma estrutura de D3DXVECTOR4 de origem.</span><span class="sxs-lookup"><span data-stu-id="b4a42-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4a42-116">*pV3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4a42-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a42-117">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="b4a42-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b4a42-118">Ponteiro para uma estrutura de D3DXVECTOR4 de origem.</span><span class="sxs-lookup"><span data-stu-id="b4a42-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4a42-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4a42-119">Return value</span></span>

<span data-ttu-id="b4a42-120">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4a42-120">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b4a42-121">Ponteiro para uma estrutura D3DXVECTOR4 que é o produto cruzado.</span><span class="sxs-lookup"><span data-stu-id="b4a42-121">Pointer to a D3DXVECTOR4 structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4a42-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4a42-122">Remarks</span></span>

<span data-ttu-id="b4a42-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="b4a42-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b4a42-124">Dessa forma, a função D3DXVec4Cross pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="b4a42-124">In this way, the D3DXVec4Cross function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a42-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4a42-125">Requirements</span></span>



| <span data-ttu-id="b4a42-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a42-126">Requirement</span></span> | <span data-ttu-id="b4a42-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b4a42-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a42-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4a42-128">Header</span></span><br/> | <dl> <span data-ttu-id="b4a42-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4a42-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a42-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4a42-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a42-131">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b4a42-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
