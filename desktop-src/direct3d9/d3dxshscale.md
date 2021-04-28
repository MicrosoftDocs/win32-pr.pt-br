---
description: Função D3DXSHScale (D3dx9math. h) – dimensiona um vetor harmônica (SH) esférico; em outras palavras, pOut \[ i \] = PA \[ \] \* escala.
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: Função D3DXSHScale (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6a91c3ea1cb49c4c501ab847cb63fe8a39d66665
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093854"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a><span data-ttu-id="162d3-103">Função D3DXSHScale (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="162d3-103">D3DXSHScale function (D3dx9math.h)</span></span>

<span data-ttu-id="162d3-104">Dimensiona um vetor harmônica (SH) esférico; em outras palavras, pOut \[ i \] = PA \[ \] \* escala.</span><span class="sxs-lookup"><span data-stu-id="162d3-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="162d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="162d3-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
);
```



## <a name="parameters"></a><span data-ttu-id="162d3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="162d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="162d3-107">*pout* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="162d3-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="162d3-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="162d3-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="162d3-109">Ponteiro para os coeficientes de saída harmônicas (SH).</span><span class="sxs-lookup"><span data-stu-id="162d3-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="162d3-110">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="162d3-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="162d3-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="162d3-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="162d3-112">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="162d3-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="162d3-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="162d3-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="162d3-114">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="162d3-114">Order of the SH evaluation.</span></span> <span data-ttu-id="162d3-115">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="162d3-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="162d3-116">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="162d3-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="162d3-117">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="162d3-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="162d3-118">*fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="162d3-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="162d3-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="162d3-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="162d3-120">Ponteiro para o vetor SH a ser dimensionado.</span><span class="sxs-lookup"><span data-stu-id="162d3-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="162d3-121">*Escala* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="162d3-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="162d3-122">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="162d3-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="162d3-123">Ponteiro para o valor de escala.</span><span class="sxs-lookup"><span data-stu-id="162d3-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="162d3-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="162d3-124">Return value</span></span>

<span data-ttu-id="162d3-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="162d3-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="162d3-126">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="162d3-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="162d3-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="162d3-127">Remarks</span></span>

<span data-ttu-id="162d3-128">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="162d3-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="162d3-129">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="162d3-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="162d3-130">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="162d3-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="162d3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="162d3-131">Requirements</span></span>



| <span data-ttu-id="162d3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="162d3-132">Requirement</span></span> | <span data-ttu-id="162d3-133">Valor</span><span class="sxs-lookup"><span data-stu-id="162d3-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="162d3-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="162d3-134">Header</span></span><br/>  | <dl> <span data-ttu-id="162d3-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="162d3-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="162d3-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="162d3-136">Library</span></span><br/> | <dl> <span data-ttu-id="162d3-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="162d3-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="162d3-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="162d3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="162d3-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="162d3-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="162d3-140">Transferência radiante de computação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="162d3-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
