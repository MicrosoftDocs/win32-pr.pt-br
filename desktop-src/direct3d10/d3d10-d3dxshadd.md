---
description: Função D3DXSHAdd (D3DX10. h) – adiciona dois vetores de harmônica esférica (SH); em outras palavras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: Função D3DXSHAdd (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8d39940fef4ad611ea530d95efea29c74266d22a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108654"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="69b72-103">Função D3DXSHAdd (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="69b72-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="69b72-104">Adiciona dois vetores de harmônica esférica (SH); em outras palavras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="69b72-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="69b72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69b72-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="69b72-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69b72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b72-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69b72-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b72-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="69b72-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="69b72-109">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="69b72-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="69b72-110">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="69b72-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="69b72-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="69b72-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="69b72-112">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69b72-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b72-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69b72-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69b72-114">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="69b72-114">Order of the SH evaluation.</span></span> <span data-ttu-id="69b72-115">Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="69b72-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="69b72-116">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="69b72-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="69b72-117">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="69b72-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="69b72-118">*PA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69b72-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b72-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="69b72-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="69b72-120">Aponta para o primeiro vetor SH.</span><span class="sxs-lookup"><span data-stu-id="69b72-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="69b72-121">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69b72-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b72-122">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="69b72-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="69b72-123">Aponta para o segundo vetor SH.</span><span class="sxs-lookup"><span data-stu-id="69b72-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b72-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="69b72-124">Return value</span></span>

<span data-ttu-id="69b72-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="69b72-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="69b72-126">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="69b72-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="69b72-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="69b72-127">Remarks</span></span>

<span data-ttu-id="69b72-128">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="69b72-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="69b72-129">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="69b72-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="69b72-130">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="69b72-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b72-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69b72-131">Requirements</span></span>



| <span data-ttu-id="69b72-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="69b72-132">Requirement</span></span> | <span data-ttu-id="69b72-133">Valor</span><span class="sxs-lookup"><span data-stu-id="69b72-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69b72-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69b72-134">Header</span></span><br/>  | <dl> <span data-ttu-id="69b72-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b72-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="69b72-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69b72-136">Library</span></span><br/> | <dl> <span data-ttu-id="69b72-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69b72-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b72-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="69b72-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b72-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="69b72-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
