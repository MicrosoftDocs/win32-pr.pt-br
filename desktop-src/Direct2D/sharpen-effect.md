---
title: Efeito de nitidez
description: Ajusta a imagem.
ms.assetid: 1eb12d1e-83c1-ba13-33be-df2078f3ccb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54203cfeb786204500c905e2ff4cfc83bf9719e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644569"
---
# <a name="sharpen-effect"></a><span data-ttu-id="74a0b-103">Efeito de nitidez</span><span class="sxs-lookup"><span data-stu-id="74a0b-103">Sharpen effect</span></span>

<span data-ttu-id="74a0b-104">Ajusta a imagem.</span><span class="sxs-lookup"><span data-stu-id="74a0b-104">Sharpens the image.</span></span>

<span data-ttu-id="74a0b-105">O CLSID para esse efeito é CLSID \_ D2D1Sharpen.</span><span class="sxs-lookup"><span data-stu-id="74a0b-105">The CLSID for this effect is CLSID\_D2D1Sharpen.</span></span>

-   [<span data-ttu-id="74a0b-106">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="74a0b-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="74a0b-107">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="74a0b-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="74a0b-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="74a0b-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="74a0b-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="74a0b-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="74a0b-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74a0b-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="74a0b-111">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="74a0b-111">Example image</span></span>

![exemplo de saída de efeito](images/sharpen-effect.png)

## <a name="sample-code"></a><span data-ttu-id="74a0b-113">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="74a0b-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sharpenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sharpen, &sharpenEffect);
 
sharpenEffect->SetInput(0, bitmap);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_SHARPNESS, 1.0f);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_THRESHOLD, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="74a0b-114">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="74a0b-114">Effect properties</span></span>

<span data-ttu-id="74a0b-115">As propriedades para o efeito de nitidez são definidas pela enumeração de [**\_ \_ prop d2d1 nitidez**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) .</span><span class="sxs-lookup"><span data-stu-id="74a0b-115">The properties for the sharpen effect are defined by the [**D2D1\_SHARPEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="74a0b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74a0b-116">Requirements</span></span>



| <span data-ttu-id="74a0b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="74a0b-117">Requirement</span></span> | <span data-ttu-id="74a0b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="74a0b-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="74a0b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74a0b-119">Minimum supported client</span></span> | <span data-ttu-id="74a0b-120">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="74a0b-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="74a0b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74a0b-121">Minimum supported server</span></span> | <span data-ttu-id="74a0b-122">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="74a0b-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="74a0b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74a0b-123">Header</span></span>                   | <span data-ttu-id="74a0b-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="74a0b-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="74a0b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74a0b-125">Library</span></span>                  | <span data-ttu-id="74a0b-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="74a0b-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="74a0b-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74a0b-127">Related topics</span></span>

* [<span data-ttu-id="74a0b-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="74a0b-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)



