---
title: Efeito de RGB para matiz
description: Converte uma imagem RGB nos espaços de cores HSL (Matiz, saturação, claridade) ou HSV (Matiz, saturação, valor).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369532"
---
# <a name="rgb-to-hue-effect"></a><span data-ttu-id="5e252-103">Efeito de RGB para matiz</span><span class="sxs-lookup"><span data-stu-id="5e252-103">RGB-to-hue effect</span></span>

<span data-ttu-id="5e252-104">Converte uma imagem RGB nos espaços de cores HSL (Matiz, saturação, claridade) ou HSV (Matiz, saturação, valor).</span><span class="sxs-lookup"><span data-stu-id="5e252-104">Converts an RGB image to either the HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) color spaces.</span></span>

<span data-ttu-id="5e252-105">HSL e HSV são dois modelos diferentes para representar uma cor RGB em um espaço de cores cilíndrico.</span><span class="sxs-lookup"><span data-stu-id="5e252-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="5e252-106">Eles são úteis porque permitem que você tenha uma razão de uma cor usando conceitos mais intuitivos, como matiz e intensidade versus combinar valores vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="5e252-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="5e252-107">Esse efeito normaliza os dados de saída (Matiz, valor de saturação para HSV ou matiz, saturação, claridade para HSL) para o intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="5e252-107">This effect normalizes the output data (hue, saturation value for HSV or hue, saturation, lightness for HSL) to the range \[0, 1\].</span></span>

<span data-ttu-id="5e252-108">O CLSID para esse efeito é CLSID \_ D2D1RgbToHue.</span><span class="sxs-lookup"><span data-stu-id="5e252-108">The CLSID for this effect is CLSID\_D2D1RgbToHue.</span></span>

<span data-ttu-id="5e252-109">Para inverter o comportamento desse efeito, use o [efeito de matiz para RGB](hue-to-rgb-effect.md).</span><span class="sxs-lookup"><span data-stu-id="5e252-109">To reverse the behavior of this effect, use the [Hue to RGB effect](hue-to-rgb-effect.md).</span></span>

-   [<span data-ttu-id="5e252-110">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="5e252-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="5e252-111">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="5e252-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="5e252-112">Requirements</span><span class="sxs-lookup"><span data-stu-id="5e252-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5e252-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e252-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="5e252-114">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="5e252-114">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a><span data-ttu-id="5e252-115">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="5e252-115">Effect properties</span></span>

<span data-ttu-id="5e252-116">As propriedades do efeito de contraste são definidas pela enumeração [**de \_ \_ prop d2d1 RGBTOHUE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) .</span><span class="sxs-lookup"><span data-stu-id="5e252-116">The properties for the contrast effect are defined by the [**D2D1\_RGBTOHUE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e252-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e252-117">Requirements</span></span>



| <span data-ttu-id="5e252-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e252-118">Requirement</span></span> | <span data-ttu-id="5e252-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5e252-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="5e252-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e252-120">Minimum supported client</span></span> | <span data-ttu-id="5e252-121">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="5e252-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5e252-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e252-122">Minimum supported server</span></span> | <span data-ttu-id="5e252-123">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="5e252-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5e252-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e252-124">Header</span></span>                   | <span data-ttu-id="5e252-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="5e252-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="5e252-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e252-126">Library</span></span>                  | <span data-ttu-id="5e252-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="5e252-127">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="5e252-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e252-128">Related topics</span></span>

* [<span data-ttu-id="5e252-129">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="5e252-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
