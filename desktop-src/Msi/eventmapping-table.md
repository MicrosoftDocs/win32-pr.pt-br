---
description: A tabela EventMappings lista os controles que assinam alguns eventos de controle e lista o atributo a ser alterado quando o evento é publicado por outro controle ou pelo Windows Installer.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: Tabela EventMappings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e9a7b5b4283b5d70102123dcb11e3e9e844221
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827949"
---
# <a name="eventmapping-table"></a><span data-ttu-id="a7308-103">Tabela EventMappings</span><span class="sxs-lookup"><span data-stu-id="a7308-103">EventMapping Table</span></span>

<span data-ttu-id="a7308-104">A tabela EventMappings lista os controles que assinam alguns eventos de controle e lista o atributo a ser alterado quando o evento é publicado por outro controle ou pelo Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a7308-104">The EventMapping Table lists the controls that subscribe to some control events, and lists the attribute to be changed when the event is published by another control or the Windows Installer.</span></span>

<span data-ttu-id="a7308-105">A tabela EventMappings tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7308-105">The EventMapping Table has the following columns.</span></span>



| <span data-ttu-id="a7308-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="a7308-106">Column</span></span>    | <span data-ttu-id="a7308-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7308-107">Type</span></span>                         | <span data-ttu-id="a7308-108">Chave</span><span class="sxs-lookup"><span data-stu-id="a7308-108">Key</span></span> | <span data-ttu-id="a7308-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="a7308-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="a7308-110">caixa de diálogo\_</span><span class="sxs-lookup"><span data-stu-id="a7308-110">Dialog\_</span></span>  | [<span data-ttu-id="a7308-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="a7308-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="a7308-112">S</span><span class="sxs-lookup"><span data-stu-id="a7308-112">Y</span></span>   | <span data-ttu-id="a7308-113">N</span><span class="sxs-lookup"><span data-stu-id="a7308-113">N</span></span>        |
| <span data-ttu-id="a7308-114">controle\_</span><span class="sxs-lookup"><span data-stu-id="a7308-114">Control\_</span></span> | [<span data-ttu-id="a7308-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="a7308-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="a7308-116">S</span><span class="sxs-lookup"><span data-stu-id="a7308-116">Y</span></span>   | <span data-ttu-id="a7308-117">N</span><span class="sxs-lookup"><span data-stu-id="a7308-117">N</span></span>        |
| <span data-ttu-id="a7308-118">Evento</span><span class="sxs-lookup"><span data-stu-id="a7308-118">Event</span></span>     | [<span data-ttu-id="a7308-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="a7308-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="a7308-120">S</span><span class="sxs-lookup"><span data-stu-id="a7308-120">Y</span></span>   | <span data-ttu-id="a7308-121">N</span><span class="sxs-lookup"><span data-stu-id="a7308-121">N</span></span>        |
| <span data-ttu-id="a7308-122">Atributo</span><span class="sxs-lookup"><span data-stu-id="a7308-122">Attribute</span></span> | [<span data-ttu-id="a7308-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="a7308-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="a7308-124">N</span><span class="sxs-lookup"><span data-stu-id="a7308-124">N</span></span>   | <span data-ttu-id="a7308-125">N</span><span class="sxs-lookup"><span data-stu-id="a7308-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a7308-126">Colunas</span><span class="sxs-lookup"><span data-stu-id="a7308-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a7308-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>'\_</span><span class="sxs-lookup"><span data-stu-id="a7308-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="a7308-128">Uma chave externa para a primeira coluna da [tabela de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="a7308-128">An external key to the first column of the [Dialog Table](dialog-table.md).</span></span> <span data-ttu-id="a7308-129">Esse campo e o campo de controle, \_ juntos, identificam um controle.</span><span class="sxs-lookup"><span data-stu-id="a7308-129">This field and the Control\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="a7308-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controlo\_</span><span class="sxs-lookup"><span data-stu-id="a7308-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="a7308-131">Uma chave externa para a segunda coluna da [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="a7308-131">An external key to the second column of the [Control Table](control-table.md).</span></span> <span data-ttu-id="a7308-132">Esse campo e o campo da caixa de diálogo \_ identificam um controle.</span><span class="sxs-lookup"><span data-stu-id="a7308-132">This field and the Dialog\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="a7308-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Circunstância</span><span class="sxs-lookup"><span data-stu-id="a7308-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="a7308-134">Esse campo é um identificador que especifica o tipo de evento que é assinado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="a7308-134">This field is an identifier that specifies the type of event that is subscribed to by the control.</span></span> <span data-ttu-id="a7308-135">Para obter mais informações, consulte [visão geral do ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a7308-135">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7308-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="a7308-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="a7308-137">O nome do atributo de controle \_ que é definido quando o evento na coluna de evento é recebido.</span><span class="sxs-lookup"><span data-stu-id="a7308-137">The name of the Control\_ attribute that is set when the event in the Event column is received.</span></span> <span data-ttu-id="a7308-138">O argumento do evento é passado como o argumento da chamada de atributo para alterar esse atributo do controle.</span><span class="sxs-lookup"><span data-stu-id="a7308-138">The Argument of the event is passed as the argument of the attribute call to change this attribute of the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7308-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7308-139">Remarks</span></span>

<span data-ttu-id="a7308-140">A [tabela ControlEvent,](controlevent-table.md) especifica os eventos de controle que são iniciados quando um usuário interage com um controle de [pressão](pushbutton-control.md), [controle de caixa de seleção](checkbox-control.md)ou [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="a7308-140">The [ControlEvent Table](controlevent-table.md) specifies the control events that are started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="a7308-141">Esses são os únicos controles que um usuário pode usar para iniciar eventos de controle.</span><span class="sxs-lookup"><span data-stu-id="a7308-141">These are the only controls that a user can use to initiate control events.</span></span>

<span data-ttu-id="a7308-142">Mais de um controle em uma caixa de diálogo pode assinar o mesmo evento.</span><span class="sxs-lookup"><span data-stu-id="a7308-142">More than one control on a dialog box can subscribe to the same event.</span></span>

<span data-ttu-id="a7308-143">A lista a seguir identifica os usos típicos para a tabela EventMappings:</span><span class="sxs-lookup"><span data-stu-id="a7308-143">The following list identifies the typical uses for the EventMapping Table:</span></span>

-   <span data-ttu-id="a7308-144">Para assinar um [controle de texto](text-control.md) para um [ActionText ControlEvent,](actiontext-controlevent.md), [ActionData ControlEvent,](actiondata-controlevent.md), [ScriptInProgress ControlEvent,](scriptinprogress-controlevent.md) ou [timecontinueing ControlEvent,](timeremaining-controlevent.md) publicados pelo Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a7308-144">To subscribe a [Text Control](text-control.md) to an [ActionText ControlEvent](actiontext-controlevent.md), [ActionData ControlEvent](actiondata-controlevent.md), [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) or [TimeRemaining ControlEvent](timeremaining-controlevent.md) published by the Windows Installer.</span></span>
-   <span data-ttu-id="a7308-145">Para assinar um controle [ProgressBar](progressbar-control.md) ou um [controle de mensagem](billboard-control.md) para um ControlEvent, de [reprogress](setprogress-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="a7308-145">To subscribe a [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) to a [SetProgress ControlEvent](setprogress-controlevent.md).</span></span>
-   <span data-ttu-id="a7308-146">Para assinar um [controle DirectoryCombo](directorycombo-control.md) para um [IgnoreChange ControlEvent,](ignorechange-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="a7308-146">To subscribe a [DirectoryCombo Control](directorycombo-control.md) to an [IgnoreChange ControlEvent](ignorechange-controlevent.md).</span></span>
-   <span data-ttu-id="a7308-147">Para desabilitar automaticamente um [controle de pressão](pushbutton-control.md) localizado na mesma caixa de diálogo com um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="a7308-147">To automatically disable a [PushButton Control](pushbutton-control.md) located on the same dialog with a [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="a7308-148">Para desabilitar o botão de ação quando nenhum recurso estiver listado no [controle SelectionTree](selectiontree-control.md), use a tabela EventMappings para assinar o controle de pressão para um [SelectionNoItems ControlEvent,](selectionnoitems-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="a7308-148">To disable the push button when no features are listed in the [SelectionTree Control](selectiontree-control.md), use the EventMapping Table to subscribe the PushButton control to a [SelectionNoItems ControlEvent](selectionnoitems-controlevent.md).</span></span> <span data-ttu-id="a7308-149">Digite **habilitar** no campo atributos da tabela EventMappings.</span><span class="sxs-lookup"><span data-stu-id="a7308-149">Enter **Enable** in the Attributes field of the EventMapping Table.</span></span>
-   <span data-ttu-id="a7308-150">Para exibir um [controle de texto](text-control.md) que mostra o caminho para o local de instalação do recurso selecionado em um [controle SelectionTree](selectiontree-control.md) na mesma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a7308-150">To display a [Text Control](text-control.md) that shows the path to the installation location for the feature that is selected in a [SelectionTree Control](selectiontree-control.md) on the same dialog.</span></span> <span data-ttu-id="a7308-151">Use a tabela EventMappings para assinar o [controle de texto](text-control.md) para um [SelectionPathOn ControlEvent,](selectionpathon-controlevent.md) e [SelectionPath ControlEvent,](selectionpath-controlevent.md) publicados pelo [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="a7308-151">Use the EventMapping Table to subscribe the [Text Control](text-control.md) to both a [SelectionPathOn ControlEvent](selectionpathon-controlevent.md) and [SelectionPath ControlEvent](selectionpath-controlevent.md) published by the [SelectionTree Control](selectiontree-control.md).</span></span>
-   <span data-ttu-id="a7308-152">Para exibir um [controle de texto](text-control.md) que mostra uma descrição do item realçado em um [controle SelectionTree](selectiontree-control.md) localizado na mesma caixa de diálogo, use a tabela EventMappings para inscrever o [controle de texto](text-control.md) em um [SelectionDescription ControlEvent,](selectiondescription-controlevent.md), [SelectionSize ControlEvent,](selectionsize-controlevent.md) ou [selectionaction ControlEvent,](selectionaction-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="a7308-152">To display a [Text Control](text-control.md) that shows a description of the item highlighted in a [SelectionTree Control](selectiontree-control.md) located on the same dialog, use the EventMapping Table to subscribe the [Text Control](text-control.md) to a [SelectionDescription ControlEvent](selectiondescription-controlevent.md), [SelectionSize ControlEvent](selectionsize-controlevent.md) or [SelectionAction ControlEvent](selectionaction-controlevent.md).</span></span> <span data-ttu-id="a7308-153">Insira o **texto** no campo atributo da tabela EventMappings.</span><span class="sxs-lookup"><span data-stu-id="a7308-153">Enter **Text** in the Attribute field of the EventMapping Table.</span></span>

## <a name="validation"></a><span data-ttu-id="a7308-154">Validação</span><span class="sxs-lookup"><span data-stu-id="a7308-154">Validation</span></span>

<dl>

[<span data-ttu-id="a7308-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="a7308-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a7308-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="a7308-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a7308-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="a7308-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



