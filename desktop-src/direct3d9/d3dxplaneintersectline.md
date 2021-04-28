---
description: Função D3DXPlaneIntersectLine (D3dx9math. h) – localiza a interseção entre um plano e uma linha.
ms.assetid: 2723cd3e-fdc3-4aab-a089-0089e5b14e3e
title: Função D3DXPlaneIntersectLine (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9b89508079b0b400135f4ae39fd6fdfaed61952
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098064"
---
# <a name="d3dxplaneintersectline-function-d3dx9mathh"></a><span data-ttu-id="1fe8d-103">Função D3DXPlaneIntersectLine (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1fe8d-103">D3DXPlaneIntersectLine function (D3dx9math.h)</span></span>

<span data-ttu-id="1fe8d-104">Localiza a interseção entre um plano e uma linha.</span><span class="sxs-lookup"><span data-stu-id="1fe8d-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fe8d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fe8d-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="1fe8d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fe8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fe8d-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1fe8d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe8d-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1fe8d-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1fe8d-109">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) , identificando a interseção entre o plano e a linha especificados.</span><span class="sxs-lookup"><span data-stu-id="1fe8d-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="1fe8d-110">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fe8d-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe8d-111">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="1fe8d-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="1fe8d-112">Ponteiro para a estrutura de [**D3DXPLANE**](d3dxplane.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="1fe8d-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1fe8d-113">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fe8d-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe8d-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1fe8d-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1fe8d-115">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem, definindo um ponto de partida de linha.</span><span class="sxs-lookup"><span data-stu-id="1fe8d-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="1fe8d-116">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fe8d-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe8d-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1fe8d-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1fe8d-118">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem, definindo um ponto de extremidade de linha.</span><span class="sxs-lookup"><span data-stu-id="1fe8d-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fe8d-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1fe8d-119">Return value</span></span>

<span data-ttu-id="1fe8d-120">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1fe8d-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1fe8d-121">Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é a interseção entre o plano e a linha especificados.</span><span class="sxs-lookup"><span data-stu-id="1fe8d-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fe8d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fe8d-122">Remarks</span></span>

<span data-ttu-id="1fe8d-123">Se a linha for paralela ao plano, **NULL** será retornado.</span><span class="sxs-lookup"><span data-stu-id="1fe8d-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="1fe8d-124">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="1fe8d-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1fe8d-125">Dessa forma, a função **D3DXPlaneIntersectLine** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="1fe8d-125">In this way, the **D3DXPlaneIntersectLine** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe8d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fe8d-126">Requirements</span></span>



| <span data-ttu-id="1fe8d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fe8d-127">Requirement</span></span> | <span data-ttu-id="1fe8d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="1fe8d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe8d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fe8d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1fe8d-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fe8d-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1fe8d-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fe8d-131">Library</span></span><br/> | <dl> <span data-ttu-id="1fe8d-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fe8d-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1fe8d-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1fe8d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe8d-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="1fe8d-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




