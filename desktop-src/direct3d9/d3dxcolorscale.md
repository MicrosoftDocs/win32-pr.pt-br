---
description: Dimensiona um valor de cor.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: Função D3DXColorScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74020f302a26162df1e42cb4c9f020af3f64e59c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810272"
---
# <a name="d3dxcolorscale-function"></a><span data-ttu-id="ff444-103">Função D3DXColorScale</span><span class="sxs-lookup"><span data-stu-id="ff444-103">D3DXColorScale function</span></span>

<span data-ttu-id="ff444-104">Dimensiona um valor de cor.</span><span class="sxs-lookup"><span data-stu-id="ff444-104">Scales a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff444-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff444-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="ff444-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff444-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff444-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ff444-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff444-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff444-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ff444-109">Ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="ff444-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ff444-110">*PC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff444-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff444-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="ff444-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ff444-112">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="ff444-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ff444-113">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ff444-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff444-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff444-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff444-115">Fator de escala.</span><span class="sxs-lookup"><span data-stu-id="ff444-115">Scale factor.</span></span> <span data-ttu-id="ff444-116">Ele dimensiona a cor, tratando-a como um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="ff444-116">It scales the color, treating it like a 4D vector.</span></span> <span data-ttu-id="ff444-117">Não há limites para o valor de s.</span><span class="sxs-lookup"><span data-stu-id="ff444-117">There are no limits on the value of s.</span></span> <span data-ttu-id="ff444-118">Se s for 1, a cor resultante será a cor original.</span><span class="sxs-lookup"><span data-stu-id="ff444-118">If s is 1, the resulting color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff444-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff444-119">Return value</span></span>

<span data-ttu-id="ff444-120">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff444-120">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="ff444-121">Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o valor de cor dimensionado.</span><span class="sxs-lookup"><span data-stu-id="ff444-121">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the scaled color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff444-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff444-122">Remarks</span></span>

<span data-ttu-id="ff444-123">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="ff444-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ff444-124">Dessa forma, a função **D3DXColorScale** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="ff444-124">In this way, the **D3DXColorScale** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ff444-125">Essa função computa o valor de cor dimensionada multiplicando os componentes de cor da estrutura [**D3DXCOLOR**](d3dxcolor.md) pelo fator de escala especificado, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff444-125">This function computes the scaled color value by multiplying the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure by the specified scale factor, as shown in the following example.</span></span>


```
pOut->r = pC->r * s;
```



## <a name="requirements"></a><span data-ttu-id="ff444-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff444-126">Requirements</span></span>



| <span data-ttu-id="ff444-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff444-127">Requirement</span></span> | <span data-ttu-id="ff444-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ff444-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff444-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff444-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ff444-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff444-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ff444-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff444-131">Library</span></span><br/> | <dl> <span data-ttu-id="ff444-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff444-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ff444-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff444-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff444-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="ff444-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ff444-135">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="ff444-135">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="ff444-136">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="ff444-136">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="ff444-137">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="ff444-137">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> </dl>

 

 
