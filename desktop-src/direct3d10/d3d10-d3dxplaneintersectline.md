---
description: Localiza a interseção entre um plano e uma linha.
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
ms.openlocfilehash: 00d25fcba9e5884cec10da96964ad0f5daa9ed14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802123"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a><span data-ttu-id="454db-103">Função D3DXPlaneIntersectLine (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="454db-103">D3DXPlaneIntersectLine function (D3DX10Math.h)</span></span>

<span data-ttu-id="454db-104">Localiza a interseção entre um plano e uma linha.</span><span class="sxs-lookup"><span data-stu-id="454db-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="454db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="454db-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="454db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="454db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="454db-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="454db-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="454db-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="454db-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="454db-109">Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identificando a interseção entre o plano e a linha especificados.</span><span class="sxs-lookup"><span data-stu-id="454db-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="454db-110">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="454db-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="454db-111">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="454db-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="454db-112">Ponteiro para o [**D3DXPLANE**](d3d10-d3dxplane.md)de origem.</span><span class="sxs-lookup"><span data-stu-id="454db-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> <dt>

<span data-ttu-id="454db-113">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="454db-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="454db-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="454db-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="454db-115">Ponteiro para uma estrutura de D3DXVECTOR3 de origem, definindo um ponto de partida de linha.</span><span class="sxs-lookup"><span data-stu-id="454db-115">Pointer to a source D3DXVECTOR3 structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="454db-116">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="454db-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="454db-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="454db-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="454db-118">Ponteiro para uma estrutura de D3DXVECTOR3 de origem, definindo um ponto de extremidade de linha.</span><span class="sxs-lookup"><span data-stu-id="454db-118">Pointer to a source D3DXVECTOR3 structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="454db-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="454db-119">Return value</span></span>

<span data-ttu-id="454db-120">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="454db-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="454db-121">Ponteiro para uma estrutura D3DXVECTOR3 que é a interseção entre o plano e a linha especificados.</span><span class="sxs-lookup"><span data-stu-id="454db-121">Pointer to a D3DXVECTOR3 structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="454db-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="454db-122">Remarks</span></span>

<span data-ttu-id="454db-123">Se a linha for paralela ao plano, **NULL** será retornado.</span><span class="sxs-lookup"><span data-stu-id="454db-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="454db-124">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="454db-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="454db-125">Dessa forma, a função D3DXPlaneIntersectLine pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="454db-125">In this way, the D3DXPlaneIntersectLine function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="454db-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="454db-126">Requirements</span></span>



| <span data-ttu-id="454db-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="454db-127">Requirement</span></span> | <span data-ttu-id="454db-128">Valor</span><span class="sxs-lookup"><span data-stu-id="454db-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="454db-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="454db-129">Header</span></span><br/>  | <dl> <span data-ttu-id="454db-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="454db-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="454db-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="454db-131">Library</span></span><br/> | <dl> <span data-ttu-id="454db-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="454db-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="454db-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="454db-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="454db-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="454db-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
