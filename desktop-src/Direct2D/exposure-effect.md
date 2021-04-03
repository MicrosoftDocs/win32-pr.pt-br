---
title: Efeito de exposição
description: Aumente ou diminua a exposição da imagem.
ms.assetid: d384f539-5c19-53c7-e52b-bf833e221449
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6f5bda52fecc0b5e3896515b04a6560f17da49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918834"
---
# <a name="exposure-effect"></a><span data-ttu-id="221db-103">Efeito de exposição</span><span class="sxs-lookup"><span data-stu-id="221db-103">Exposure effect</span></span>

<span data-ttu-id="221db-104">Aumente ou diminua a exposição da imagem.</span><span class="sxs-lookup"><span data-stu-id="221db-104">Increase or decreases the exposure of the image.</span></span>

<span data-ttu-id="221db-105">O CLSID para esse efeito é CLSID \_ D2D1Exposure.</span><span class="sxs-lookup"><span data-stu-id="221db-105">The CLSID for this effect is CLSID\_D2D1Exposure.</span></span>

-   [<span data-ttu-id="221db-106">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="221db-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="221db-107">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="221db-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="221db-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="221db-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="221db-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="221db-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="221db-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="221db-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="221db-111">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="221db-111">Example image</span></span>

![exemplo de saída de efeito](images/exposure-effect.png)

## <a name="sample-code"></a><span data-ttu-id="221db-113">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="221db-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> exposureEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Exposure, &exposureEffect);
 
exposureEffect->SetInput(0, bitmap);
exposureEffect->SetValue(D2D1_EXPOSURE_PROP_EXPOSURE_VALUE, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(exposureEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="221db-114">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="221db-114">Effect properties</span></span>

<span data-ttu-id="221db-115">As propriedades do efeito de exposição são definidas pela enumeração [**de \_ \_ prop d2d1 Exposure**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) .</span><span class="sxs-lookup"><span data-stu-id="221db-115">The properties for the exposure effect are defined by the [**D2D1\_EXPOSURE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="221db-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="221db-116">Requirements</span></span>



| <span data-ttu-id="221db-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="221db-117">Requirement</span></span> | <span data-ttu-id="221db-118">Valor</span><span class="sxs-lookup"><span data-stu-id="221db-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="221db-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="221db-119">Minimum supported client</span></span> | <span data-ttu-id="221db-120">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="221db-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="221db-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="221db-121">Minimum supported server</span></span> | <span data-ttu-id="221db-122">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="221db-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="221db-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="221db-123">Header</span></span>                   | <span data-ttu-id="221db-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="221db-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="221db-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="221db-125">Library</span></span>                  | <span data-ttu-id="221db-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="221db-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="221db-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="221db-127">Related topics</span></span>

* [<span data-ttu-id="221db-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="221db-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




