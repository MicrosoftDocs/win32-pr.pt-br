---
title: SLIDER. thumbImage
description: O atributo thumbImage especifica ou recupera a imagem que será usada para representar a posição atual do controle deslizante.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- Controle deslizante. thumbImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b798dfbae24fe2cef3669d2fb372966e47254026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761185"
---
# <a name="sliderthumbimage"></a><span data-ttu-id="5802d-104">SLIDER. thumbImage</span><span class="sxs-lookup"><span data-stu-id="5802d-104">SLIDER.thumbImage</span></span>

<span data-ttu-id="5802d-105">O atributo **thumbImage** especifica ou recupera a imagem que será usada para representar a posição atual do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="5802d-105">The **thumbImage** attribute specifies or retrieves the image that will be used to represent the current position of the slider.</span></span>

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a><span data-ttu-id="5802d-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5802d-106">Possible Values</span></span>

<span data-ttu-id="5802d-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="5802d-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="5802d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="5802d-108">Remarks</span></span>

<span data-ttu-id="5802d-109">O **thumbImage** especifica a imagem que será usada para representar a posição atual, bem como indicar que o usuário pode executar uma ação com o controle.</span><span class="sxs-lookup"><span data-stu-id="5802d-109">The **thumbImage** specifies the image that will be used to represent current position, as well as indicate that the user can take action with the control.</span></span> <span data-ttu-id="5802d-110">Se nenhuma imagem Thumb for especificada, o controle deslizante será não interativo.</span><span class="sxs-lookup"><span data-stu-id="5802d-110">If no thumb image is specified, the slider is non-interactive.</span></span>

<span data-ttu-id="5802d-111">A imagem em miniatura é centralizada na dimensão estreita do controle Slider.</span><span class="sxs-lookup"><span data-stu-id="5802d-111">The thumb image is centered in the narrow dimension of the slider control.</span></span> <span data-ttu-id="5802d-112">Se a imagem em miniatura for mais estreita do que o controle, a imagem aparecerá no meio do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="5802d-112">If the thumb image is narrower than the control, the image appears in the middle of the background.</span></span> <span data-ttu-id="5802d-113">Se a imagem em miniatura for maior que o controle, as extremidades da imagem serão cortadas.</span><span class="sxs-lookup"><span data-stu-id="5802d-113">If the thumb image is larger than the control, the ends of the image are cut off.</span></span>

<span data-ttu-id="5802d-114">A posição do controle deslizante é especificada pelo centro da imagem do polegar.</span><span class="sxs-lookup"><span data-stu-id="5802d-114">The position of the slider is specified by the center of the thumb image.</span></span> <span data-ttu-id="5802d-115">Se **Bordere** for zero, apenas metade da imagem Thumb ficará visível nas posições do controle deslizante inicial e final.</span><span class="sxs-lookup"><span data-stu-id="5802d-115">If **borderSize** is zero, only half the thumb image will be visible at the beginning and end slider positions.</span></span> <span data-ttu-id="5802d-116">Para evitar isso, defina **borderize** como um valor maior ou igual à metade da largura da imagem Thumb (ou metade da altura se a **direção** for definida como "vertical").</span><span class="sxs-lookup"><span data-stu-id="5802d-116">To prevent this, set **borderSize** to a value greater than or equal to half the width of the thumb image (or half the height if **direction** is set to "vertical").</span></span>

<span data-ttu-id="5802d-117">Os formatos com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).</span><span class="sxs-lookup"><span data-stu-id="5802d-117">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

<span data-ttu-id="5802d-118">Consulte o **CUSTOMSLIDER**. atributo [positionImage](customslider-positionimage.md) para um exemplo que ilustra como os atributos do elemento **Slider** são usados.</span><span class="sxs-lookup"><span data-stu-id="5802d-118">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5802d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5802d-119">Requirements</span></span>



| <span data-ttu-id="5802d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5802d-120">Requirement</span></span> | <span data-ttu-id="5802d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5802d-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5802d-122">Versão</span><span class="sxs-lookup"><span data-stu-id="5802d-122">Version</span></span><br/> | <span data-ttu-id="5802d-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5802d-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5802d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5802d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5802d-125">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="5802d-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="5802d-126">**Controle deslizante. Borderize**</span><span class="sxs-lookup"><span data-stu-id="5802d-126">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="5802d-127">**Controle deslizante. direção**</span><span class="sxs-lookup"><span data-stu-id="5802d-127">**SLIDER.direction**</span></span>](slider-direction.md)
</dt> </dl>

 

 





