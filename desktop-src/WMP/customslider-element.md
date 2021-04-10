---
title: Elemento CUSTOMSLIDER
description: Elemento CUSTOMSLIDER
ms.assetid: 9cba9bdd-ea5b-4a4a-a61e-e6aff29fc3e0
keywords:
- Capas do Windows Media Player, elemento CUSTOMSLIDER
- Skins, elemento CUSTOMSLIDER
- Elemento CUSTOMSLIDER
- referência para capas, elemento CUSTOMSLIDER
- elementos, CUSTOMSLIDER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f49fc6260df295e3266ae9ddf7b5b3eceee43d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292408"
---
# <a name="customslider-element"></a><span data-ttu-id="d27ac-108">Elemento CUSTOMSLIDER</span><span class="sxs-lookup"><span data-stu-id="d27ac-108">CUSTOMSLIDER Element</span></span>

<span data-ttu-id="d27ac-109">O elemento **CUSTOMSLIDER** fornece uma maneira de criar e manipular um controle deslizante de qualquer forma, como um botão circular.</span><span class="sxs-lookup"><span data-stu-id="d27ac-109">The **CUSTOMSLIDER** element provides a way to create and manipulate a slider control of any shape, such as a circular knob.</span></span> <span data-ttu-id="d27ac-110">As tabelas a seguir listam os atributos e manipuladores de eventos com suporte neste elemento.</span><span class="sxs-lookup"><span data-stu-id="d27ac-110">The following tables list the attributes and event handlers supported by this element.</span></span>

<span data-ttu-id="d27ac-111">O elemento **CUSTOMSLIDER** dá suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="d27ac-111">The **CUSTOMSLIDER** element supports the following attributes.</span></span>



| <span data-ttu-id="d27ac-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="d27ac-112">Attribute</span></span>                                               | <span data-ttu-id="d27ac-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="d27ac-113">Description</span></span>                                                                                                                 |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d27ac-114">cursor</span><span class="sxs-lookup"><span data-stu-id="d27ac-114">cursor</span></span>](customslider-cursor.md)                       | <span data-ttu-id="d27ac-115">Especifica ou recupera o valor do cursor de controle Slider que aparece quando o mouse está sobre o controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="d27ac-115">Specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>               |
| [<span data-ttu-id="d27ac-116">disabledImage</span><span class="sxs-lookup"><span data-stu-id="d27ac-116">disabledImage</span></span>](customslider-disabledimage.md)         | <span data-ttu-id="d27ac-117">Especifica ou recupera a imagem do controle deslizante usado quando o controle deslizante está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d27ac-117">Specifies or retrieves the image of the slider used when the slider is disabled.</span></span>                                            |
| [<span data-ttu-id="d27ac-118">downImage</span><span class="sxs-lookup"><span data-stu-id="d27ac-118">downImage</span></span>](customslider-downimage.md)                 | <span data-ttu-id="d27ac-119">Especifica ou recupera a imagem de estado inferior do controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="d27ac-119">Specifies or retrieves the down state image of the custom slider.</span></span>                                                           |
| [<span data-ttu-id="d27ac-120">hoverImage</span><span class="sxs-lookup"><span data-stu-id="d27ac-120">hoverImage</span></span>](customslider-hoverimage.md)               | <span data-ttu-id="d27ac-121">Especifica ou recupera a imagem exibida quando o mouse está sobre o controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="d27ac-121">Specifies or retrieves the image that displays when the mouse is over the custom slider.</span></span>                                    |
| [<span data-ttu-id="d27ac-122">imagem</span><span class="sxs-lookup"><span data-stu-id="d27ac-122">image</span></span>](customslider-image.md)                         | <span data-ttu-id="d27ac-123">Especifica ou recupera o nome do arquivo que contém as imagens correspondentes aos vários Estados do controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="d27ac-123">Specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span> |
| [<span data-ttu-id="d27ac-124">max</span><span class="sxs-lookup"><span data-stu-id="d27ac-124">max</span></span>](customslider-max.md)                             | <span data-ttu-id="d27ac-125">Especifica ou recupera o valor máximo do intervalo definido pelo controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="d27ac-125">Specifies or retrieves the maximum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="d27ac-126">min</span><span class="sxs-lookup"><span data-stu-id="d27ac-126">min</span></span>](customslider-min.md)                             | <span data-ttu-id="d27ac-127">Especifica ou recupera o valor mínimo do intervalo definido pelo controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="d27ac-127">Specifies or retrieves the minimum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="d27ac-128">positionImage</span><span class="sxs-lookup"><span data-stu-id="d27ac-128">positionImage</span></span>](customslider-positionimage.md)         | <span data-ttu-id="d27ac-129">Especifica ou recupera o mapa de imagem usado para determinar qual imagem de posição do arquivo de **imagem** a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="d27ac-129">Specifies or retrieves the image map used to determine which position image from the **image** file to display.</span></span>             |
| [<span data-ttu-id="d27ac-130">Dessa</span><span class="sxs-lookup"><span data-stu-id="d27ac-130">toolTip</span></span>](customslider-tooltip.md)                     | <span data-ttu-id="d27ac-131">Especifica ou recupera o texto da dica de ferramenta para o controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="d27ac-131">Specifies or retrieves the ToolTip text for the slider.</span></span>                                                                     |
| [<span data-ttu-id="d27ac-132">transparencyColor</span><span class="sxs-lookup"><span data-stu-id="d27ac-132">transparencyColor</span></span>](customslider-transparencycolor.md) | <span data-ttu-id="d27ac-133">Especifica ou recupera a cor de transparência das imagens do controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="d27ac-133">Specifies or retrieves the transparency color of the custom slider images.</span></span>                                                  |
| [<span data-ttu-id="d27ac-134">value</span><span class="sxs-lookup"><span data-stu-id="d27ac-134">value</span></span>](customslider-value.md)                         | <span data-ttu-id="d27ac-135">Especifica ou recupera a posição atual do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="d27ac-135">Specifies or retrieves the current position of the slider.</span></span>                                                                  |



 

