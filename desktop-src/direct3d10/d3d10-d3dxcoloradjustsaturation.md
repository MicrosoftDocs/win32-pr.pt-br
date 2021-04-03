---
description: Ajusta o valor de saturação de uma cor.
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: Função D3DXColorAdjustSaturation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6cfa4dd2af6e4a4ac3772af80ba11b8189405f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930696"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a><span data-ttu-id="f2a7e-103">Função D3DXColorAdjustSaturation (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f2a7e-103">D3DXColorAdjustSaturation function (D3DX10Math.h)</span></span>

<span data-ttu-id="f2a7e-104">Ajusta o valor de saturação de uma cor.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-104">Adjusts the saturation value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a7e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2a7e-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="f2a7e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2a7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2a7e-107">*pout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2a7e-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a7e-108">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2a7e-108">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="f2a7e-109">Ponteiro para um [**D3DXCOLOR**](d3d10-d3dxcolor.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-109">Pointer to a [**D3DXCOLOR**](d3d10-d3dxcolor.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f2a7e-110">*PC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2a7e-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a7e-111">Tipo: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2a7e-111">Type: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="f2a7e-112">Ponteiro para uma estrutura de D3DXCOLOR de origem.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-112">Pointer to a source D3DXCOLOR structure.</span></span>

</dd> <dt>

<span data-ttu-id="f2a7e-113">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="f2a7e-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a7e-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2a7e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2a7e-115">Valor de saturação.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-115">Saturation value.</span></span> <span data-ttu-id="f2a7e-116">Esse parâmetro interpola linearmente entre a cor convertida em escala de cinza e a cor original, pC.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-116">This parameter linearly interpolates between the color converted to grayscale and the original color, pC.</span></span> <span data-ttu-id="f2a7e-117">Não há limites para o valor de s.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-117">There are no limits on the value of s.</span></span> <span data-ttu-id="f2a7e-118">Se s for 0, a cor retornada será a cor de escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-118">If s is 0, the returned color is the grayscale color.</span></span> <span data-ttu-id="f2a7e-119">Se s for 1, a cor retornada será a cor original.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-119">If s is 1, the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2a7e-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2a7e-120">Return value</span></span>

<span data-ttu-id="f2a7e-121">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2a7e-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="f2a7e-122">Essa função retorna um ponteiro para uma estrutura D3DXCOLOR que é o resultado do ajuste de saturação.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-122">This function returns a pointer to a D3DXCOLOR structure that is the result of the saturation adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2a7e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2a7e-123">Remarks</span></span>

<span data-ttu-id="f2a7e-124">O canal alfa de entrada é copiado, não modificado, para o canal alfa de saída.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="f2a7e-125">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f2a7e-126">Dessa forma, essa função pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f2a7e-127">Essa função interpola os componentes de cor vermelho, verde e azul de uma estrutura D3DXCOLOR entre uma cor não saturada e uma cor, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-127">This function interpolates the red, green, and blue color components of a D3DXCOLOR structure between an unsaturated color and a color, as shown in the following example.</span></span>


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



<span data-ttu-id="f2a7e-128">Se s for maior que 0 e menor que 1, a saturação será diminuída.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-128">If s is greater than 0 and less than 1, the saturation is decreased.</span></span> <span data-ttu-id="f2a7e-129">Se s for maior que 1, a saturação será aumentada.</span><span class="sxs-lookup"><span data-stu-id="f2a7e-129">If s is greater than 1, the saturation is increased.</span></span>

<span data-ttu-id="f2a7e-130">A cor de escala de cinza é calculada como:</span><span class="sxs-lookup"><span data-stu-id="f2a7e-130">The grayscale color is computed as:</span></span>


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
```



## <a name="requirements"></a><span data-ttu-id="f2a7e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2a7e-131">Requirements</span></span>



| <span data-ttu-id="f2a7e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2a7e-132">Requirement</span></span> | <span data-ttu-id="f2a7e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f2a7e-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a7e-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2a7e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f2a7e-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2a7e-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f2a7e-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f2a7e-136">Library</span></span><br/> | <dl> <span data-ttu-id="f2a7e-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2a7e-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2a7e-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2a7e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2a7e-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f2a7e-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
