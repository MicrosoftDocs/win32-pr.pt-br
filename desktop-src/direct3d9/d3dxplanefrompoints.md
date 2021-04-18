---
description: Constrói um plano a partir de três pontos.
ms.assetid: 13d5ce6b-0046-441b-b826-f34f4fe16979
title: Função D3DXPlaneFromPoints (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPoints
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c537915c56cdbbfb33228b0c5a5ea3f2acc2baff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798527"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="c1afd-103">Função D3DXPlaneFromPoints (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c1afd-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="c1afd-104">Constrói um plano a partir de três pontos.</span><span class="sxs-lookup"><span data-stu-id="c1afd-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1afd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1afd-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="c1afd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1afd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1afd-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c1afd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1afd-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c1afd-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c1afd-109">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="c1afd-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c1afd-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1afd-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1afd-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1afd-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c1afd-112">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , definindo um dos pontos usados para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="c1afd-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="c1afd-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1afd-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1afd-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1afd-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c1afd-115">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , definindo um dos pontos usados para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="c1afd-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="c1afd-116">*pV3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1afd-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1afd-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1afd-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c1afd-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , definindo um dos pontos usados para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="c1afd-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1afd-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1afd-119">Return value</span></span>

<span data-ttu-id="c1afd-120">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c1afd-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c1afd-121">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) construída a partir dos pontos especificados.</span><span class="sxs-lookup"><span data-stu-id="c1afd-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1afd-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1afd-122">Remarks</span></span>

<span data-ttu-id="c1afd-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="c1afd-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c1afd-124">Dessa forma, a função **D3DXPlaneFromPoints** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="c1afd-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1afd-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1afd-125">Requirements</span></span>



| <span data-ttu-id="c1afd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1afd-126">Requirement</span></span> | <span data-ttu-id="c1afd-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c1afd-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1afd-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1afd-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c1afd-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1afd-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c1afd-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1afd-130">Library</span></span><br/> | <dl> <span data-ttu-id="c1afd-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1afd-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1afd-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1afd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1afd-133">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="c1afd-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c1afd-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="c1afd-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




