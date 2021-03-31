---
title: Croma-efeito de chave
description: Converte uma determinada cor mais ou menos uma tolerância para alfa. Por exemplo, croma-Key pode remover o plano de fundo de uma imagem para um efeito de sobreposição de tela verde.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a13d5558d103d6f937ed6638d0debbeddaf71dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824326"
---
# <a name="chroma-key-effect"></a><span data-ttu-id="1e50f-104">Croma-efeito de chave</span><span class="sxs-lookup"><span data-stu-id="1e50f-104">Chroma-key effect</span></span>

<span data-ttu-id="1e50f-105">Converte uma determinada cor mais ou menos uma tolerância para alfa.</span><span class="sxs-lookup"><span data-stu-id="1e50f-105">Converts a given color plus or minus a tolerance to alpha.</span></span> <span data-ttu-id="1e50f-106">Por exemplo, croma-Key pode remover o plano de fundo de uma imagem para um efeito de sobreposição de tela verde.</span><span class="sxs-lookup"><span data-stu-id="1e50f-106">For example, chroma-key can remove the background of an image for a green-screen overlay effect.</span></span>

<span data-ttu-id="1e50f-107">O CLSID para esse efeito é CLSID \_ D2D1ChromaKey.</span><span class="sxs-lookup"><span data-stu-id="1e50f-107">The CLSID for this effect is CLSID\_D2D1ChromaKey.</span></span>

-   [<span data-ttu-id="1e50f-108">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="1e50f-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="1e50f-109">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="1e50f-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="1e50f-110">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="1e50f-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="1e50f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e50f-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="1e50f-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e50f-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="1e50f-113">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="1e50f-113">Example image</span></span>

![exemplo de saída de efeito](images/chromakey-effect.png)

> [!Note]  
> <span data-ttu-id="1e50f-115">Neste exemplo, a saída do efeito croma é a segunda imagem com o plano de fundo transparente do xadrez.</span><span class="sxs-lookup"><span data-stu-id="1e50f-115">In this example, the output of the chroma-key effect is the second image with the checkerboard transparent background.</span></span> <span data-ttu-id="1e50f-116">A terceira imagem combina isso com uma imagem de plano de fundo para a sobreposição de tela verde final.</span><span class="sxs-lookup"><span data-stu-id="1e50f-116">The third image combines this with a background image for the final green-screen overlay.</span></span>

## <a name="sample-code"></a><span data-ttu-id="1e50f-117">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="1e50f-117">Sample code</span></span>

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="1e50f-118">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="1e50f-118">Effect properties</span></span>

<span data-ttu-id="1e50f-119">As propriedades para o efeito croma-Key são definidas pela enumeração [**d2d1 \_ Chromakey \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) .</span><span class="sxs-lookup"><span data-stu-id="1e50f-119">The properties for the chroma-key effect are defined by the [**D2D1\_CHROMAKEY\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e50f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e50f-120">Requirements</span></span>

| <span data-ttu-id="1e50f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e50f-121">Requirement</span></span> | <span data-ttu-id="1e50f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1e50f-122">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="1e50f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e50f-123">Minimum supported client</span></span> | <span data-ttu-id="1e50f-124">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="1e50f-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1e50f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e50f-125">Minimum supported server</span></span> | <span data-ttu-id="1e50f-126">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="1e50f-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1e50f-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e50f-127">Header</span></span>                   | <span data-ttu-id="1e50f-128">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="1e50f-128">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="1e50f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e50f-129">Library</span></span>                  | <span data-ttu-id="1e50f-130">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="1e50f-130">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="1e50f-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e50f-131">Related topics</span></span>

* [<span data-ttu-id="1e50f-132">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="1e50f-132">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
