---
description: Função D3DXSHRotateZ (D3dx9math. h) – gira o vetor harmônica esférico (SH) no eixo z pelo ângulo fornecido.
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: Função D3DXSHRotateZ (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed7db57dc3acedd1e65edab7377b525940ea10e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117844"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="12461-103">Função D3DXSHRotateZ (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="12461-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="12461-104">Gira o vetor harmônica (SH) esférico no eixo z pelo ângulo fornecido.</span><span class="sxs-lookup"><span data-stu-id="12461-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="12461-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12461-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="12461-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12461-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12461-107">*pout* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="12461-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12461-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="12461-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12461-109">Ponteiro para os coeficientes de saída harmônicas (SH).</span><span class="sxs-lookup"><span data-stu-id="12461-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="12461-110">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="12461-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="12461-111">Esse ponteiro não deve ser alias com *pIn*.</span><span class="sxs-lookup"><span data-stu-id="12461-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="12461-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="12461-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="12461-113">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12461-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12461-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12461-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12461-115">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="12461-115">Order of the SH evaluation.</span></span> <span data-ttu-id="12461-116">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="12461-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="12461-117">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="12461-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="12461-118">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="12461-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="12461-119">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12461-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12461-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12461-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12461-121">Ângulo de rotação em radianos.</span><span class="sxs-lookup"><span data-stu-id="12461-121">Rotation angle in radians.</span></span> <span data-ttu-id="12461-122">A rotação é executada em volta do eixo z.</span><span class="sxs-lookup"><span data-stu-id="12461-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="12461-123">*fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12461-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12461-124">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="12461-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12461-125">Ponteiro para de doeficientes de forma girada.</span><span class="sxs-lookup"><span data-stu-id="12461-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12461-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="12461-126">Return value</span></span>

<span data-ttu-id="12461-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="12461-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12461-128">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="12461-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="12461-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="12461-129">Remarks</span></span>

<span data-ttu-id="12461-130">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="12461-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="12461-131">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="12461-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="12461-132">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="12461-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="12461-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12461-133">Requirements</span></span>



| <span data-ttu-id="12461-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="12461-134">Requirement</span></span> | <span data-ttu-id="12461-135">Valor</span><span class="sxs-lookup"><span data-stu-id="12461-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12461-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12461-136">Header</span></span><br/>  | <dl> <span data-ttu-id="12461-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="12461-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="12461-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12461-138">Library</span></span><br/> | <dl> <span data-ttu-id="12461-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12461-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12461-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="12461-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12461-141">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="12461-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="12461-142">Transferência radiante de computação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="12461-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
