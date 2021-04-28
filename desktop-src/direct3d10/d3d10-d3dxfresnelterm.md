---
description: Função D3DXFresnelTerm (D3DX10Math. h) – calcular o termo de Fresnel.
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: Função D3DXFresnelTerm (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9efa557d44451674d2ae4c48a58370e939760a03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113264"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a><span data-ttu-id="4bf5a-103">Função D3DXFresnelTerm (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4bf5a-103">D3DXFresnelTerm function (D3DX10Math.h)</span></span>

<span data-ttu-id="4bf5a-104">Calcule o termo Fresnel.</span><span class="sxs-lookup"><span data-stu-id="4bf5a-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf5a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4bf5a-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="4bf5a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4bf5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf5a-107">*CosTheta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4bf5a-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf5a-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bf5a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bf5a-109">O valor deve estar entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="4bf5a-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="4bf5a-110">*RefractionIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4bf5a-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf5a-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bf5a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bf5a-112">O índice de refração de um material.</span><span class="sxs-lookup"><span data-stu-id="4bf5a-112">The refraction index of a material.</span></span> <span data-ttu-id="4bf5a-113">O valor deve ser maior que 1.</span><span class="sxs-lookup"><span data-stu-id="4bf5a-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf5a-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4bf5a-114">Return value</span></span>

<span data-ttu-id="4bf5a-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bf5a-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bf5a-116">Essa função retorna o termo Fresnel para uma luz não polarizada.</span><span class="sxs-lookup"><span data-stu-id="4bf5a-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="4bf5a-117">CosTheta é o cosseno do ângulo do incidente.</span><span class="sxs-lookup"><span data-stu-id="4bf5a-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bf5a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4bf5a-118">Remarks</span></span>

<span data-ttu-id="4bf5a-119">Para localizar o termo de Fresnel (F):</span><span class="sxs-lookup"><span data-stu-id="4bf5a-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="4bf5a-120">Se um for um ângulo de incidência e B for o ângulo de refração, então</span><span class="sxs-lookup"><span data-stu-id="4bf5a-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]

Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="4bf5a-121">Em seguida, expandindo o usando as identidades trigonométricas e simplificando, você obtém:</span><span class="sxs-lookup"><span data-stu-id="4bf5a-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="4bf5a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bf5a-122">Requirements</span></span>



| <span data-ttu-id="4bf5a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bf5a-123">Requirement</span></span> | <span data-ttu-id="4bf5a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4bf5a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf5a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4bf5a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4bf5a-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bf5a-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4bf5a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4bf5a-127">Library</span></span><br/> | <dl> <span data-ttu-id="4bf5a-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bf5a-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4bf5a-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4bf5a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf5a-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="4bf5a-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
