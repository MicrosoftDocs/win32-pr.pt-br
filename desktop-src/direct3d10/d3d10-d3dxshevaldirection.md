---
description: Avalia as funções de base esférica harmônica (SH) de um vetor de direção de entrada.
ms.assetid: c86973cc-c5b0-4358-b7eb-5c31f38b5b5a
title: Função D3DXSHEvalDirection (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 698873f3278b37970120b03c25918096762ead34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104557391"
---
# <a name="d3dxshevaldirection-function-d3dx10h"></a><span data-ttu-id="fc778-103">Função D3DXSHEvalDirection (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="fc778-103">D3DXSHEvalDirection function (D3DX10.h)</span></span>

<span data-ttu-id="fc778-104">Avalia as funções de base esférica harmônica (SH) de um vetor de direção de entrada.</span><span class="sxs-lookup"><span data-stu-id="fc778-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc778-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc778-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _In_       FLOAT       *pOut,
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="fc778-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc778-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc778-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc778-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc778-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc778-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fc778-109">Ponteiro para os coeficientes de saída harmônicas (SH).</span><span class="sxs-lookup"><span data-stu-id="fc778-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="fc778-110">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="fc778-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="fc778-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="fc778-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fc778-112">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc778-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc778-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc778-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc778-114">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="fc778-114">Order of the SH evaluation.</span></span> <span data-ttu-id="fc778-115">Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="fc778-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="fc778-116">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="fc778-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="fc778-117">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="fc778-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="fc778-118">*pDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc778-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc778-119">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fc778-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fc778-120">(x, y, z) vetor de direção no qual avaliar as funções de base SH.</span><span class="sxs-lookup"><span data-stu-id="fc778-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="fc778-121">Deve ser normalizado.</span><span class="sxs-lookup"><span data-stu-id="fc778-121">Must be normalized.</span></span> <span data-ttu-id="fc778-122">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="fc778-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc778-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc778-123">Return value</span></span>

<span data-ttu-id="fc778-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc778-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fc778-125">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="fc778-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="fc778-126">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="fc778-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc778-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc778-127">Remarks</span></span>

<span data-ttu-id="fc778-128">Cada coeficiente da função base Ylm é armazenado no local da memória l ² + m + l, em que:</span><span class="sxs-lookup"><span data-stu-id="fc778-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="fc778-129">l é o grau da função base.</span><span class="sxs-lookup"><span data-stu-id="fc778-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="fc778-130">m é o índice de função base para o valor l fornecido e varia de-l a l, inclusive.</span><span class="sxs-lookup"><span data-stu-id="fc778-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="fc778-131">Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na direção da mão direita e Phi, o ângulo de z.</span><span class="sxs-lookup"><span data-stu-id="fc778-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

<span data-ttu-id="fc778-133">As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade.</span><span class="sxs-lookup"><span data-stu-id="fc778-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="fc778-134">O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.</span><span class="sxs-lookup"><span data-stu-id="fc778-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="fc778-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc778-136">Requirements</span></span>



| <span data-ttu-id="fc778-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc778-137">Requirement</span></span> | <span data-ttu-id="fc778-138">Valor</span><span class="sxs-lookup"><span data-stu-id="fc778-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc778-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc778-139">Header</span></span><br/>  | <dl> <span data-ttu-id="fc778-140"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc778-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc778-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc778-141">Library</span></span><br/> | <dl> <span data-ttu-id="fc778-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc778-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc778-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc778-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc778-144">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="fc778-144">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
