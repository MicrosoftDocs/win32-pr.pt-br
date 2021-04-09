---
title: Efeito de detecção de borda
description: Filtra o conteúdo de uma imagem, deixando linhas nas bordas das seções contrastantes da imagem.
ms.assetid: d22868cf-95fe-690e-66ac-268d7e116aee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47239bede77dc5d32582c6e83c8101e5c9bbf2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009769"
---
# <a name="edge-detection-effect"></a><span data-ttu-id="6c3e1-103">Efeito de detecção de borda</span><span class="sxs-lookup"><span data-stu-id="6c3e1-103">Edge-detection effect</span></span>

<span data-ttu-id="6c3e1-104">Filtra o conteúdo de uma imagem, deixando linhas nas bordas das seções contrastantes da imagem.</span><span class="sxs-lookup"><span data-stu-id="6c3e1-104">Filters out the content of an image, leaving lines at the edges of contrasting sections of the image.</span></span>

<span data-ttu-id="6c3e1-105">O CLSID para esse efeito é CLSID \_ D2D1EdgeDetection.</span><span class="sxs-lookup"><span data-stu-id="6c3e1-105">The CLSID for this effect is CLSID\_D2D1EdgeDetection.</span></span>

-   [<span data-ttu-id="6c3e1-106">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="6c3e1-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="6c3e1-107">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="6c3e1-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="6c3e1-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="6c3e1-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="6c3e1-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="6c3e1-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6c3e1-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c3e1-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="6c3e1-111">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="6c3e1-111">Example image</span></span>

![exemplo de saída de efeito](images/edge-detection-effect.png)

## <a name="sample-code"></a><span data-ttu-id="6c3e1-113">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="6c3e1-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> edgeDetectionEffect;
m_d2dContext->CreateEffect(CLSID_D2D1EdgeDetection, &edgeDetectionEffect);
 
edgeDetectionEffect->SetInput(0, bitmap);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_STRENGTH, 0.5f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, 0.0f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_MODE_SOBEL);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, false);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(edgeDetectionEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="6c3e1-114">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="6c3e1-114">Effect properties</span></span>

<span data-ttu-id="6c3e1-115">As propriedades do efeito de detecção de borda são definidas pela enumeração de [**\_ \_ prop d2d1 EDGEDETECTION**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) .</span><span class="sxs-lookup"><span data-stu-id="6c3e1-115">The properties for the edge detection effect are defined by the [**D2D1\_EDGEDETECTION\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c3e1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c3e1-116">Requirements</span></span>



| <span data-ttu-id="6c3e1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c3e1-117">Requirement</span></span> | <span data-ttu-id="6c3e1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6c3e1-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="6c3e1-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c3e1-119">Minimum supported client</span></span> | <span data-ttu-id="6c3e1-120">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="6c3e1-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6c3e1-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c3e1-121">Minimum supported server</span></span> | <span data-ttu-id="6c3e1-122">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="6c3e1-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6c3e1-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c3e1-123">Header</span></span>                   | <span data-ttu-id="6c3e1-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="6c3e1-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="6c3e1-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c3e1-125">Library</span></span>                  | <span data-ttu-id="6c3e1-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="6c3e1-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="6c3e1-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c3e1-127">Related topics</span></span>

* [<span data-ttu-id="6c3e1-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="6c3e1-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
