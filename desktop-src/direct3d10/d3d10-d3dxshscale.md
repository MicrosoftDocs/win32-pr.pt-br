---
description: Dimensiona um vetor harmônica (SH) esférico; em outras palavras, pOut \[ i \] = PA \[ \] \* escala.
ms.assetid: e323d238-f635-4780-982d-8798ba178f31
title: Função D3DXSHScale (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7aa7ee66b29c7d9816708a8625bb568426a62b57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763861"
---
# <a name="d3dxshscale-function-d3dx10h"></a><span data-ttu-id="d1f43-103">Função D3DXSHScale (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d1f43-103">D3DXSHScale function (D3DX10.h)</span></span>

<span data-ttu-id="d1f43-104">Dimensiona um vetor harmônica (SH) esférico; em outras palavras, pOut \[ i \] = PA \[ \] \* escala.</span><span class="sxs-lookup"><span data-stu-id="d1f43-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1f43-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1f43-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pIn,
  _In_ const FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="d1f43-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1f43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1f43-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1f43-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f43-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1f43-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d1f43-109">Ponteiro para os coeficientes de saída harmônicas (SH).</span><span class="sxs-lookup"><span data-stu-id="d1f43-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="d1f43-110">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="d1f43-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="d1f43-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="d1f43-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d1f43-112">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1f43-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f43-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1f43-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1f43-114">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="d1f43-114">Order of the SH evaluation.</span></span> <span data-ttu-id="d1f43-115">Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="d1f43-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="d1f43-116">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="d1f43-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="d1f43-117">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="d1f43-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="d1f43-118">*fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1f43-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f43-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d1f43-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d1f43-120">Ponteiro para o vetor SH a ser dimensionado.</span><span class="sxs-lookup"><span data-stu-id="d1f43-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="d1f43-121">*Escala* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1f43-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f43-122">Tipo: **const [**float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1f43-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1f43-123">Ponteiro para o valor de escala.</span><span class="sxs-lookup"><span data-stu-id="d1f43-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1f43-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1f43-124">Return value</span></span>

<span data-ttu-id="d1f43-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1f43-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d1f43-126">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="d1f43-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1f43-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1f43-127">Remarks</span></span>

<span data-ttu-id="d1f43-128">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="d1f43-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="d1f43-129">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="d1f43-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="d1f43-130">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="d1f43-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1f43-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1f43-131">Requirements</span></span>



| <span data-ttu-id="d1f43-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1f43-132">Requirement</span></span> | <span data-ttu-id="d1f43-133">Valor</span><span class="sxs-lookup"><span data-stu-id="d1f43-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1f43-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1f43-134">Header</span></span><br/>  | <dl> <span data-ttu-id="d1f43-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1f43-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1f43-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1f43-136">Library</span></span><br/> | <dl> <span data-ttu-id="d1f43-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1f43-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1f43-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1f43-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1f43-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d1f43-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
