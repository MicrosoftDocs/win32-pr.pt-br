---
description: Computa o produto de duas funções de harmônica esféricas (f e g). Ambas as funções são da ordem N = 4.
ms.assetid: 05427a18-447e-45d7-a851-e580298c9a1f
title: Função D3DXSHMultiply4 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply4
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 13e8b62674ccbabbb03259f06b79f330424ddf84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173109"
---
# <a name="d3dxshmultiply4-function"></a><span data-ttu-id="12f59-104">Função D3DXSHMultiply4</span><span class="sxs-lookup"><span data-stu-id="12f59-104">D3DXSHMultiply4 function</span></span>

<span data-ttu-id="12f59-105">Computa o produto de duas funções de harmônica esféricas (*f* e *g*).</span><span class="sxs-lookup"><span data-stu-id="12f59-105">Computes the product of two spherical harmonics functions (*f* and *g*).</span></span> <span data-ttu-id="12f59-106">Ambas as funções são da ordem N = 4.</span><span class="sxs-lookup"><span data-stu-id="12f59-106">Both functions are of order N = 4.</span></span>

## <a name="syntax"></a><span data-ttu-id="12f59-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12f59-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply4(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="12f59-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12f59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12f59-109">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12f59-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f59-110">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="12f59-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12f59-111">Ponteiro para a saída SH-ineficientes – a função base *Y* LM é armazenada em l ² + *m* + l.</span><span class="sxs-lookup"><span data-stu-id="12f59-111">Pointer to the output SH coefficients — basis function *Y* ₗₘ is stored at l² + *m* + l.</span></span> <span data-ttu-id="12f59-112">A ordem *N* determina o comprimento da matriz, onde sempre deve haver *N*² coeficientes.</span><span class="sxs-lookup"><span data-stu-id="12f59-112">The order *N* determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="12f59-113">*PF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12f59-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f59-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="12f59-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12f59-115">Entrada SH coeficientes para a primeira função.</span><span class="sxs-lookup"><span data-stu-id="12f59-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="12f59-116">*PG* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12f59-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f59-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="12f59-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12f59-118">Segundo conjunto de entrada SH coeficientes.</span><span class="sxs-lookup"><span data-stu-id="12f59-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12f59-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12f59-119">Return value</span></span>

<span data-ttu-id="12f59-120">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="12f59-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12f59-121">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="12f59-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="12f59-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="12f59-122">Remarks</span></span>

<span data-ttu-id="12f59-123">O produto de duas funções SH de Order N = 4 gera uma função SH da ordem 2 × *N* -1 = 7, mas os resultados são truncados.</span><span class="sxs-lookup"><span data-stu-id="12f59-123">The product of two SH functions of order N = 4 generates an SH function of order 2 × *N* - 1 = 7, but the results are truncated.</span></span> <span data-ttu-id="12f59-124">Isso significa que o produto está mudo ( *f* × *g*  =  *g* × *f* ), mas não associa ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span><span class="sxs-lookup"><span data-stu-id="12f59-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span></span>

<span data-ttu-id="12f59-125">Essa função usa a seguinte equação:</span><span class="sxs-lookup"><span data-stu-id="12f59-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="12f59-126">em que y \_ i (s) é a função base i sh e em que f (s) e g (s) usam a seguinte função sh:</span><span class="sxs-lookup"><span data-stu-id="12f59-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="12f59-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12f59-127">Requirements</span></span>



| <span data-ttu-id="12f59-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="12f59-128">Requirement</span></span> | <span data-ttu-id="12f59-129">Valor</span><span class="sxs-lookup"><span data-stu-id="12f59-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12f59-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12f59-130">Header</span></span><br/>  | <dl> <span data-ttu-id="12f59-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="12f59-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="12f59-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12f59-132">Library</span></span><br/> | <dl> <span data-ttu-id="12f59-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12f59-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12f59-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="12f59-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f59-135">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="12f59-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
