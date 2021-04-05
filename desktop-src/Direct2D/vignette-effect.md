---
title: Efeito de Vignette
description: Esmaece a imagem de entrada nas bordas para uma cor definida pelo usuário.
ms.assetid: 34da221f-44a2-1d01-d88d-d7846b9770b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fe9302a86a49b060aa05ecb856ce43122d946d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085974"
---
# <a name="vignette-effect"></a><span data-ttu-id="efada-103">Efeito de Vignette</span><span class="sxs-lookup"><span data-stu-id="efada-103">Vignette effect</span></span>

<span data-ttu-id="efada-104">Esmaece a imagem de entrada nas bordas para uma cor definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="efada-104">Fades the input image at the edges to a user-set color.</span></span>

<span data-ttu-id="efada-105">O CLSID para esse efeito é CLSID \_ D2D1Vignette.</span><span class="sxs-lookup"><span data-stu-id="efada-105">The CLSID for this effect is CLSID\_D2D1Vignette.</span></span>

-   [<span data-ttu-id="efada-106">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="efada-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="efada-107">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="efada-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="efada-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="efada-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="efada-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="efada-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="efada-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="efada-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="efada-111">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="efada-111">Example image</span></span>

![exemplo de saída de efeito](images/vignette-effect.png)

## <a name="sample-code"></a><span data-ttu-id="efada-113">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="efada-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> vignetteEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Vignette, &vignetteEffect);
 
vignetteEffect->SetInput(0, bitmap);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_COLOR, );
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_TRANSITION_SIZE, 0.1f);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_STRENGTH, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(vignetteEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="efada-114">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="efada-114">Effect properties</span></span>

<span data-ttu-id="efada-115">As propriedades para o efeito de Vignette são definidas pela enumeração de [**\_ \_ prop d2d1 Vignette**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) .</span><span class="sxs-lookup"><span data-stu-id="efada-115">The properties for the vignette effect are defined by the [**D2D1\_VIGNETTE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="efada-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efada-116">Requirements</span></span>

| <span data-ttu-id="efada-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="efada-117">Requirement</span></span> | <span data-ttu-id="efada-118">Valor</span><span class="sxs-lookup"><span data-stu-id="efada-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="efada-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efada-119">Minimum supported client</span></span> | <span data-ttu-id="efada-120">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="efada-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="efada-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efada-121">Minimum supported server</span></span> | <span data-ttu-id="efada-122">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="efada-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="efada-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="efada-123">Header</span></span>                   | <span data-ttu-id="efada-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="efada-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="efada-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="efada-125">Library</span></span>                  | <span data-ttu-id="efada-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="efada-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="efada-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="efada-127">Related topics</span></span>

* [<span data-ttu-id="efada-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="efada-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
