---
title: SLIDER. foregroundImage
description: O atributo foregroundImage especifica ou recupera a imagem em primeiro plano do controle deslizante.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- Controle deslizante. foregroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a286d3b73a2647160a0bd23357703f4fcb88d267
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756098"
---
# <a name="sliderforegroundimage"></a><span data-ttu-id="0f154-104">SLIDER. foregroundImage</span><span class="sxs-lookup"><span data-stu-id="0f154-104">SLIDER.foregroundImage</span></span>

<span data-ttu-id="0f154-105">O atributo **foregroundImage** especifica ou recupera a imagem em primeiro plano do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="0f154-105">The **foregroundImage** attribute specifies or retrieves the foreground image of the slider.</span></span>

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a><span data-ttu-id="0f154-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0f154-106">Possible Values</span></span>

<span data-ttu-id="0f154-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="0f154-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f154-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f154-108">Remarks</span></span>

<span data-ttu-id="0f154-109">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="0f154-109">This attribute is optional.</span></span> <span data-ttu-id="0f154-110">Ao usar imagens para construir um controle deslizante, o **backgroundImage** é usado para a imagem principal do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="0f154-110">When using images to construct a slider control, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="0f154-111">O **thumbImage** representa o controle deslizante real e pode ser movido usando o mouse.</span><span class="sxs-lookup"><span data-stu-id="0f154-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="0f154-112">No controle deslizante **thumbImage** , há uma linha invisível em que a imagem de plano de fundo é exibida em um lado da linha e a imagem em primeiro plano é exibida no outro lado.</span><span class="sxs-lookup"><span data-stu-id="0f154-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="0f154-113">Quando o controle deslizante **thumbImage** for movido com o mouse, se o **Slide** estiver definido como true, a imagem em primeiro plano deslizará como se fosse puxada pelo controle deslizante para cobrir a imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="0f154-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="0f154-114">Se o **Slide** for definido como false, a imagem em primeiro plano não se moverá, mas será revelada no lugar, como se o controle deslizante estiver movendo a imagem de plano de fundo para a imagem em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="0f154-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="0f154-115">Se o **atributo de** subbarra for definido como true e a imagem em primeiro plano for menor do que a área de primeiro plano do controle deslizante, a imagem será colocada lado-a-horizontal ou verticalmente, dependendo do atributo **Direction** , para preencher o espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="0f154-115">If the **tiled** attribute is set to true and the foreground image is smaller than the foreground area of the slider control, the image will be tiled either horizontally or vertically, depending on the **direction** attribute, to fill the available space.</span></span>

<span data-ttu-id="0f154-116">Os formatos com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).</span><span class="sxs-lookup"><span data-stu-id="0f154-116">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f154-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f154-117">Requirements</span></span>



| <span data-ttu-id="0f154-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f154-118">Requirement</span></span> | <span data-ttu-id="0f154-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0f154-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0f154-120">Versão</span><span class="sxs-lookup"><span data-stu-id="0f154-120">Version</span></span><br/> | <span data-ttu-id="0f154-121">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0f154-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f154-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f154-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f154-123">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="0f154-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="0f154-124">**SLIDER. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="0f154-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="0f154-125">**Controle deslizante. slide**</span><span class="sxs-lookup"><span data-stu-id="0f154-125">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="0f154-126">**SLIDER. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="0f154-126">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="0f154-127">**Controle deslizante. valor**</span><span class="sxs-lookup"><span data-stu-id="0f154-127">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





