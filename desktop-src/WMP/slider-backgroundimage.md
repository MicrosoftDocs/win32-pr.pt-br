---
title: SLIDER. backgroundImage
description: O atributo backgroundImage especifica ou recupera a imagem de plano de fundo do controle deslizante.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- Controle deslizante. backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1188756c16b13bef69dfd0bcd9a5b66560856f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769129"
---
# <a name="sliderbackgroundimage"></a><span data-ttu-id="cbbf4-104">SLIDER. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="cbbf4-104">SLIDER.backgroundImage</span></span>

<span data-ttu-id="cbbf4-105">O atributo **backgroundImage** especifica ou recupera a imagem de plano de fundo do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="cbbf4-105">The **backgroundImage** attribute specifies or retrieves the background image of the slider.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="cbbf4-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="cbbf4-106">Possible Values</span></span>

<span data-ttu-id="cbbf4-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="cbbf4-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbbf4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbbf4-108">Remarks</span></span>

<span data-ttu-id="cbbf4-109">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="cbbf4-109">This attribute is optional.</span></span> <span data-ttu-id="cbbf4-110">Ao usar imagens para construir um controle deslizante, o **backgroundImage** é usado para a imagem principal do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="cbbf4-110">When using images to construct a slider, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="cbbf4-111">O **thumbImage** representa o controle deslizante real e pode ser movido usando o mouse.</span><span class="sxs-lookup"><span data-stu-id="cbbf4-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="cbbf4-112">No controle deslizante **thumbImage** , há uma linha invisível em que a imagem de plano de fundo é exibida em um lado da linha e a imagem em primeiro plano é exibida no outro lado.</span><span class="sxs-lookup"><span data-stu-id="cbbf4-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="cbbf4-113">Quando o controle deslizante **thumbImage** for movido com o mouse, se o **Slide** estiver definido como true, a imagem em primeiro plano deslizará como se fosse puxada pelo controle deslizante para cobrir a imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="cbbf4-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="cbbf4-114">Se o **Slide** for definido como false, a imagem em primeiro plano não se moverá, mas será revelada no lugar, como se o controle deslizante estiver movendo a imagem de plano de fundo para a imagem em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="cbbf4-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="cbbf4-115">Se o **atributo de** subbarra for definido como true e a imagem de plano de fundo for menor do que o controle deslizante, a imagem será colocada na horizontal ou verticalmente, dependendo do atributo **Direction** .</span><span class="sxs-lookup"><span data-stu-id="cbbf4-115">If the **tiled** attribute is set to true and the background image is smaller than the slider control, the image will be tiled either horizontally or vertically depending on the **direction** attribute.</span></span> <span data-ttu-id="cbbf4-116">Se o atributo **borderize** for definido como um valor maior que zero, o número especificado será o número de pixels da esquerda e da direita ou da parte superior e inferior da imagem (novamente, dependendo do atributo **Direction** ) que será reservado para as bordas do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="cbbf4-116">If the **borderSize** attribute is set to a value greater than zero, the number specified will be the number of pixels from the left and right or top and bottom of the image (again, depending on the **direction** attribute) that will be reserved for the borders of the slider control.</span></span> <span data-ttu-id="cbbf4-117">Nesse caso, somente a parte central da imagem é usada para sublado o restante do controle.</span><span class="sxs-lookup"><span data-stu-id="cbbf4-117">In this case, only the central portion of the image is used for tiling the remainder of the control.</span></span>

<span data-ttu-id="cbbf4-118">Os formatos com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).</span><span class="sxs-lookup"><span data-stu-id="cbbf4-118">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbbf4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbbf4-119">Requirements</span></span>



| <span data-ttu-id="cbbf4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbbf4-120">Requirement</span></span> | <span data-ttu-id="cbbf4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cbbf4-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cbbf4-122">Versão</span><span class="sxs-lookup"><span data-stu-id="cbbf4-122">Version</span></span><br/> | <span data-ttu-id="cbbf4-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cbbf4-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cbbf4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbbf4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbbf4-125">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="cbbf4-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="cbbf4-126">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="cbbf4-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="cbbf4-127">**Controle deslizante. slide**</span><span class="sxs-lookup"><span data-stu-id="cbbf4-127">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="cbbf4-128">**SLIDER. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="cbbf4-128">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> </dl>

 

 





