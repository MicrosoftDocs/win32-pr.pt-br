---
title: Efeito de sépia
description: Converte uma imagem em tons de sépia.
ms.assetid: fe321be9-6ade-bd0c-1c66-cc8042e5a5e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6ead1d439e86cbd35be14d1f0ae32923de408d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918331"
---
# <a name="sepia-effect"></a><span data-ttu-id="3db7f-103">Efeito de sépia</span><span class="sxs-lookup"><span data-stu-id="3db7f-103">Sepia effect</span></span>

<span data-ttu-id="3db7f-104">Converte uma imagem em tons de sépia.</span><span class="sxs-lookup"><span data-stu-id="3db7f-104">Converts an image to sepia tones.</span></span>

<span data-ttu-id="3db7f-105">O CLSID para esse efeito é CLSID \_ D2D1Sepia.</span><span class="sxs-lookup"><span data-stu-id="3db7f-105">The CLSID for this effect is CLSID\_D2D1Sepia.</span></span>

-   [<span data-ttu-id="3db7f-106">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="3db7f-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="3db7f-107">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="3db7f-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="3db7f-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="3db7f-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="3db7f-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3db7f-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3db7f-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3db7f-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="3db7f-111">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="3db7f-111">Example image</span></span>

![exemplo de saída de efeito](images/sepia-effect.png)

## <a name="sample-code"></a><span data-ttu-id="3db7f-113">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="3db7f-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sepiaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sepia, &sepiaEffect);
 
sepiaEffect->SetInput(0, bitmap);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_INTENSITY, 0.75f);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(sepiaEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="3db7f-114">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="3db7f-114">Effect properties</span></span>

<span data-ttu-id="3db7f-115">As propriedades do efeito de sépia são definidas pela enumeração [**de \_ \_ prop d2d1 sépia**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) .</span><span class="sxs-lookup"><span data-stu-id="3db7f-115">The properties for the sepia effect are defined by the [**D2D1\_SEPIA\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="3db7f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3db7f-116">Requirements</span></span>



| <span data-ttu-id="3db7f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3db7f-117">Requirement</span></span> | <span data-ttu-id="3db7f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3db7f-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="3db7f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3db7f-119">Minimum supported client</span></span> | <span data-ttu-id="3db7f-120">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="3db7f-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="3db7f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3db7f-121">Minimum supported server</span></span> | <span data-ttu-id="3db7f-122">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="3db7f-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="3db7f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3db7f-123">Header</span></span>                   | <span data-ttu-id="3db7f-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="3db7f-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="3db7f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3db7f-125">Library</span></span>                  | <span data-ttu-id="3db7f-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="3db7f-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="3db7f-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3db7f-127">Related topics</span></span>

* [<span data-ttu-id="3db7f-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="3db7f-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




