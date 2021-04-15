---
title: Controle deslizante. xadrez
description: O atributo de sublado especifica ou recupera um valor que indica se a imagem do controle deslizante será disposta ao lado.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- Controle deslizante. xadrez do Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753674"
---
# <a name="slidertiled"></a><span data-ttu-id="e8d30-104">Controle deslizante. xadrez</span><span class="sxs-lookup"><span data-stu-id="e8d30-104">SLIDER.tiled</span></span>

<span data-ttu-id="e8d30-105">O atributo de **sublado** especifica ou recupera um valor que indica se a imagem do controle deslizante será disposta ao lado.</span><span class="sxs-lookup"><span data-stu-id="e8d30-105">The **tiled** attribute specifies or retrieves a value indicating whether the slider image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="e8d30-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="e8d30-106">Possible Values</span></span>

<span data-ttu-id="e8d30-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e8d30-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="e8d30-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e8d30-108">Value</span></span> | <span data-ttu-id="e8d30-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8d30-109">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d30-110">true</span><span class="sxs-lookup"><span data-stu-id="e8d30-110">true</span></span>  | <span data-ttu-id="e8d30-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="e8d30-111">Default.</span></span> <span data-ttu-id="e8d30-112">O bitmap de imagem será repetido até ocupar a região inteira do controle.</span><span class="sxs-lookup"><span data-stu-id="e8d30-112">The image bitmap will be repeated until it fills the entire region of the control.</span></span> |
| <span data-ttu-id="e8d30-113">false</span><span class="sxs-lookup"><span data-stu-id="e8d30-113">false</span></span> | <span data-ttu-id="e8d30-114">A imagem não será enlado.</span><span class="sxs-lookup"><span data-stu-id="e8d30-114">The image will not be tiled.</span></span>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="e8d30-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8d30-115">Remarks</span></span>

<span data-ttu-id="e8d30-116">Esse atributo se aplica somente se você estiver usando imagens de primeiro e segundo plano para definir um controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="e8d30-116">This attribute applies only if you are using foreground and background images to define a slider control.</span></span> <span data-ttu-id="e8d30-117">Se as imagens forem menores do que a área definida do controle deslizante, e o atributo de **ladrilho** for definido como true, as imagens serão repetidas até que preencham toda a duração do controle.</span><span class="sxs-lookup"><span data-stu-id="e8d30-117">If the images are smaller than the defined area of the slider, and the **tiled** attribute is set to true, the images will be repeated until they fill the entire length of the control.</span></span>

<span data-ttu-id="e8d30-118">Talvez você queira usar esse atributo em conjunto com o atributo **borderize** .</span><span class="sxs-lookup"><span data-stu-id="e8d30-118">You may wish to use this attribute in conjunction with the **borderSize** attribute.</span></span> <span data-ttu-id="e8d30-119">O atributo **borderize** permite que você defina uma borda que não é repetida durante a divisão.</span><span class="sxs-lookup"><span data-stu-id="e8d30-119">The **borderSize** attribute allows you to define a border that is not repeated during tiling.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8d30-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8d30-120">Requirements</span></span>



| <span data-ttu-id="e8d30-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8d30-121">Requirement</span></span> | <span data-ttu-id="e8d30-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e8d30-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e8d30-123">Versão</span><span class="sxs-lookup"><span data-stu-id="e8d30-123">Version</span></span><br/> | <span data-ttu-id="e8d30-124">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e8d30-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8d30-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8d30-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8d30-126">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="e8d30-126">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="e8d30-127">**SLIDER. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="e8d30-127">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="e8d30-128">**Controle deslizante. Borderize**</span><span class="sxs-lookup"><span data-stu-id="e8d30-128">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="e8d30-129">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="e8d30-129">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





