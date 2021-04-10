---
title: Elemento subview
description: Elemento subview
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Capas do Windows Media Player, elemento subview
- elemento skins, subview
- Elemento subview
- referência para capas, elemento subview
- elementos, subexibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292654"
---
# <a name="subview-element"></a><span data-ttu-id="af3d2-108">Elemento subview</span><span class="sxs-lookup"><span data-stu-id="af3d2-108">SUBVIEW Element</span></span>

<span data-ttu-id="af3d2-109">O elemento **subview** fornece uma maneira de manipular uma parte de uma capa, por exemplo, para fornecer um painel de controle que pode ser ocultado quando não está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="af3d2-109">The **SUBVIEW** element provides a way to manipulate a portion of a skin, for example, to provide a control panel that can be hidden when it is not being used.</span></span> <span data-ttu-id="af3d2-110">Os elementos de **subexibição** são sempre filhos dos elementos de **exibição** pai e podem conter outro elemento de capa, exceto para **exibição**, **tema** e outros elementos de **subexibição** .</span><span class="sxs-lookup"><span data-stu-id="af3d2-110">**SUBVIEW** elements are always children of parent **VIEW** elements, and can contain other skin element except for **VIEW**, **THEME**, and other **SUBVIEW** elements.</span></span>

<span data-ttu-id="af3d2-111">O elemento **subview** dá suporte aos seguintes atributos, que são definidos no elemento **View** .</span><span class="sxs-lookup"><span data-stu-id="af3d2-111">The **SUBVIEW** element supports the following attributes, which are defined under the **VIEW** element.</span></span>



| <span data-ttu-id="af3d2-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="af3d2-112">Attribute</span></span>                                                       | <span data-ttu-id="af3d2-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="af3d2-113">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af3d2-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="af3d2-114">backgroundColor</span></span>](view-backgroundcolor.md)                     | <span data-ttu-id="af3d2-115">Especifica ou recupera a cor da tela de fundo do controle de **subexibição** .</span><span class="sxs-lookup"><span data-stu-id="af3d2-115">Specifies or retrieves the background color of the **SUBVIEW** control.</span></span> <span data-ttu-id="af3d2-116">O valor padrão é "None".</span><span class="sxs-lookup"><span data-stu-id="af3d2-116">The default value is "none".</span></span>        |
| [<span data-ttu-id="af3d2-117">backgroundImage</span><span class="sxs-lookup"><span data-stu-id="af3d2-117">backgroundImage</span></span>](view-backgroundimage.md)                     | <span data-ttu-id="af3d2-118">Especifica ou recupera a imagem de plano de fundo do controle de **subexibição** .</span><span class="sxs-lookup"><span data-stu-id="af3d2-118">Specifies or retrieves the background image of the **SUBVIEW** control.</span></span>                                     |
| [<span data-ttu-id="af3d2-119">backgroundImageHueShift</span><span class="sxs-lookup"><span data-stu-id="af3d2-119">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="af3d2-120">Especifica ou recupera a quantidade pela qual o matiz da imagem de plano de fundo é deslocado.</span><span class="sxs-lookup"><span data-stu-id="af3d2-120">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                      |
| [<span data-ttu-id="af3d2-121">backgroundImageSaturation</span><span class="sxs-lookup"><span data-stu-id="af3d2-121">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="af3d2-122">Especifica ou recupera o valor de saturação da imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="af3d2-122">Specifies or retrieves the saturation value of the background image.</span></span>                                        |
| [<span data-ttu-id="af3d2-123">backgroundTiled</span><span class="sxs-lookup"><span data-stu-id="af3d2-123">backgroundTiled</span></span>](view-backgroundtiled.md)                     | <span data-ttu-id="af3d2-124">Especifica ou recupera um valor que indica se a imagem de plano de fundo do controle de **subexibição** está lado a lado.</span><span class="sxs-lookup"><span data-stu-id="af3d2-124">Specifies or retrieves a value indicating whether the background image of the **SUBVIEW** control is tiled.</span></span> |
| [<span data-ttu-id="af3d2-125">resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="af3d2-125">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="af3d2-126">Especifica ou recupera um valor que indica se a imagem de plano de fundo pode ser redimensionada.</span><span class="sxs-lookup"><span data-stu-id="af3d2-126">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                      |
| [<span data-ttu-id="af3d2-127">transparencyColor</span><span class="sxs-lookup"><span data-stu-id="af3d2-127">transparencyColor</span></span>](view-transparencycolor.md)                 | <span data-ttu-id="af3d2-128">Especifica ou recupera a cor de transparência da imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="af3d2-128">Specifies or retrieves the transparency color of the background image.</span></span>                                      |



 

<span data-ttu-id="af3d2-129">O elemento **subview** oferece suporte aos atributos de ambiente, exceto quando indicado.</span><span class="sxs-lookup"><span data-stu-id="af3d2-129">The **SUBVIEW** element supports the ambient attributes, except where noted.</span></span> <span data-ttu-id="af3d2-130">Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="af3d2-130">For more information, see [Ambient Attributes](ambient-attributes.md).</span></span>

<span data-ttu-id="af3d2-131">O elemento **subview** pode implementar os seguintes manipuladores de eventos de ambiente: [onendmove](onendmove.md) e [OnResize](onresize.md).</span><span class="sxs-lookup"><span data-stu-id="af3d2-131">The **SUBVIEW** element can implement the following ambient event handlers: [onendmove](onendmove.md) and [onresize](onresize.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af3d2-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af3d2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af3d2-133">**Referência de programação de capa**</span><span class="sxs-lookup"><span data-stu-id="af3d2-133">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="af3d2-134">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="af3d2-134">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 




