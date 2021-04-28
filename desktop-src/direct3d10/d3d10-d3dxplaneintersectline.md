---
description: Função D3DXPlaneIntersectLine (D3DX10Math. h) – localiza a interseção entre um plano e uma linha.
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: Função D3DXPlaneIntersectLine (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1d32bb312c97b793f492f7a29bebe11529b79cf9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108804"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a><span data-ttu-id="310e5-103">Função D3DXPlaneIntersectLine (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="310e5-103">D3DXPlaneIntersectLine function (D3DX10Math.h)</span></span>

<span data-ttu-id="310e5-104">Localiza a interseção entre um plano e uma linha.</span><span class="sxs-lookup"><span data-stu-id="310e5-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="310e5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="310e5-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="310e5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="310e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="310e5-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="310e5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="310e5-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="310e5-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="310e5-109">Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identificando a interseção entre o plano e a linha especificados.</span><span class="sxs-lookup"><span data-stu-id="310e5-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="310e5-110">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="310e5-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="310e5-111">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="310e5-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="310e5-112">Ponteiro para o [**D3DXPLANE**](d3d10-d3dxplane.md)de origem.</span><span class="sxs-lookup"><span data-stu-id="310e5-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> <dt>

<span data-ttu-id="310e5-113">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="310e5-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="310e5-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="310e5-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="310e5-115">Ponteiro para uma estrutura de D3DXVECTOR3 de origem, definindo um ponto de partida de linha.</span><span class="sxs-lookup"><span data-stu-id="310e5-115">Pointer to a source D3DXVECTOR3 structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="310e5-116">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="310e5-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="310e5-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="310e5-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="310e5-118">Ponteiro para uma estrutura de D3DXVECTOR3 de origem, definindo um ponto de extremidade de linha.</span><span class="sxs-lookup"><span data-stu-id="310e5-118">Pointer to a source D3DXVECTOR3 structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="310e5-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="310e5-119">Return value</span></span>

<span data-ttu-id="310e5-120">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="310e5-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="310e5-121">Ponteiro para uma estrutura D3DXVECTOR3 que é a interseção entre o plano e a linha especificados.</span><span class="sxs-lookup"><span data-stu-id="310e5-121">Pointer to a D3DXVECTOR3 structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="310e5-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="310e5-122">Remarks</span></span>

<span data-ttu-id="310e5-123">Se a linha for paralela ao plano, **NULL** será retornado.</span><span class="sxs-lookup"><span data-stu-id="310e5-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="310e5-124">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="310e5-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="310e5-125">Dessa forma, a função D3DXPlaneIntersectLine pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="310e5-125">In this way, the D3DXPlaneIntersectLine function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="310e5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="310e5-126">Requirements</span></span>



| <span data-ttu-id="310e5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="310e5-127">Requirement</span></span> | <span data-ttu-id="310e5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="310e5-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="310e5-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="310e5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="310e5-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="310e5-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="310e5-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="310e5-131">Library</span></span><br/> | <dl> <span data-ttu-id="310e5-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="310e5-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="310e5-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="310e5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="310e5-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="310e5-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
