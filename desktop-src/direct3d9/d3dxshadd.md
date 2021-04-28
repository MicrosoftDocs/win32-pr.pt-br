---
description: Função D3DXSHAdd (D3dx9math. h) – adiciona dois vetores de harmônica esférica (SH); em outras palavras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: Função D3DXSHAdd (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7333d1803b9f7ea7b056ff78ffd053bd6086184b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117954"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a><span data-ttu-id="46eaa-103">Função D3DXSHAdd (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="46eaa-103">D3DXSHAdd function (D3dx9math.h)</span></span>

<span data-ttu-id="46eaa-104">Adiciona dois vetores de harmônica esférica (SH); em outras palavras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="46eaa-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="46eaa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46eaa-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="46eaa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46eaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46eaa-107">*pout* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="46eaa-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46eaa-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="46eaa-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="46eaa-109">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="46eaa-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="46eaa-110">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="46eaa-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="46eaa-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="46eaa-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="46eaa-112">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46eaa-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46eaa-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46eaa-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46eaa-114">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="46eaa-114">Order of the SH evaluation.</span></span> <span data-ttu-id="46eaa-115">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="46eaa-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="46eaa-116">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="46eaa-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="46eaa-117">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="46eaa-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="46eaa-118">*PA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46eaa-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46eaa-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="46eaa-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="46eaa-120">Aponta para o primeiro vetor SH.</span><span class="sxs-lookup"><span data-stu-id="46eaa-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="46eaa-121">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46eaa-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46eaa-122">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="46eaa-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="46eaa-123">Aponta para o segundo vetor SH.</span><span class="sxs-lookup"><span data-stu-id="46eaa-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46eaa-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="46eaa-124">Return value</span></span>

<span data-ttu-id="46eaa-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="46eaa-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="46eaa-126">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="46eaa-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="46eaa-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="46eaa-127">Remarks</span></span>

<span data-ttu-id="46eaa-128">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="46eaa-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="46eaa-129">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="46eaa-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="46eaa-130">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="46eaa-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="46eaa-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46eaa-131">Requirements</span></span>



| <span data-ttu-id="46eaa-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="46eaa-132">Requirement</span></span> | <span data-ttu-id="46eaa-133">Valor</span><span class="sxs-lookup"><span data-stu-id="46eaa-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46eaa-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46eaa-134">Header</span></span><br/>  | <dl> <span data-ttu-id="46eaa-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="46eaa-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="46eaa-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46eaa-136">Library</span></span><br/> | <dl> <span data-ttu-id="46eaa-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46eaa-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="46eaa-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="46eaa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46eaa-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="46eaa-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="46eaa-140">Transferência radiante de computação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="46eaa-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
