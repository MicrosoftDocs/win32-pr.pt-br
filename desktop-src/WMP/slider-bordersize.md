---
title: Controle deslizante. Borderize
description: O atributo Borderize especifica ou recupera a largura da borda em pixels.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- Controle deslizante. Bordasize o Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756321"
---
# <a name="sliderbordersize"></a><span data-ttu-id="96cba-104">Controle deslizante. Borderize</span><span class="sxs-lookup"><span data-stu-id="96cba-104">SLIDER.borderSize</span></span>

<span data-ttu-id="96cba-105">O atributo **borderize** especifica ou recupera a largura da borda em pixels.</span><span class="sxs-lookup"><span data-stu-id="96cba-105">The **borderSize** attribute specifies or retrieves the border width in pixels.</span></span>

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a><span data-ttu-id="96cba-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="96cba-106">Possible Values</span></span>

<span data-ttu-id="96cba-107">Esse atributo é um **número** de leitura/gravação (**longo**) que representa a largura da borda em pixels.</span><span class="sxs-lookup"><span data-stu-id="96cba-107">This attribute is a read/write **Number** (**long**) representing the border width in pixels.</span></span> <span data-ttu-id="96cba-108">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="96cba-108">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="96cba-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="96cba-109">Remarks</span></span>

<span data-ttu-id="96cba-110">Esse atributo define um deslocamento do início e do fim do controle deslizante que é, da esquerda e direita, se o atributo **Direction** estiver definido como "horizontal", e da parte superior e inferior se for definido como "vertical".</span><span class="sxs-lookup"><span data-stu-id="96cba-110">This attribute defines an offset from the beginning and end of the slider control that is, from the left and right if the **direction** attribute is set to "horizontal", and from the top and bottom if it is set to "vertical".</span></span> <span data-ttu-id="96cba-111">Essas posições de deslocamento determinam as posições mínima e máxima do controle deslizante, além dos quais a cor ou a imagem de primeiro plano não será aplicada.</span><span class="sxs-lookup"><span data-stu-id="96cba-111">These offset positions dictate the minimum and maximum positions of the slider thumb, beyond which the foreground color or image will not be applied.</span></span>

<span data-ttu-id="96cba-112">Se uma imagem de plano de fundo for usada **com o atributo** de sublinhado definido como true, o deslocamento será aplicado à imagem, ditando a quantidade da imagem (da esquerda e da direita ou da parte superior e inferior) a ser usada nas bordas inicial e final do controle deslizante, com a parte central da imagem que está sendo colocada ao lado do restante.</span><span class="sxs-lookup"><span data-stu-id="96cba-112">If a background image is used with the **tiled** attribute set to true, the offset is applied to the image, dictating the amount of the image (either from the left and right or from the top and bottom) to be used for the beginning and end borders of the slider control, with the central portion of the image being tiled throughout the remainder.</span></span> <span data-ttu-id="96cba-113">Dessa forma, uma pequena imagem de fundo pode ser usada para cobrir todo o comprimento de um controle deslizante maior.</span><span class="sxs-lookup"><span data-stu-id="96cba-113">In this way, a small background image can be used to cover the full length of a larger slider control.</span></span>

## <a name="requirements"></a><span data-ttu-id="96cba-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96cba-114">Requirements</span></span>



| <span data-ttu-id="96cba-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="96cba-115">Requirement</span></span> | <span data-ttu-id="96cba-116">Valor</span><span class="sxs-lookup"><span data-stu-id="96cba-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="96cba-117">Versão</span><span class="sxs-lookup"><span data-stu-id="96cba-117">Version</span></span><br/> | <span data-ttu-id="96cba-118">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="96cba-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96cba-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="96cba-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96cba-120">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="96cba-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="96cba-121">**SLIDER. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="96cba-121">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="96cba-122">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="96cba-122">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="96cba-123">**SLIDER. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="96cba-123">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="96cba-124">**Controle deslizante. xadrez**</span><span class="sxs-lookup"><span data-stu-id="96cba-124">**SLIDER.tiled**</span></span>](slider-tiled.md)
</dt> </dl>

 

 





