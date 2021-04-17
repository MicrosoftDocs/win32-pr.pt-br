---
title: Controle deslizante. slide
description: O atributo de slide especifica ou recupera um valor que indica se a imagem em primeiro plano desliza sobre a imagem de plano de fundo ou é revelada gradualmente em uma posição estática na imagem de plano de fundo.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- Controle deslizante. Deslize o Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749398"
---
# <a name="sliderslide"></a><span data-ttu-id="1c8a6-104">Controle deslizante. slide</span><span class="sxs-lookup"><span data-stu-id="1c8a6-104">SLIDER.slide</span></span>

<span data-ttu-id="1c8a6-105">O atributo de **Slide** especifica ou recupera um valor que indica se a imagem em primeiro plano desliza sobre a imagem de plano de fundo ou é revelada gradualmente em uma posição estática na imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-105">The **slide** attribute specifies or retrieves a value indicating whether the foreground image slides over the background image or is gradually revealed in a static position over the background image.</span></span>

``` syntax
        elementID.slide
```

## <a name="possible-values"></a><span data-ttu-id="1c8a6-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="1c8a6-106">Possible Values</span></span>

<span data-ttu-id="1c8a6-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="1c8a6-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1c8a6-108">Value</span></span> | <span data-ttu-id="1c8a6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c8a6-109">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="1c8a6-110">true</span><span class="sxs-lookup"><span data-stu-id="1c8a6-110">true</span></span>  | <span data-ttu-id="1c8a6-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-111">Default.</span></span> <span data-ttu-id="1c8a6-112">A imagem em primeiro plano desliza sobre a imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-112">The foreground image slides over the background image.</span></span>      |
| <span data-ttu-id="1c8a6-113">false</span><span class="sxs-lookup"><span data-stu-id="1c8a6-113">false</span></span> | <span data-ttu-id="1c8a6-114">A imagem em primeiro plano é revelada no lugar da imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-114">The foreground image is revealed in place over the background image.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1c8a6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c8a6-115">Remarks</span></span>

<span data-ttu-id="1c8a6-116">Quando o controle deslizante **thumbImage** for movido com o mouse, se o **Slide** estiver definido como true, a imagem em primeiro plano deslizará como se fosse puxada pelo controle deslizante para cobrir a imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-116">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="1c8a6-117">Se o **Slide** for definido como false, a imagem em primeiro plano não se moverá, mas será revelada no lugar, como se o controle deslizante estiver movendo a imagem de plano de fundo para a imagem em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-117">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c8a6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c8a6-118">Requirements</span></span>



| <span data-ttu-id="1c8a6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c8a6-119">Requirement</span></span> | <span data-ttu-id="1c8a6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1c8a6-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1c8a6-121">Versão</span><span class="sxs-lookup"><span data-stu-id="1c8a6-121">Version</span></span><br/> | <span data-ttu-id="1c8a6-122">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1c8a6-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c8a6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c8a6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c8a6-124">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="1c8a6-124">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="1c8a6-125">**SLIDER. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="1c8a6-125">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="1c8a6-126">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="1c8a6-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





