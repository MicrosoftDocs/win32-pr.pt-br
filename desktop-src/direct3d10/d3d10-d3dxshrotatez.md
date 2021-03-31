---
description: Gira o vetor harmônica (SH) esférico no eixo z pelo ângulo fornecido.
ms.assetid: 7c4bec55-4a4c-4f7e-8849-1cac373a2340
title: Função D3DXSHRotateZ (D3DX10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0348dd8dfed9b100f64c53427ca2b77dd48ccded
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930670"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a><span data-ttu-id="ea684-103">Função D3DXSHRotateZ (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="ea684-103">D3DXSHRotateZ function (D3DX10.h)</span></span>

<span data-ttu-id="ea684-104">Gira o vetor harmônica (SH) esférico no eixo z pelo ângulo fornecido.</span><span class="sxs-lookup"><span data-stu-id="ea684-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea684-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea684-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="ea684-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea684-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea684-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea684-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea684-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea684-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ea684-109">Ponteiro para os coeficientes de saída harmônicas (SH).</span><span class="sxs-lookup"><span data-stu-id="ea684-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="ea684-110">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="ea684-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="ea684-111">Esse ponteiro não deve ser alias com pIn.</span><span class="sxs-lookup"><span data-stu-id="ea684-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="ea684-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="ea684-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ea684-113">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea684-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea684-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea684-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea684-115">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="ea684-115">Order of the SH evaluation.</span></span> <span data-ttu-id="ea684-116">Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="ea684-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="ea684-117">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="ea684-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="ea684-118">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="ea684-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="ea684-119">*Ângulo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea684-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea684-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea684-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea684-121">Ângulo de rotação em radianos.</span><span class="sxs-lookup"><span data-stu-id="ea684-121">Rotation angle in radians.</span></span> <span data-ttu-id="ea684-122">A rotação é executada em volta do eixo z.</span><span class="sxs-lookup"><span data-stu-id="ea684-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="ea684-123">*fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea684-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea684-124">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea684-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ea684-125">Ponteiro para de doeficientes de forma girada.</span><span class="sxs-lookup"><span data-stu-id="ea684-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea684-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea684-126">Return value</span></span>

<span data-ttu-id="ea684-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea684-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ea684-128">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="ea684-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea684-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea684-129">Remarks</span></span>

<span data-ttu-id="ea684-130">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="ea684-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="ea684-131">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="ea684-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="ea684-132">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="ea684-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea684-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea684-133">Requirements</span></span>



| <span data-ttu-id="ea684-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea684-134">Requirement</span></span> | <span data-ttu-id="ea684-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ea684-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea684-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea684-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ea684-137"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea684-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea684-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea684-138">Library</span></span><br/> | <dl> <span data-ttu-id="ea684-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea684-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea684-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea684-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea684-141">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="ea684-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
