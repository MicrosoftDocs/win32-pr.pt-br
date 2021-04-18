---
description: Ajusta o valor de saturação de uma cor.
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: Função D3DXColorAdjustSaturation (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d9a801a8355c1a9399f9864f9b1753bbecc17b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105758713"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a><span data-ttu-id="50b61-103">Função D3DXColorAdjustSaturation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="50b61-103">D3DXColorAdjustSaturation function (D3dx9math.h)</span></span>

<span data-ttu-id="50b61-104">Ajusta o valor de saturação de uma cor.</span><span class="sxs-lookup"><span data-stu-id="50b61-104">Adjusts the saturation value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b61-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50b61-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="50b61-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50b61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50b61-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="50b61-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50b61-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="50b61-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="50b61-109">Ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="50b61-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="50b61-110">*PC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50b61-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50b61-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="50b61-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="50b61-112">Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="50b61-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="50b61-113">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="50b61-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50b61-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50b61-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50b61-115">Valor de saturação.</span><span class="sxs-lookup"><span data-stu-id="50b61-115">Saturation value.</span></span> <span data-ttu-id="50b61-116">Esse parâmetro interpola linearmente entre a cor convertida em escala de cinza e a cor original, pC.</span><span class="sxs-lookup"><span data-stu-id="50b61-116">This parameter linearly interpolates between the color converted to grayscale and the original color, pC.</span></span> <span data-ttu-id="50b61-117">Não há limites para o valor de s.</span><span class="sxs-lookup"><span data-stu-id="50b61-117">There are no limits on the value of s.</span></span> <span data-ttu-id="50b61-118">Se s for 0, a cor retornada será a cor de escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="50b61-118">If s is 0, the returned color is the grayscale color.</span></span> <span data-ttu-id="50b61-119">Se s for 1, a cor retornada será a cor original.</span><span class="sxs-lookup"><span data-stu-id="50b61-119">If s is 1, the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50b61-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50b61-120">Return value</span></span>

<span data-ttu-id="50b61-121">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="50b61-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="50b61-122">Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado do ajuste de saturação.</span><span class="sxs-lookup"><span data-stu-id="50b61-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the saturation adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="50b61-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="50b61-123">Remarks</span></span>

<span data-ttu-id="50b61-124">O canal alfa de entrada é copiado, não modificado, para o canal alfa de saída.</span><span class="sxs-lookup"><span data-stu-id="50b61-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="50b61-125">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="50b61-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="50b61-126">Dessa forma, essa função pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="50b61-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="50b61-127">Essa função interpola os componentes de cor vermelho, verde e azul de uma estrutura [**D3DXCOLOR**](d3dxcolor.md) entre uma cor não saturada e uma cor, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="50b61-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between an unsaturated color and a color, as shown in the following example.</span></span>


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



<span data-ttu-id="50b61-128">Se s for maior que 0 e menor que 1, a saturação será diminuída.</span><span class="sxs-lookup"><span data-stu-id="50b61-128">If s is greater than 0 and less than 1, the saturation is decreased.</span></span> <span data-ttu-id="50b61-129">Se s for maior que 1, a saturação será aumentada.</span><span class="sxs-lookup"><span data-stu-id="50b61-129">If s is greater than 1, the saturation is increased.</span></span>

<span data-ttu-id="50b61-130">A cor de escala de cinza é calculada como:</span><span class="sxs-lookup"><span data-stu-id="50b61-130">The grayscale color is computed as:</span></span>


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
```



## <a name="requirements"></a><span data-ttu-id="50b61-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50b61-131">Requirements</span></span>



| <span data-ttu-id="50b61-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="50b61-132">Requirement</span></span> | <span data-ttu-id="50b61-133">Valor</span><span class="sxs-lookup"><span data-stu-id="50b61-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50b61-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50b61-134">Header</span></span><br/>  | <dl> <span data-ttu-id="50b61-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="50b61-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="50b61-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50b61-136">Library</span></span><br/> | <dl> <span data-ttu-id="50b61-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50b61-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50b61-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="50b61-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b61-139">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="50b61-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="50b61-140">**D3DXColorAdjustContrast**</span><span class="sxs-lookup"><span data-stu-id="50b61-140">**D3DXColorAdjustContrast**</span></span>](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
