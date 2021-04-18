---
description: Computa o produto de duas funções representadas usando SH (f e g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: Função D3DXSHMultiply2 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105795453"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a><span data-ttu-id="fd6a9-103">Função D3DXSHMultiply2 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fd6a9-103">D3DXSHMultiply2 function (D3dx9math.h)</span></span>

<span data-ttu-id="fd6a9-104">Computa o produto de duas funções representadas usando SH (f e g).</span><span class="sxs-lookup"><span data-stu-id="fd6a9-104">Computes the product of two functions represented using SH (f and g).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6a9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd6a9-105">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="fd6a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd6a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6a9-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd6a9-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6a9-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd6a9-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fd6a9-109">O ponteiro para a saída SH Ylm de função de base é armazenado em l \* l + m + l.</span><span class="sxs-lookup"><span data-stu-id="fd6a9-109">Pointer to the output SH coefficients - basis function Ylm is stored at l\*l + m+l.</span></span>

</dd> <dt>

<span data-ttu-id="fd6a9-110">*PF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd6a9-110">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6a9-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd6a9-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fd6a9-112">Entrada SH coeffs para a primeira função.</span><span class="sxs-lookup"><span data-stu-id="fd6a9-112">Input SH coeffs for first function.</span></span>

</dd> <dt>

<span data-ttu-id="fd6a9-113">*PG* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd6a9-113">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6a9-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd6a9-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fd6a9-115">Segundo conjunto de entrada SH coeffs.</span><span class="sxs-lookup"><span data-stu-id="fd6a9-115">Second set of input SH coeffs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd6a9-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd6a9-116">Return value</span></span>

<span data-ttu-id="fd6a9-117">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd6a9-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fd6a9-118">Ponteiro para SH coeficientes de saída.</span><span class="sxs-lookup"><span data-stu-id="fd6a9-118">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd6a9-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd6a9-119">Remarks</span></span>

<span data-ttu-id="fd6a9-120">A ordem é um número entre 2 e 6, inclusive.</span><span class="sxs-lookup"><span data-stu-id="fd6a9-120">The order is a number between 2 and 6 inclusive.</span></span> <span data-ttu-id="fd6a9-121">Dessa forma, essa página documenta várias funções: D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.</span><span class="sxs-lookup"><span data-stu-id="fd6a9-121">So this page actually documents several functions: D3DXSHMultiply2, D3DXSHMultiply3, ... D3DXSHMultiply6.</span></span>

<span data-ttu-id="fd6a9-122">Computa o produto de duas funções representadas usando SH (f e g), em que *pout* \[ i \] = int (y i (s) f (s) \_ \* \* g (s)), em que y \_ i (s) é a função base i i, f (s) e g (s) são funções sh (Sum \_ i ( \_ s) \* c \_ i)).</span><span class="sxs-lookup"><span data-stu-id="fd6a9-122">Computes the product of two functions represented using SH (f and g), where *pOut*\[i\] = int(y\_i(s) \* f(s) \* g(s)), where y\_i(s) is the ith SH basis function, f(s) and g(s) are SH functions (sum\_i(y\_i(s)\*c\_i)).</span></span> <span data-ttu-id="fd6a9-123">A ordem o determina os comprimentos das matrizes, em que sempre deve haver O ^ 2 coeficientes.</span><span class="sxs-lookup"><span data-stu-id="fd6a9-123">The order O determines the lengths of the arrays, where there should always be O^2 coefficients.</span></span> <span data-ttu-id="fd6a9-124">Em geral, o produto de duas funções SH de Order O gera uma função SH da ordem 2 \* o-1, mas os resultados são truncados.</span><span class="sxs-lookup"><span data-stu-id="fd6a9-124">In general the product of two SH functions of order O generates an SH function of order 2\*O - 1, but the results are truncated.</span></span> <span data-ttu-id="fd6a9-125">Isso significa que o produto faz o mudo (f \* g = = g \* f), mas não associa (f \* (g \* h)! = (f \* g) \* h.</span><span class="sxs-lookup"><span data-stu-id="fd6a9-125">This means that the product commutes (f\*g == g\*f) but doesn't associate (f\*(g\*h) != (f\*g)\*h.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd6a9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd6a9-126">Requirements</span></span>



| <span data-ttu-id="fd6a9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd6a9-127">Requirement</span></span> | <span data-ttu-id="fd6a9-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fd6a9-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6a9-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd6a9-129">Header</span></span><br/> | <dl> <span data-ttu-id="fd6a9-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd6a9-130"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd6a9-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd6a9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6a9-132">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="fd6a9-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
