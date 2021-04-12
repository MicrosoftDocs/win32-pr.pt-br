---
title: Manipuladores de eventos de ambiente
description: Manipuladores de eventos de ambiente
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Capas do Windows Media Player, manipuladores de eventos de ambiente
- capas, manipuladores de eventos de ambiente
- referência para capas, manipuladores de eventos de ambiente
- manipuladores de eventos de ambiente
- eventos, ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363777"
---
# <a name="ambient-event-handlers"></a><span data-ttu-id="b946d-108">Manipuladores de eventos de ambiente</span><span class="sxs-lookup"><span data-stu-id="b946d-108">Ambient Event Handlers</span></span>

<span data-ttu-id="b946d-109">Os manipuladores de eventos a seguir podem ser implementados para a maioria dos elementos de capa.</span><span class="sxs-lookup"><span data-stu-id="b946d-109">The following event handlers can be implemented for most skin elements.</span></span> <span data-ttu-id="b946d-110">Os atributos de evento de ambiente acessados com a palavra-chave do **evento** podem ser usados dentro de um manipulador de eventos para determinar o estado do teclado e do mouse no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="b946d-110">The ambient event attributes accessed with the **event** keyword can be used within an event handler to determine the state of the keyboard and mouse at the time of the event.</span></span>



| <span data-ttu-id="b946d-111">Manipulador de eventos</span><span class="sxs-lookup"><span data-stu-id="b946d-111">Event handler</span></span>                                   | <span data-ttu-id="b946d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b946d-112">Description</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b946d-113">*atributo* \_ OnChange</span><span class="sxs-lookup"><span data-stu-id="b946d-113">*attribute*\_onchange</span></span>](attribute-onchange.md) | <span data-ttu-id="b946d-114">Quando um atributo de aparência muda de valor, ocorre um evento que pode ser manipulado por um manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="b946d-114">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="b946d-115">O nome do manipulador de eventos é o nome do atributo seguido por um sublinhado e "OnChange", como "valor \_ onChange".</span><span class="sxs-lookup"><span data-stu-id="b946d-115">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span> |
| [<span data-ttu-id="b946d-116">desfoque</span><span class="sxs-lookup"><span data-stu-id="b946d-116">onblur</span></span>](onblur.md)                            | <span data-ttu-id="b946d-117">Manipula um evento que ocorre quando o elemento perde o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="b946d-117">Handles an event that occurs when the element loses the keyboard focus.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="b946d-118">OnClick</span><span class="sxs-lookup"><span data-stu-id="b946d-118">onclick</span></span>](onclick.md)                          | <span data-ttu-id="b946d-119">Manipula um evento que ocorre quando o usuário clica no elemento.</span><span class="sxs-lookup"><span data-stu-id="b946d-119">Handles an event that occurs when the user clicks the element.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="b946d-120">AoClicarDuasVezes</span><span class="sxs-lookup"><span data-stu-id="b946d-120">ondblclick</span></span>](ondblclick.md)                    | <span data-ttu-id="b946d-121">Manipula um evento que ocorre quando o usuário clica duas vezes no elemento.</span><span class="sxs-lookup"><span data-stu-id="b946d-121">Handles an event that occurs when the user double-clicks the element.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="b946d-122">onendalphablend</span><span class="sxs-lookup"><span data-stu-id="b946d-122">onendalphablend</span></span>](onendalphablend.md)          | <span data-ttu-id="b946d-123">Manipula um evento que ocorre quando um elemento conclui uma operação **alphaBlendTo** .</span><span class="sxs-lookup"><span data-stu-id="b946d-123">Handles an event that occurs when an element completes an **alphaBlendTo** operation.</span></span>                                                                                                                                         |
| [<span data-ttu-id="b946d-124">onendmove</span><span class="sxs-lookup"><span data-stu-id="b946d-124">onendmove</span></span>](onendmove.md)                      | <span data-ttu-id="b946d-125">Manipula um evento que ocorre quando um elemento conclui uma operação **MoveTo** .</span><span class="sxs-lookup"><span data-stu-id="b946d-125">Handles an event that occurs when an element completes a **moveTo** operation.</span></span>                                                                                                                                                |
| [<span data-ttu-id="b946d-126">enfoco</span><span class="sxs-lookup"><span data-stu-id="b946d-126">onfocus</span></span>](onfocus.md)                          | <span data-ttu-id="b946d-127">Manipula um evento que ocorre quando o elemento recebe o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="b946d-127">Handles an event that occurs when the element receives the keyboard focus.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="b946d-128">AoApertarTecla</span><span class="sxs-lookup"><span data-stu-id="b946d-128">onkeydown</span></span>](onkeydown.md)                      | <span data-ttu-id="b946d-129">Manipula um evento que ocorre quando uma tecla é pressionada.</span><span class="sxs-lookup"><span data-stu-id="b946d-129">Handles an event that occurs when a key is pressed.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="b946d-130">OnKeyPress</span><span class="sxs-lookup"><span data-stu-id="b946d-130">onkeypress</span></span>](onkeypress.md)                    | <span data-ttu-id="b946d-131">Manipula um evento que ocorre quando o usuário pressiona uma tecla alfanumérica.</span><span class="sxs-lookup"><span data-stu-id="b946d-131">Handles an event that occurs when the user presses an alphanumeric key.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="b946d-132">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="b946d-132">onkeyup</span></span>](onkeyup.md)                          | <span data-ttu-id="b946d-133">Manipula um evento que ocorre quando uma chave é liberada.</span><span class="sxs-lookup"><span data-stu-id="b946d-133">Handles an event that occurs when a key is released.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="b946d-134">OnMouseDown</span><span class="sxs-lookup"><span data-stu-id="b946d-134">onmousedown</span></span>](onmousedown.md)                  | <span data-ttu-id="b946d-135">Manipula um evento que ocorre quando o usuário clica em um botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="b946d-135">Handles an event that occurs when the user clicks a mouse button.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="b946d-136">OnMouseMove</span><span class="sxs-lookup"><span data-stu-id="b946d-136">onmousemove</span></span>](onmousemove.md)                  | <span data-ttu-id="b946d-137">Manipula um evento que ocorre quando o usuário move o ponteiro do mouse enquanto ele está sobre um elemento.</span><span class="sxs-lookup"><span data-stu-id="b946d-137">Handles an event that occurs when the user moves the mouse pointer while it is over an element.</span></span>                                                                                                                               |
| [<span data-ttu-id="b946d-138">onmouseout</span><span class="sxs-lookup"><span data-stu-id="b946d-138">onmouseout</span></span>](onmouseout.md)                    | <span data-ttu-id="b946d-139">Manipula um evento que ocorre quando o usuário move o ponteiro para fora do elemento.</span><span class="sxs-lookup"><span data-stu-id="b946d-139">Handles an event that occurs when the user moves the pointer off the element.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="b946d-140">onmouseover</span><span class="sxs-lookup"><span data-stu-id="b946d-140">onmouseover</span></span>](onmouseover.md)                  | <span data-ttu-id="b946d-141">Manipula um evento que ocorre quando o usuário coloca o ponteiro pela primeira vez sobre o elemento.</span><span class="sxs-lookup"><span data-stu-id="b946d-141">Handles an event that occurs when the user first places the pointer over the element.</span></span>                                                                                                                                         |
| [<span data-ttu-id="b946d-142">OnMouseUp</span><span class="sxs-lookup"><span data-stu-id="b946d-142">onmouseup</span></span>](onmouseup.md)                      | <span data-ttu-id="b946d-143">Manipula um evento que ocorre quando o usuário libera um botão do mouse enquanto o ponteiro está sobre o elemento.</span><span class="sxs-lookup"><span data-stu-id="b946d-143">Handles an event that occurs when the user releases a mouse button while the pointer is over the element.</span></span>                                                                                                                     |
| [<span data-ttu-id="b946d-144">OnResize</span><span class="sxs-lookup"><span data-stu-id="b946d-144">onresize</span></span>](onresize.md)                        | <span data-ttu-id="b946d-145">Manipula um evento que ocorre quando um controle é redimensionado.</span><span class="sxs-lookup"><span data-stu-id="b946d-145">Handles an event that occurs when a control resizes.</span></span>                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="b946d-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b946d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b946d-147">**Atributos de evento de ambiente**</span><span class="sxs-lookup"><span data-stu-id="b946d-147">**Ambient Event Attributes**</span></span>](ambient-event-attributes.md)
</dt> <dt>

[<span data-ttu-id="b946d-148">**Referência de programação de capa**</span><span class="sxs-lookup"><span data-stu-id="b946d-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




