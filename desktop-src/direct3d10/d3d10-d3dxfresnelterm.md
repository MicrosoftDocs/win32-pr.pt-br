---
description: Calcule o termo Fresnel.
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
ms.openlocfilehash: 1e87649d340e7d90c4df02c641919fd906631268
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506527"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a><span data-ttu-id="15398-103">Função D3DXFresnelTerm (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="15398-103">D3DXFresnelTerm function (D3DX10Math.h)</span></span>

<span data-ttu-id="15398-104">Calcule o termo Fresnel.</span><span class="sxs-lookup"><span data-stu-id="15398-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="15398-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15398-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="15398-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15398-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15398-107">*CosTheta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15398-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15398-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15398-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15398-109">O valor deve estar entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="15398-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="15398-110">*RefractionIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15398-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15398-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15398-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15398-112">O índice de refração de um material.</span><span class="sxs-lookup"><span data-stu-id="15398-112">The refraction index of a material.</span></span> <span data-ttu-id="15398-113">O valor deve ser maior que 1.</span><span class="sxs-lookup"><span data-stu-id="15398-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15398-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15398-114">Return value</span></span>

<span data-ttu-id="15398-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15398-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15398-116">Essa função retorna o termo Fresnel para uma luz não polarizada.</span><span class="sxs-lookup"><span data-stu-id="15398-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="15398-117">CosTheta é o cosseno do ângulo do incidente.</span><span class="sxs-lookup"><span data-stu-id="15398-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="15398-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="15398-118">Remarks</span></span>

<span data-ttu-id="15398-119">Para localizar o termo de Fresnel (F):</span><span class="sxs-lookup"><span data-stu-id="15398-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="15398-120">Se um for um ângulo de incidência e B for o ângulo de refração, então</span><span class="sxs-lookup"><span data-stu-id="15398-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]

Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="15398-121">Em seguida, expandindo o usando as identidades trigonométricas e simplificando, você obtém:</span><span class="sxs-lookup"><span data-stu-id="15398-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="15398-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15398-122">Requirements</span></span>



| <span data-ttu-id="15398-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="15398-123">Requirement</span></span> | <span data-ttu-id="15398-124">Valor</span><span class="sxs-lookup"><span data-stu-id="15398-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15398-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15398-125">Header</span></span><br/>  | <dl> <span data-ttu-id="15398-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="15398-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="15398-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15398-127">Library</span></span><br/> | <dl> <span data-ttu-id="15398-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15398-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15398-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="15398-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15398-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="15398-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
