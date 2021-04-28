---
description: Função D3DXPlaneFromPoints (D3DX10Math. h) – constrói um plano a partir de três pontos.
ms.assetid: 0e77af1b-cedf-482c-8398-10becb398a2c
title: Função D3DXPlaneFromPoints (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a3af01df7d1ce66029994226d040544b733a75df
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103314"
---
# <a name="d3dxplanefrompoints-function-d3dx10mathh"></a><span data-ttu-id="d6c11-103">Função D3DXPlaneFromPoints (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d6c11-103">D3DXPlaneFromPoints function (D3DX10Math.h)</span></span>

<span data-ttu-id="d6c11-104">Constrói um plano a partir de três pontos.</span><span class="sxs-lookup"><span data-stu-id="d6c11-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c11-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6c11-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="d6c11-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6c11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c11-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d6c11-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c11-108">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6c11-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="d6c11-109">Ponteiro para o [**D3DXPLANE**](d3d10-d3dxplane.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d6c11-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d6c11-110">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6c11-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c11-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6c11-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6c11-112">Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), definindo um dos pontos usados para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="d6c11-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="d6c11-113">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6c11-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c11-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6c11-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6c11-115">Ponteiro para uma estrutura D3DXVECTOR3, definindo um dos pontos usados para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="d6c11-115">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="d6c11-116">*pV3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6c11-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c11-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6c11-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6c11-118">Ponteiro para uma estrutura D3DXVECTOR3, definindo um dos pontos usados para construir o plano.</span><span class="sxs-lookup"><span data-stu-id="d6c11-118">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c11-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d6c11-119">Return value</span></span>

<span data-ttu-id="d6c11-120">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6c11-120">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="d6c11-121">Ponteiro para a estrutura D3DXPLANE construída a partir dos pontos especificados.</span><span class="sxs-lookup"><span data-stu-id="d6c11-121">Pointer to the D3DXPLANE structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6c11-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6c11-122">Remarks</span></span>

<span data-ttu-id="d6c11-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="d6c11-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d6c11-124">Dessa forma, a função D3DXPlaneFromPoints pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d6c11-124">In this way, the D3DXPlaneFromPoints function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c11-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6c11-125">Requirements</span></span>



| <span data-ttu-id="d6c11-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c11-126">Requirement</span></span> | <span data-ttu-id="d6c11-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d6c11-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c11-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6c11-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d6c11-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c11-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d6c11-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6c11-130">Library</span></span><br/> | <dl> <span data-ttu-id="d6c11-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6c11-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d6c11-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d6c11-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c11-133">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d6c11-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
