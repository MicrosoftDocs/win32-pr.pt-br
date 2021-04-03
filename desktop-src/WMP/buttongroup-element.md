---
title: Elemento de botão
description: Elemento de botão
ms.assetid: 4756c016-3347-4129-be5e-e822270a24de
keywords:
- Capas do Windows Media Player, elemento de botão
- capas, elemento de botão
- Elemento de botão
- referência de capas, elemento de botão
- elementos, um botão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4de489e779b5e20214778b56fd8d19c7627e444
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084117"
---
# <a name="buttongroup-element"></a><span data-ttu-id="7d3b4-108">Elemento de botão</span><span class="sxs-lookup"><span data-stu-id="7d3b4-108">BUTTONGROUP Element</span></span>

<span data-ttu-id="7d3b4-109">O elemento **Button** fornece uma maneira de agrupar vários botões em uma capa.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-109">The **BUTTONGROUP** element provides a way to group several buttons within a skin.</span></span> <span data-ttu-id="7d3b4-110">Esses botões podem ser especificados usando elementos **buttonelement** como filhos do elemento **Button** .</span><span class="sxs-lookup"><span data-stu-id="7d3b4-110">These buttons can be specified by using **BUTTONELEMENT** elements as children of the **BUTTONGROUP** element.</span></span>

<span data-ttu-id="7d3b4-111">O elemento **Button** dá suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-111">The **BUTTONGROUP** element supports the following attributes.</span></span>



| <span data-ttu-id="7d3b4-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="7d3b4-112">Attribute</span></span>                                              | <span data-ttu-id="7d3b4-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d3b4-113">Description</span></span>                                                                                                                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d3b4-114">buttonCount</span><span class="sxs-lookup"><span data-stu-id="7d3b4-114">buttonCount</span></span>](buttongroup-buttoncount.md)             | <span data-ttu-id="7d3b4-115">Recupera o número de botões no **botão**.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-115">Retrieves the number of buttons in the **BUTTONGROUP**.</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="7d3b4-116">cursor</span><span class="sxs-lookup"><span data-stu-id="7d3b4-116">cursor</span></span>](buttongroup-cursor.md)                       | <span data-ttu-id="7d3b4-117">Especifica ou recupera o tipo de cursor que aparece quando o mouse está sobre um botão no botão **.**</span><span class="sxs-lookup"><span data-stu-id="7d3b4-117">Specifies or retrieves the type of cursor that appears when the mouse is over a button in the **BUTTONGROUP**.</span></span>                                                                                                                  |
| [<span data-ttu-id="7d3b4-118">disabledImage</span><span class="sxs-lookup"><span data-stu-id="7d3b4-118">disabledImage</span></span>](buttongroup-disabledimage.md)         | <span data-ttu-id="7d3b4-119">Especifica ou recupera o nome da imagem que representa o estado desabilitado dos botões no **botão**.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-119">Specifies or retrieves the name of the image representing the disabled state of the buttons in the **BUTTONGROUP**.</span></span>                                                                                                             |
| [<span data-ttu-id="7d3b4-120">downImage</span><span class="sxs-lookup"><span data-stu-id="7d3b4-120">downImage</span></span>](buttongroup-downimage.md)                 | <span data-ttu-id="7d3b4-121">Especifica ou recupera o nome da imagem que representa o estado inferior do **botão**.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-121">Specifies or retrieves the name of the image representing the down state of the **BUTTONGROUP**.</span></span>                                                                                                                                |
| [<span data-ttu-id="7d3b4-122">hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="7d3b4-122">hoverDownImage</span></span>](buttongroup-hoverdownimage.md)       | <span data-ttu-id="7d3b4-123">Especifica ou recupera o nome da imagem que representa o estado de focalização de um botão no **botão**.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-123">Specifies or retrieves the name of the image representing the hover-down state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="7d3b4-124">O estado de focalização ocorre quando o botão está no estado inativo e o usuário passa o mouse sobre ele.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-124">The hover-down state occurs when the button is in the down state and the user hovers over it with the mouse.</span></span> |
| [<span data-ttu-id="7d3b4-125">hoverImage</span><span class="sxs-lookup"><span data-stu-id="7d3b4-125">hoverImage</span></span>](buttongroup-hoverimage.md)               | <span data-ttu-id="7d3b4-126">Especifica ou recupera o nome da imagem que representa o estado de foco de um botão no **botão**.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-126">Specifies or retrieves the name of the image representing the hover state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="7d3b4-127">O estado de foco ocorre quando o botão está no estado ativo e o usuário passa o mouse sobre ele.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-127">The hover state occurs when the button is in the up state and the user hovers over it with the mouse.</span></span>             |
| [<span data-ttu-id="7d3b4-128">hueShift</span><span class="sxs-lookup"><span data-stu-id="7d3b4-128">hueShift</span></span>](buttongroup-hueshift.md)                   | <span data-ttu-id="7d3b4-129">Especifica ou recupera a quantidade pela qual o matiz das imagens de um **botão** é deslocado.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-129">Specifies or retrieves the amount by which the hue of the **BUTTONGROUP** images is shifted.</span></span>                                                                                                                                    |
| [<span data-ttu-id="7d3b4-130">imagem</span><span class="sxs-lookup"><span data-stu-id="7d3b4-130">image</span></span>](buttongroup-image.md)                         | <span data-ttu-id="7d3b4-131">Especifica ou recupera o nome da imagem que representa os botões de um **botão**.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-131">Specifies or retrieves the name of the image representing the buttons of a **BUTTONGROUP**.</span></span>                                                                                                                                     |
| [<span data-ttu-id="7d3b4-132">mappingImage</span><span class="sxs-lookup"><span data-stu-id="7d3b4-132">mappingImage</span></span>](buttongroup-mappingimage.md)           | <span data-ttu-id="7d3b4-133">Especifica ou recupera o nome da imagem que representa o mapa de botão do **botão**.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-133">Specifies or retrieves the name of the image representing the button map of the **BUTTONGROUP**.</span></span>                                                                                                                                |
| [<span data-ttu-id="7d3b4-134">radio</span><span class="sxs-lookup"><span data-stu-id="7d3b4-134">radio</span></span>](buttongroup-radio.md)                         | <span data-ttu-id="7d3b4-135">Especifica ou recupera um valor que indica se o **botão** é composto por botões de opção.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-135">Specifies or retrieves a value indicating whether the **BUTTONGROUP** is composed of radio buttons.</span></span>                                                                                                                             |
| [<span data-ttu-id="7d3b4-136">saturação</span><span class="sxs-lookup"><span data-stu-id="7d3b4-136">saturation</span></span>](buttongroup-saturation.md)               | <span data-ttu-id="7d3b4-137">Especifica ou recupera o valor de saturação das imagens de um **botão** .</span><span class="sxs-lookup"><span data-stu-id="7d3b4-137">Specifies or retrieves the saturation value of the **BUTTONGROUP** images.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="7d3b4-138">obter plano de fundo</span><span class="sxs-lookup"><span data-stu-id="7d3b4-138">showBackground</span></span>](buttongroup-showbackground.md)       | <span data-ttu-id="7d3b4-139">Especifica ou recupera um valor que indica se o **MyButton** exibe apenas os botões ou exibe o bitmap completo especificado no atributo **Image** .</span><span class="sxs-lookup"><span data-stu-id="7d3b4-139">Specifies or retrieves a value indicating whether the **BUTTONGROUP** displays only the buttons, or displays the full bitmap specified in the **image** attribute.</span></span>                                                              |
| [<span data-ttu-id="7d3b4-140">transparencyColor</span><span class="sxs-lookup"><span data-stu-id="7d3b4-140">transparencyColor</span></span>](buttongroup-transparencycolor.md) | <span data-ttu-id="7d3b4-141">Especifica ou recupera a cor transparente das imagens de um **botão** .</span><span class="sxs-lookup"><span data-stu-id="7d3b4-141">Specifies or retrieves the transparent color of the **BUTTONGROUP** images.</span></span>                                                                                                                                                     |



 

