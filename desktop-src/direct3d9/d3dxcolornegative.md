---
description: Cria o valor de cor negativo de um valor de cor.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: Função D3DXColorNegative (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6d4d8559e64580897aec5261c450dc739496e75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760792"
---
# <a name="d3dxcolornegative-function"></a><span data-ttu-id="17e63-103">Função D3DXColorNegative</span><span class="sxs-lookup"><span data-stu-id="17e63-103">D3DXColorNegative function</span></span>

<span data-ttu-id="17e63-104">Cria o valor de cor negativo de um valor de cor.</span><span class="sxs-lookup"><span data-stu-id="17e63-104">Creates the negative color value of a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e63-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17e63-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
);
```



## <a name="parameters"></a><span data-ttu-id="17e63-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17e63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e63-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="17e63-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="17e63-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="17e63-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="17e63-109">Ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="17e63-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="17e63-110">*PC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17e63-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17e63-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="17e63-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="17e63-112">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="17e63-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17e63-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17e63-113">Return value</span></span>

<span data-ttu-id="17e63-114">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="17e63-114">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="17e63-115">Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o valor de cor negativo do valor de cor.</span><span class="sxs-lookup"><span data-stu-id="17e63-115">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the negative color value of the color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e63-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="17e63-116">Remarks</span></span>

<span data-ttu-id="17e63-117">O canal alfa de entrada é copiado, não modificado, para o canal alfa de saída.</span><span class="sxs-lookup"><span data-stu-id="17e63-117">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="17e63-118">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="17e63-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="17e63-119">Dessa forma, a função **D3DXColorNegative** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="17e63-119">In this way, the **D3DXColorNegative** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="17e63-120">Essa função retorna o valor de cor negativo subtraindo 1,0 dos componentes de cor da estrutura [**D3DXCOLOR**](d3dxcolor.md) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="17e63-120">This function returns the negative color value by subtracting 1.0 from the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure, as shown in the following example.</span></span>


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a><span data-ttu-id="17e63-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17e63-121">Requirements</span></span>



| <span data-ttu-id="17e63-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="17e63-122">Requirement</span></span> | <span data-ttu-id="17e63-123">Valor</span><span class="sxs-lookup"><span data-stu-id="17e63-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17e63-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17e63-124">Header</span></span><br/>  | <dl> <span data-ttu-id="17e63-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="17e63-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="17e63-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17e63-126">Library</span></span><br/> | <dl> <span data-ttu-id="17e63-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17e63-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="17e63-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="17e63-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e63-129">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="17e63-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="17e63-130">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="17e63-130">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="17e63-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="17e63-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="17e63-132">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="17e63-132">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




