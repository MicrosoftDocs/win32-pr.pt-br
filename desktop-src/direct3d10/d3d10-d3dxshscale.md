---
description: Função D3DXSHScale (D3DX10. h) – dimensiona um vetor harmônica (SH) esférico; em outras palavras, pOut \[ i \] = PA \[ \] \* escala.
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
ms.openlocfilehash: 0fab96575e5542eaaed725a88f9ba52c3289a4ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108494"
---
# <a name="d3dxshscale-function-d3dx10h"></a><span data-ttu-id="79f87-103">Função D3DXSHScale (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="79f87-103">D3DXSHScale function (D3DX10.h)</span></span>

<span data-ttu-id="79f87-104">Dimensiona um vetor harmônica (SH) esférico; em outras palavras, pOut \[ i \] = PA \[ \] \* escala.</span><span class="sxs-lookup"><span data-stu-id="79f87-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="79f87-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79f87-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pIn,
  _In_ const FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="79f87-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79f87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79f87-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79f87-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79f87-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="79f87-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="79f87-109">Ponteiro para os coeficientes de saída harmônicas (SH).</span><span class="sxs-lookup"><span data-stu-id="79f87-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="79f87-110">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="79f87-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="79f87-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="79f87-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="79f87-112">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79f87-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79f87-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79f87-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79f87-114">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="79f87-114">Order of the SH evaluation.</span></span> <span data-ttu-id="79f87-115">Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="79f87-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="79f87-116">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="79f87-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="79f87-117">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="79f87-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="79f87-118">*fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79f87-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79f87-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="79f87-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="79f87-120">Ponteiro para o vetor SH a ser dimensionado.</span><span class="sxs-lookup"><span data-stu-id="79f87-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="79f87-121">*Escala* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79f87-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79f87-122">Tipo: **const [**float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79f87-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79f87-123">Ponteiro para o valor de escala.</span><span class="sxs-lookup"><span data-stu-id="79f87-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79f87-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="79f87-124">Return value</span></span>

<span data-ttu-id="79f87-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="79f87-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="79f87-126">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="79f87-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="79f87-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="79f87-127">Remarks</span></span>

<span data-ttu-id="79f87-128">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="79f87-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="79f87-129">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="79f87-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="79f87-130">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="79f87-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="79f87-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79f87-131">Requirements</span></span>



| <span data-ttu-id="79f87-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="79f87-132">Requirement</span></span> | <span data-ttu-id="79f87-133">Valor</span><span class="sxs-lookup"><span data-stu-id="79f87-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79f87-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79f87-134">Header</span></span><br/>  | <dl> <span data-ttu-id="79f87-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="79f87-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="79f87-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79f87-136">Library</span></span><br/> | <dl> <span data-ttu-id="79f87-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79f87-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79f87-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="79f87-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f87-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="79f87-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