<span data-ttu-id="7d3b4-142">O elemento **Button** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-142">The **BUTTONGROUP** element supports the following methods.</span></span>



| <span data-ttu-id="7d3b4-143">Método</span><span class="sxs-lookup"><span data-stu-id="7d3b4-143">Method</span></span>                                 | <span data-ttu-id="7d3b4-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d3b4-144">Description</span></span>                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d3b4-145">Selecione</span><span class="sxs-lookup"><span data-stu-id="7d3b4-145">click</span></span>](buttongroup-click.md)         | <span data-ttu-id="7d3b4-146">Chama o manipulador de eventos **onclick** definido para o **buttonelement** com o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-146">Calls the **onclick** event handler defined for the **BUTTONELEMENT** with the specified index.</span></span> |
| [<span data-ttu-id="7d3b4-147">getbutton</span><span class="sxs-lookup"><span data-stu-id="7d3b4-147">getButton</span></span>](buttongroup-getbutton.md) | <span data-ttu-id="7d3b4-148">Recupera o **botãoelement** com o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-148">Retrieves the **BUTTONELEMENT** with the specified index.</span></span>                                       |



 

<span data-ttu-id="7d3b4-149">O elemento de **botão** é compatível com os atributos de ambiente e pode implementar os manipuladores de eventos de ambiente.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-149">The **BUTTONGROUP** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="7d3b4-150">Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md) e [manipuladores de eventos de ambiente](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="7d3b4-150">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d3b4-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d3b4-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d3b4-152">**Referência de programação de capa**</span><span class="sxs-lookup"><span data-stu-id="7d3b4-152">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




