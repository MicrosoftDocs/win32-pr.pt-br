---
description: Adiciona dois vetores de harmônica esférica (SH); em outras palavras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .
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
ms.openlocfilehash: 1750b473764daf030160adc42d258a1f911f5f16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173139"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="33c2c-103">Função D3DXSHAdd (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="33c2c-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="33c2c-104">Adiciona dois vetores de harmônica esférica (SH); em outras palavras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="33c2c-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="33c2c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33c2c-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="33c2c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33c2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c2c-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33c2c-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c2c-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="33c2c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="33c2c-109">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="33c2c-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="33c2c-110">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="33c2c-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="33c2c-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="33c2c-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="33c2c-112">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33c2c-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c2c-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33c2c-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33c2c-114">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="33c2c-114">Order of the SH evaluation.</span></span> <span data-ttu-id="33c2c-115">Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="33c2c-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="33c2c-116">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="33c2c-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="33c2c-117">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="33c2c-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="33c2c-118">*PA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33c2c-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c2c-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="33c2c-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="33c2c-120">Aponta para o primeiro vetor SH.</span><span class="sxs-lookup"><span data-stu-id="33c2c-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="33c2c-121">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33c2c-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c2c-122">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="33c2c-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="33c2c-123">Aponta para o segundo vetor SH.</span><span class="sxs-lookup"><span data-stu-id="33c2c-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c2c-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33c2c-124">Return value</span></span>

<span data-ttu-id="33c2c-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="33c2c-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="33c2c-126">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="33c2c-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="33c2c-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="33c2c-127">Remarks</span></span>

<span data-ttu-id="33c2c-128">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="33c2c-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="33c2c-129">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="33c2c-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="33c2c-130">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="33c2c-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c2c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33c2c-131">Requirements</span></span>



| <span data-ttu-id="33c2c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="33c2c-132">Requirement</span></span> | <span data-ttu-id="33c2c-133">Valor</span><span class="sxs-lookup"><span data-stu-id="33c2c-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33c2c-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33c2c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="33c2c-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="33c2c-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="33c2c-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33c2c-136">Library</span></span><br/> | <dl> <span data-ttu-id="33c2c-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33c2c-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33c2c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="33c2c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c2c-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="33c2c-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
