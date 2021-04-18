---
description: Subtrai dois valores de cor para criar um novo valor de cor.
ms.assetid: c21f8402-c1c2-4909-896f-2872ef518537
title: Função D3DXColorSubtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorSubtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 47f28ea3a3fb6d1556e699fed3820e228faf6604
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790261"
---
# <a name="d3dxcolorsubtract-function"></a><span data-ttu-id="a1a8e-103">Função D3DXColorSubtract</span><span class="sxs-lookup"><span data-stu-id="a1a8e-103">D3DXColorSubtract function</span></span>

<span data-ttu-id="a1a8e-104">Subtrai dois valores de cor para criar um novo valor de cor.</span><span class="sxs-lookup"><span data-stu-id="a1a8e-104">Subtracts two color values to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a8e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1a8e-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorSubtract(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="a1a8e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1a8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1a8e-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a1a8e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a8e-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1a8e-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="a1a8e-109">Ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="a1a8e-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a1a8e-110"> \ \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a1a8e-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a8e-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1a8e-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="a1a8e-112">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="a1a8e-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a1a8e-113">*pC2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a1a8e-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a8e-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1a8e-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="a1a8e-115">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="a1a8e-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1a8e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1a8e-116">Return value</span></span>

<span data-ttu-id="a1a8e-117">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1a8e-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="a1a8e-118">Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é a diferença entre dois valores de cor.</span><span class="sxs-lookup"><span data-stu-id="a1a8e-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the difference between two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1a8e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1a8e-119">Remarks</span></span>

<span data-ttu-id="a1a8e-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="a1a8e-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a1a8e-121">Dessa forma, a função **D3DXColorSubtract** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="a1a8e-121">In this way, the **D3DXColorSubtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1a8e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1a8e-122">Requirements</span></span>



| <span data-ttu-id="a1a8e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1a8e-123">Requirement</span></span> | <span data-ttu-id="a1a8e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a1a8e-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a8e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1a8e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a1a8e-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8e-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a1a8e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1a8e-127">Library</span></span><br/> | <dl> <span data-ttu-id="a1a8e-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1a8e-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1a8e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1a8e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a8e-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="a1a8e-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a1a8e-131">**D3DXColorAdd**</span><span class="sxs-lookup"><span data-stu-id="a1a8e-131">**D3DXColorAdd**</span></span>](d3dxcoloradd.md)
</dt> </dl>

 

 




