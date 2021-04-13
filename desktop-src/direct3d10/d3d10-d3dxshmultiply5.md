---
description: Computa o produto de duas funções de harmônica esféricas (f e g). Ambas as funções são da ordem N = 5.
ms.assetid: c72231a1-9db3-4701-b7ad-4509028ce508
title: Função D3DXSHMultiply5 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply5
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b43fb89bdd5d6f75a4adca86323786d4a2bddac1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298764"
---
# <a name="d3dxshmultiply5-function"></a><span data-ttu-id="72031-104">Função D3DXSHMultiply5</span><span class="sxs-lookup"><span data-stu-id="72031-104">D3DXSHMultiply5 function</span></span>

<span data-ttu-id="72031-105">Computa o produto de duas funções de harmônica esféricas (f e g).</span><span class="sxs-lookup"><span data-stu-id="72031-105">Computes the product of two spherical harmonics functions (f and g).</span></span> <span data-ttu-id="72031-106">Ambas as funções são da ordem N = 5.</span><span class="sxs-lookup"><span data-stu-id="72031-106">Both functions are of order N = 5.</span></span>

## <a name="syntax"></a><span data-ttu-id="72031-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72031-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply5(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="72031-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72031-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72031-109">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72031-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72031-110">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="72031-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="72031-111">Ponteiro para a saída SH dieficientes – a função base *Y* LM é armazenada em *l*² + *m* + l.</span><span class="sxs-lookup"><span data-stu-id="72031-111">Pointer to the output SH coefficients — the basis function *Y* ₗₘ is stored at *l*² + *m* + l.</span></span> <span data-ttu-id="72031-112">A ordem N determina o comprimento da matriz, onde sempre deve haver *N*² coeficientes.</span><span class="sxs-lookup"><span data-stu-id="72031-112">The order N determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="72031-113">*PF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72031-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72031-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="72031-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="72031-115">Entrada SH coeficientes para a primeira função.</span><span class="sxs-lookup"><span data-stu-id="72031-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="72031-116">*PG* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72031-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72031-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="72031-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="72031-118">Segundo conjunto de entrada SH coeficientes.</span><span class="sxs-lookup"><span data-stu-id="72031-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72031-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72031-119">Return value</span></span>

<span data-ttu-id="72031-120">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="72031-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="72031-121">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="72031-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="72031-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="72031-122">Remarks</span></span>

<span data-ttu-id="72031-123">O produto de duas funções SH de Order N = 5 gera uma função SH da ordem 2 × *N* -1 = 9, mas os resultados são truncados.</span><span class="sxs-lookup"><span data-stu-id="72031-123">The product of two SH functions of order N = 5 generates an SH function of order 2 × *N* - 1 = 9, but the results are truncated.</span></span> <span data-ttu-id="72031-124">Isso significa que o produto está mudo ( *f* × *g*  =  *g* × *f* ), mas não associa ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span><span class="sxs-lookup"><span data-stu-id="72031-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span></span>

<span data-ttu-id="72031-125">Essa função usa a seguinte equação:</span><span class="sxs-lookup"><span data-stu-id="72031-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="72031-126">em que y \_ i (s) é a função base i sh e em que f (s) e g (s) usam a seguinte função sh:</span><span class="sxs-lookup"><span data-stu-id="72031-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="72031-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72031-127">Requirements</span></span>



| <span data-ttu-id="72031-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="72031-128">Requirement</span></span> | <span data-ttu-id="72031-129">Valor</span><span class="sxs-lookup"><span data-stu-id="72031-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72031-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72031-130">Header</span></span><br/>  | <dl> <span data-ttu-id="72031-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="72031-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="72031-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72031-132">Library</span></span><br/> | <dl> <span data-ttu-id="72031-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72031-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="72031-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="72031-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72031-135">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="72031-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
