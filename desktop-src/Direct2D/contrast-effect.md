---
title: Efeito de contraste
description: Aumenta ou reduz o contraste de uma imagem.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009476"
---
# <a name="contrast-effect"></a><span data-ttu-id="d96ef-103">Efeito de contraste</span><span class="sxs-lookup"><span data-stu-id="d96ef-103">Contrast effect</span></span>

<span data-ttu-id="d96ef-104">Aumenta ou reduz o contraste de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="d96ef-104">Increases or decreases the contrast of an image.</span></span>

<span data-ttu-id="d96ef-105">O CLSID para esse efeito é CLSID \_ D2D1Contrast.</span><span class="sxs-lookup"><span data-stu-id="d96ef-105">The CLSID for this effect is CLSID\_D2D1Contrast.</span></span>

<span data-ttu-id="d96ef-106">A função Contrast modifica cada valor de canal de cor usando dois, piecewises quadráticas de semipolinomiais que atendem à continuidade da inclinação no ponto (0,5, 0,5).</span><span class="sxs-lookup"><span data-stu-id="d96ef-106">The contrast function modifies each color channel value using two, piecewise quadratic polynomials that meet with slope continuity at the point (0.5, 0.5).</span></span>

![polinomiais quadráticas piecewise que atendem à continuidade da inclinação no ponto (0,5, 0,5)](images/contrast-effect-slope.png)

-   [<span data-ttu-id="d96ef-108">Imagens de exemplo</span><span class="sxs-lookup"><span data-stu-id="d96ef-108">Example Images</span></span>](#example-images)
-   [<span data-ttu-id="d96ef-109">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="d96ef-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="d96ef-110">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="d96ef-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="d96ef-111">Requirements</span><span class="sxs-lookup"><span data-stu-id="d96ef-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d96ef-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d96ef-112">Related topics</span></span>](#related-topics)

## <a name="example-images"></a><span data-ttu-id="d96ef-113">Imagens de exemplo</span><span class="sxs-lookup"><span data-stu-id="d96ef-113">Example images</span></span>

<span data-ttu-id="d96ef-114">Este exemplo mostra a saída do efeito com o contraste máximo aplicado (Contrast = 1,0).</span><span class="sxs-lookup"><span data-stu-id="d96ef-114">This example shows the output of the effect with maximum contrast applied (Contrast = 1.0).</span></span>

<span data-ttu-id="d96ef-115">Antes</span><span class="sxs-lookup"><span data-stu-id="d96ef-115">Before</span></span>

![imagem antes da aplicação do efeito](images/contrast-effect-before.png)

<span data-ttu-id="d96ef-117">After (após)</span><span class="sxs-lookup"><span data-stu-id="d96ef-117">After</span></span>

![imagem após o efeito ser aplicado](images/contrast-effect-after.png)

## <a name="sample-code"></a><span data-ttu-id="d96ef-119">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="d96ef-119">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="d96ef-120">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="d96ef-120">Effect properties</span></span>

<span data-ttu-id="d96ef-121">As propriedades do efeito de contraste são definidas pela enumeração [**de \_ \_ prop Contrast d2d1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) .</span><span class="sxs-lookup"><span data-stu-id="d96ef-121">The properties for the contrast effect are defined by the [**D2D1\_CONTRAST\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d96ef-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d96ef-122">Requirements</span></span>

| <span data-ttu-id="d96ef-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d96ef-123">Requirement</span></span> | <span data-ttu-id="d96ef-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d96ef-124">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="d96ef-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d96ef-125">Minimum supported client</span></span> | <span data-ttu-id="d96ef-126">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d96ef-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d96ef-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d96ef-127">Minimum supported server</span></span> | <span data-ttu-id="d96ef-128">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d96ef-128">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d96ef-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d96ef-129">Header</span></span>                   | <span data-ttu-id="d96ef-130">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="d96ef-130">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="d96ef-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d96ef-131">Library</span></span>                  | <span data-ttu-id="d96ef-132">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="d96ef-132">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="d96ef-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d96ef-133">Related topics</span></span>

* [<span data-ttu-id="d96ef-134">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="d96ef-134">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
