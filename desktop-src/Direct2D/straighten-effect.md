---
title: Efeito de retificação
description: Gira e, opcionalmente, dimensiona uma imagem.
ms.assetid: aa37cdf1-bbb6-db4e-45a7-67c7cc16b7b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8e521ca4c0c452301c0f8031c94ba8c22efe80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104555536"
---
# <a name="straighten-effect"></a><span data-ttu-id="d29a4-103">Efeito de retificação</span><span class="sxs-lookup"><span data-stu-id="d29a4-103">Straighten effect</span></span>

<span data-ttu-id="d29a4-104">Gira e, opcionalmente, dimensiona uma imagem.</span><span class="sxs-lookup"><span data-stu-id="d29a4-104">Rotates and optionally scales an image.</span></span>

<span data-ttu-id="d29a4-105">O CLSID para esse efeito é CLSID \_ D2D1Straighten.</span><span class="sxs-lookup"><span data-stu-id="d29a4-105">The CLSID for this effect is CLSID\_D2D1Straighten.</span></span>

-   [<span data-ttu-id="d29a4-106">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="d29a4-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="d29a4-107">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="d29a4-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="d29a4-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="d29a4-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="d29a4-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="d29a4-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d29a4-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d29a4-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="d29a4-111">Imagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="d29a4-111">Example image</span></span>

![exemplo de saída de efeito](images/straighten-effect.png)

## <a name="sample-code"></a><span data-ttu-id="d29a4-113">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="d29a4-113">Sample code</span></span>


```cpp
ComPtr<ID2D1Effect> straightenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Straighten, &straightenEffect);
 
straightenEffect->SetInput(0, bitmap);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_ANGLE, 12.0f);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, true);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_SCALE_MODE, D2D1_STRAIGHTEN_SCALE_MODE_LINEAR);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(straightenEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="d29a4-114">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="d29a4-114">Effect properties</span></span>

<span data-ttu-id="d29a4-115">As propriedades para o efeito de retificação são definidas pela enumeração [**d2d1 \_ retifica \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) .</span><span class="sxs-lookup"><span data-stu-id="d29a4-115">The properties for the straighten effect are defined by the [**D2D1\_STRAIGHTEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d29a4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d29a4-116">Requirements</span></span>



| <span data-ttu-id="d29a4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d29a4-117">Requirement</span></span> | <span data-ttu-id="d29a4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d29a4-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="d29a4-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d29a4-119">Minimum supported client</span></span> | <span data-ttu-id="d29a4-120">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d29a4-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d29a4-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d29a4-121">Minimum supported server</span></span> | <span data-ttu-id="d29a4-122">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d29a4-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d29a4-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d29a4-123">Header</span></span>                   | <span data-ttu-id="d29a4-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="d29a4-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="d29a4-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d29a4-125">Library</span></span>                  | <span data-ttu-id="d29a4-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="d29a4-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="d29a4-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d29a4-127">Related topics</span></span>

* [<span data-ttu-id="d29a4-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="d29a4-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

