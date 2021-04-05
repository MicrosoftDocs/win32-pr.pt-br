---
title: Efeito de matiz-to-RGB
description: Converte uma imagem HSL (Matiz, saturação, claridade) ou HSV (Matiz, saturação, valor) para o espaço de cores RGB.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918379"
---
# <a name="hue-to-rgb-effect"></a><span data-ttu-id="2be92-103">Efeito de matiz-to-RGB</span><span class="sxs-lookup"><span data-stu-id="2be92-103">Hue-to-RGB effect</span></span>

<span data-ttu-id="2be92-104">Converte uma imagem HSL (Matiz, saturação, claridade) ou HSV (Matiz, saturação, valor) para o espaço de cores RGB.</span><span class="sxs-lookup"><span data-stu-id="2be92-104">Converts an HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) image to the RGB color space.</span></span>

<span data-ttu-id="2be92-105">HSL e HSV são dois modelos diferentes para representar uma cor RGB em um espaço de cores cilíndrico.</span><span class="sxs-lookup"><span data-stu-id="2be92-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="2be92-106">Eles são úteis porque permitem que você tenha uma razão de uma cor usando conceitos mais intuitivos, como matiz e intensidade versus combinar valores vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="2be92-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="2be92-107">Esse efeito passa por quaisquer valores Alfa de entrada.</span><span class="sxs-lookup"><span data-stu-id="2be92-107">This effect passes through any input alpha values.</span></span>

<span data-ttu-id="2be92-108">O CLSID para esse efeito é CLSID \_ D2D1HueToRgb.</span><span class="sxs-lookup"><span data-stu-id="2be92-108">The CLSID for this effect is CLSID\_D2D1HueToRgb.</span></span>

<span data-ttu-id="2be92-109">Para inverter o comportamento desse efeito, use o [efeito de RGB para matiz](rgb-to-hue-effect.md).</span><span class="sxs-lookup"><span data-stu-id="2be92-109">To reverse the behavior of this effect, use the [RGB to Hue effect](rgb-to-hue-effect.md).</span></span>

-   [<span data-ttu-id="2be92-110">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="2be92-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="2be92-111">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="2be92-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="2be92-112">Requirements</span><span class="sxs-lookup"><span data-stu-id="2be92-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2be92-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2be92-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="2be92-114">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="2be92-114">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="2be92-115">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="2be92-115">Effect properties</span></span>

<span data-ttu-id="2be92-116">As propriedades do efeito de contraste são definidas pela enumeração [**de \_ \_ prop d2d1 HUETORGB**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) .</span><span class="sxs-lookup"><span data-stu-id="2be92-116">The properties for the contrast effect are defined by the [**D2D1\_HUETORGB\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="2be92-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2be92-117">Requirements</span></span>



| <span data-ttu-id="2be92-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2be92-118">Requirement</span></span> | <span data-ttu-id="2be92-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2be92-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="2be92-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2be92-120">Minimum supported client</span></span> | <span data-ttu-id="2be92-121">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="2be92-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2be92-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2be92-122">Minimum supported server</span></span> | <span data-ttu-id="2be92-123">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="2be92-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2be92-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2be92-124">Header</span></span>                   | <span data-ttu-id="2be92-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="2be92-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="2be92-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2be92-126">Library</span></span>                  | <span data-ttu-id="2be92-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="2be92-127">d2d1.lib, dxguid.lib</span></span>                              |



## <a name="related-topics"></a><span data-ttu-id="2be92-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2be92-128">Related topics</span></span>

* [<span data-ttu-id="2be92-129">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="2be92-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
