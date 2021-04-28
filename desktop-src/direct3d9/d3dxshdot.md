---
description: Função D3DXSHDot (D3dx9math. h) – computa o produto dot de dois vetores de harmônica esférica (SH).
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: Função D3DXSHDot (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87f88c7c7b80871a68084607cb99621199dfcc0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093924"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a><span data-ttu-id="b9095-103">Função D3DXSHDot (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b9095-103">D3DXSHDot function (D3dx9math.h)</span></span>

<span data-ttu-id="b9095-104">Computa o produto de ponto de dois vetores de harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="b9095-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9095-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9095-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="b9095-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9095-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9095-107">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9095-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9095-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9095-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9095-109">Ordem da avaliação harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="b9095-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="b9095-110">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="b9095-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="b9095-111">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="b9095-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="b9095-112">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="b9095-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="b9095-113">*PA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9095-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9095-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9095-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b9095-115">Aponta para o primeiro vetor SH.</span><span class="sxs-lookup"><span data-stu-id="b9095-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="b9095-116">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9095-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9095-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9095-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b9095-118">Aponta para o segundo vetor SH.</span><span class="sxs-lookup"><span data-stu-id="b9095-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9095-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b9095-119">Return value</span></span>

<span data-ttu-id="b9095-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9095-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9095-121">SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="b9095-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9095-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9095-122">Remarks</span></span>

<span data-ttu-id="b9095-123">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="b9095-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="b9095-124">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="b9095-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="b9095-125">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="b9095-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9095-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9095-126">Requirements</span></span>



| <span data-ttu-id="b9095-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9095-127">Requirement</span></span> | <span data-ttu-id="b9095-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b9095-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9095-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9095-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b9095-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9095-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b9095-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9095-131">Library</span></span><br/> | <dl> <span data-ttu-id="b9095-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9095-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b9095-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b9095-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9095-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b9095-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b9095-135">Transferência radiante de computação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b9095-135">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
