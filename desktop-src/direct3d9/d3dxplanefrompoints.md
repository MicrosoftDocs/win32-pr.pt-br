---
description: Função D3DXPlaneFromPoints (D3dx9math. h) – constrói um plano a partir de três pontos.
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
ms.openlocfilehash: 0d945dff9c124f4c66cea4f9d61c490c6eaf7a66
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094154"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="7fd07-103">Função D3DXPlaneFromPoints (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7fd07-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="7fd07-104">Constrói um plano a partir de três pontos.</span><span class="sxs-lookup"><span data-stu-id="7fd07-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fd07-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="7fd07-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fd07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fd07-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7fd07-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd07-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="7fd07-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="7fd07-109">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="7fd07-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7fd07-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7fd07-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd07-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7fd07-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7fd07-112">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , definindo um dos pontos usados para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="7fd07-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="7fd07-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7fd07-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd07-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7fd07-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7fd07-115">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , definindo um dos pontos usados para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="7fd07-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="7fd07-116">*pV3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7fd07-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd07-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7fd07-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7fd07-118">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , definindo um dos pontos usados para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="7fd07-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fd07-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7fd07-119">Return value</span></span>

<span data-ttu-id="7fd07-120">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="7fd07-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="7fd07-121">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) construída a partir dos pontos especificados.</span><span class="sxs-lookup"><span data-stu-id="7fd07-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd07-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fd07-122">Remarks</span></span>

<span data-ttu-id="7fd07-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="7fd07-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7fd07-124">Dessa forma, a função **D3DXPlaneFromPoints** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="7fd07-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd07-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fd07-125">Requirements</span></span>



| <span data-ttu-id="7fd07-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fd07-126">Requirement</span></span> | <span data-ttu-id="7fd07-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7fd07-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd07-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7fd07-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7fd07-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fd07-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7fd07-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7fd07-130">Library</span></span><br/> | <dl> <span data-ttu-id="7fd07-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fd07-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7fd07-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7fd07-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd07-133">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="7fd07-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7fd07-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="7fd07-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




