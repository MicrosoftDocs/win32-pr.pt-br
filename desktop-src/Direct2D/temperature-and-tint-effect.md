---
title: Efeito de temperatura e tonalidade
description: Efeito de temperatura e tonalidade
ms.assetid: 8df72105-26ea-2dea-a4de-ef06902b7e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c3628e1fdcb1c72a84a9e08736e4215d55514
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096634"
---
# <a name="temperature-and-tint-effect"></a><span data-ttu-id="af5e7-103">Efeito de temperatura e tonalidade</span><span class="sxs-lookup"><span data-stu-id="af5e7-103">Temperature and tint effect</span></span>

<span data-ttu-id="af5e7-104">O CLSID para esse efeito é CLSID \_ D2D1TemperatureTint.</span><span class="sxs-lookup"><span data-stu-id="af5e7-104">The CLSID for this effect is CLSID\_D2D1TemperatureTint.</span></span>

## <a name="sample-code"></a><span data-ttu-id="af5e7-105">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="af5e7-105">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> temperatureTintEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TemperatureTint, &temperatureTintEffect);
 
temperatureTintEffect->SetInput(0, bitmap);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, 0.5f);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TINT, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(temperatureTintEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="af5e7-106">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="af5e7-106">Effect properties</span></span>

<span data-ttu-id="af5e7-107">As propriedades para o efeito de temperatura e tonalidade são definidas pela enumeração de [**\_ \_ prop d2d1 TEMPERATUREANDTINT**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) .</span><span class="sxs-lookup"><span data-stu-id="af5e7-107">The properties for the temperature and tint effect are defined by the [**D2D1\_TEMPERATUREANDTINT\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="af5e7-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af5e7-108">Requirements</span></span>



| <span data-ttu-id="af5e7-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="af5e7-109">Requirement</span></span> | <span data-ttu-id="af5e7-110">Valor</span><span class="sxs-lookup"><span data-stu-id="af5e7-110">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="af5e7-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af5e7-111">Minimum supported client</span></span> | <span data-ttu-id="af5e7-112">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="af5e7-112">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="af5e7-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af5e7-113">Minimum supported server</span></span> | <span data-ttu-id="af5e7-114">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="af5e7-114">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="af5e7-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af5e7-115">Header</span></span>                   | <span data-ttu-id="af5e7-116">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="af5e7-116">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="af5e7-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af5e7-117">Library</span></span>                  | <span data-ttu-id="af5e7-118">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="af5e7-118">d2d1.lib, dxguid.lib</span></span>                              |



 

## <a name="related-topics"></a><span data-ttu-id="af5e7-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af5e7-119">Related topics</span></span>

* [<span data-ttu-id="af5e7-120">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="af5e7-120">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
