---
title: Posterização do efeito
description: O efeito de Posterização reduz o número de cores exclusivas em uma imagem.
ms.assetid: e6686998-1246-b3b7-6f4f-212568c3191c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c98c55154300f7b29c23c24e97570335c6e930f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009541"
---
# <a name="posterize-effect"></a><span data-ttu-id="fd23a-103">Posterização do efeito</span><span class="sxs-lookup"><span data-stu-id="fd23a-103">Posterize effect</span></span>

<span data-ttu-id="fd23a-104">O efeito de Posterização reduz o número de cores exclusivas em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="fd23a-104">The posterize effect reduces the number of unique colors in an image.</span></span>

<span data-ttu-id="fd23a-105">O CLSID para esse efeito é CLSID \_ D2D1Posterize.</span><span class="sxs-lookup"><span data-stu-id="fd23a-105">The CLSID for this effect is CLSID\_D2D1Posterize.</span></span>

-   [<span data-ttu-id="fd23a-106">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="fd23a-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="fd23a-107">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="fd23a-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="fd23a-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="fd23a-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="fd23a-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="fd23a-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="fd23a-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd23a-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="fd23a-111">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="fd23a-111">Example image</span></span>

![exemplo de saída de efeito](images/posterize-effect.png)

## <a name="sample-code"></a><span data-ttu-id="fd23a-113">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="fd23a-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> posterizeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Posterize, &posterizeEffect);
 
posterizeEffect->SetInput(0, bitmap);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_RED_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT, 4);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(posterizeEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="fd23a-114">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="fd23a-114">Effect properties</span></span>

<span data-ttu-id="fd23a-115">As propriedades do efeito de Posterização são definidas pela enumeração [**d2d1 \_ poster \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop) .</span><span class="sxs-lookup"><span data-stu-id="fd23a-115">The properties for the posterize effect are defined by the [**D2D1\_POSTERIZE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd23a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd23a-116">Requirements</span></span>



| <span data-ttu-id="fd23a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd23a-117">Requirement</span></span> | <span data-ttu-id="fd23a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fd23a-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="fd23a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd23a-119">Minimum supported client</span></span> | <span data-ttu-id="fd23a-120">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="fd23a-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fd23a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd23a-121">Minimum supported server</span></span> | <span data-ttu-id="fd23a-122">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="fd23a-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fd23a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd23a-123">Header</span></span>                   | <span data-ttu-id="fd23a-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="fd23a-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="fd23a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd23a-125">Library</span></span>                  | <span data-ttu-id="fd23a-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="fd23a-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="fd23a-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd23a-127">Related topics</span></span>

* [<span data-ttu-id="fd23a-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="fd23a-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)


