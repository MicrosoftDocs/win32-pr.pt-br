---
description: Computa o produto de ponto de dois vetores de harmônica esférica (SH).
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: Função D3DXSHDot (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20f0896168dae0e2a779625c683777938c8e2df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782667"
---
# <a name="d3dxshdot-function-d3dx10h"></a><span data-ttu-id="23e78-103">Função D3DXSHDot (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="23e78-103">D3DXSHDot function (D3DX10.h)</span></span>

<span data-ttu-id="23e78-104">Computa o produto de ponto de dois vetores de harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="23e78-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e78-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23e78-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="23e78-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23e78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23e78-107">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23e78-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23e78-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23e78-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23e78-109">Ordem da avaliação harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="23e78-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="23e78-110">Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="23e78-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="23e78-111">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="23e78-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="23e78-112">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="23e78-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="23e78-113">*PA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23e78-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23e78-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="23e78-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="23e78-115">Aponta para o primeiro vetor SH.</span><span class="sxs-lookup"><span data-stu-id="23e78-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="23e78-116">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23e78-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23e78-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="23e78-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="23e78-118">Aponta para o segundo vetor SH.</span><span class="sxs-lookup"><span data-stu-id="23e78-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23e78-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23e78-119">Return value</span></span>

<span data-ttu-id="23e78-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23e78-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23e78-121">SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="23e78-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="23e78-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="23e78-122">Remarks</span></span>

<span data-ttu-id="23e78-123">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="23e78-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="23e78-124">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="23e78-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="23e78-125">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="23e78-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="23e78-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23e78-126">Requirements</span></span>



| <span data-ttu-id="23e78-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="23e78-127">Requirement</span></span> | <span data-ttu-id="23e78-128">Valor</span><span class="sxs-lookup"><span data-stu-id="23e78-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23e78-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23e78-129">Header</span></span><br/>  | <dl> <span data-ttu-id="23e78-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="23e78-130"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="23e78-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23e78-131">Library</span></span><br/> | <dl> <span data-ttu-id="23e78-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23e78-132"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23e78-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="23e78-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e78-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="23e78-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