<span data-ttu-id="d27ac-136">O elemento **CUSTOMSLIDER** pode implementar os manipuladores de eventos a seguir.</span><span class="sxs-lookup"><span data-stu-id="d27ac-136">The **CUSTOMSLIDER** element can implement the following event handlers.</span></span>



| <span data-ttu-id="d27ac-137">Manipulador de eventos</span><span class="sxs-lookup"><span data-stu-id="d27ac-137">Event handler</span></span>                                         | <span data-ttu-id="d27ac-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="d27ac-138">Description</span></span>                                                                                                          |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d27ac-139">onDragBegin</span><span class="sxs-lookup"><span data-stu-id="d27ac-139">onDragBegin</span></span>](customslider-ondragbegin.md)           | <span data-ttu-id="d27ac-140">Manipula um evento que ocorre quando o usuário clica e mantém o botão esquerdo do mouse pressionado e começa a arrastar o mouse.</span><span class="sxs-lookup"><span data-stu-id="d27ac-140">Handles an event that occurs when the user clicks and holds the left mouse button down and begins to drag the mouse.</span></span> |
| [<span data-ttu-id="d27ac-141">onDragEnd</span><span class="sxs-lookup"><span data-stu-id="d27ac-141">onDragEnd</span></span>](customslider-ondragend.md)               | <span data-ttu-id="d27ac-142">Manipula um evento que ocorre quando o botão esquerdo do mouse é liberado após uma operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="d27ac-142">Handles an event that occurs when the left mouse button is released after a dragging operation.</span></span>                      |
| [<span data-ttu-id="d27ac-143">onPositionChange</span><span class="sxs-lookup"><span data-stu-id="d27ac-143">onPositionChange</span></span>](customslider-onpositionchange.md) | <span data-ttu-id="d27ac-144">Manipula um evento que ocorre quando a posição do controle deslizante é alterada como resultado do clique ou arraste do usuário.</span><span class="sxs-lookup"><span data-stu-id="d27ac-144">Handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>   |



 

<span data-ttu-id="d27ac-145">O elemento **CUSTOMSLIDER** dá suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente.</span><span class="sxs-lookup"><span data-stu-id="d27ac-145">The **CUSTOMSLIDER** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="d27ac-146">Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md) e [manipuladores de eventos de ambiente](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="d27ac-146">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d27ac-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d27ac-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d27ac-148">**Referência de programação de capa**</span><span class="sxs-lookup"><span data-stu-id="d27ac-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




