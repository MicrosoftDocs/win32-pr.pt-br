---
description: A tabela ControlEvent, permite que o autor especifique os eventos de controle iniciados quando um usuário interage com um controle de pressão, controle de caixa de seleção ou controle SelectionTree.
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: Tabela ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721dc7ac9a729b8df0623a2958a4d0fe32851307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837111"
---
# <a name="controlevent-table"></a><span data-ttu-id="e13c1-103">Tabela ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="e13c1-103">ControlEvent Table</span></span>

<span data-ttu-id="e13c1-104">A tabela ControlEvent, permite que o autor especifique os [eventos de controle](control-events.md) iniciados quando um usuário interage com um [controle de pressão](pushbutton-control.md), controle de caixa de [seleção](checkbox-control.md)ou [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="e13c1-104">The ControlEvent table allows the author to specify the [Control Events](control-events.md) started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="e13c1-105">Esses são os únicos controles que os usuários podem usar para iniciar eventos de controle.</span><span class="sxs-lookup"><span data-stu-id="e13c1-105">These are the only controls users can use to initiate control events.</span></span> <span data-ttu-id="e13c1-106">Cada controle pode publicar vários eventos de controle.</span><span class="sxs-lookup"><span data-stu-id="e13c1-106">Each control can publish multiple control events.</span></span> <span data-ttu-id="e13c1-107">O instalador inicia cada evento na ordem especificada na coluna ordenação.</span><span class="sxs-lookup"><span data-stu-id="e13c1-107">The installer starts each event in the order specified in the Ordering column.</span></span> <span data-ttu-id="e13c1-108">Por exemplo, um controle de botão de ação pode publicar eventos para iniciar uma transição para outra caixa de diálogo, sair da sequência da caixa de diálogo e iniciar a instalação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e13c1-108">For example, a push button control can publish events to initiate a transition to another dialog box, exit the dialog box sequence, and begin file installation.</span></span>

<span data-ttu-id="e13c1-109">A exceção a ser observada é que cada controle pode publicar um evento mais [NewDialog](newdialog-controlevent.md) ou um [SpawnDialog](spawndialog-controlevent.md) .</span><span class="sxs-lookup"><span data-stu-id="e13c1-109">The exception to note is that each control can publish a most one [NewDialog](newdialog-controlevent.md) or one [SpawnDialog](spawndialog-controlevent.md) event.</span></span> <span data-ttu-id="e13c1-110">Se você precisar criar vários eventos de controle NewDialog e SpawnDialog nesta tabela, também inclua instruções condicionais nos campos de condição que asseguram que, no máximo, um evento seja publicado.</span><span class="sxs-lookup"><span data-stu-id="e13c1-110">If you need to author multiple NewDialog and SpawnDialog control events in this table, also include conditional statements in the Condition fields that ensure at most one event is published.</span></span> <span data-ttu-id="e13c1-111">Se vários eventos de controle NewDialog e SpawnDialog forem selecionados para o mesmo controle, somente o evento com o maior valor na coluna ordenação será publicado quando o controle for ativado.</span><span class="sxs-lookup"><span data-stu-id="e13c1-111">If multiple NewDialog and SpawnDialog control events are selected for the same control, only the event with the largest value in the Ordering column gets published when the control is activated.</span></span>

<span data-ttu-id="e13c1-112">A tabela ControlEvent, tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="e13c1-112">The ControlEvent table has the following columns.</span></span>



| <span data-ttu-id="e13c1-113">Coluna</span><span class="sxs-lookup"><span data-stu-id="e13c1-113">Column</span></span>    | <span data-ttu-id="e13c1-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="e13c1-114">Type</span></span>                         | <span data-ttu-id="e13c1-115">Chave</span><span class="sxs-lookup"><span data-stu-id="e13c1-115">Key</span></span> | <span data-ttu-id="e13c1-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="e13c1-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="e13c1-117">caixa de diálogo\_</span><span class="sxs-lookup"><span data-stu-id="e13c1-117">Dialog\_</span></span>  | [<span data-ttu-id="e13c1-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="e13c1-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="e13c1-119">S</span><span class="sxs-lookup"><span data-stu-id="e13c1-119">Y</span></span>   | <span data-ttu-id="e13c1-120">N</span><span class="sxs-lookup"><span data-stu-id="e13c1-120">N</span></span>        |
| <span data-ttu-id="e13c1-121">controle\_</span><span class="sxs-lookup"><span data-stu-id="e13c1-121">Control\_</span></span> | [<span data-ttu-id="e13c1-122">Identificador</span><span class="sxs-lookup"><span data-stu-id="e13c1-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="e13c1-123">S</span><span class="sxs-lookup"><span data-stu-id="e13c1-123">Y</span></span>   | <span data-ttu-id="e13c1-124">N</span><span class="sxs-lookup"><span data-stu-id="e13c1-124">N</span></span>        |
| <span data-ttu-id="e13c1-125">Evento</span><span class="sxs-lookup"><span data-stu-id="e13c1-125">Event</span></span>     | [<span data-ttu-id="e13c1-126">Binário</span><span class="sxs-lookup"><span data-stu-id="e13c1-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e13c1-127">S</span><span class="sxs-lookup"><span data-stu-id="e13c1-127">Y</span></span>   | <span data-ttu-id="e13c1-128">N</span><span class="sxs-lookup"><span data-stu-id="e13c1-128">N</span></span>        |
| <span data-ttu-id="e13c1-129">Argumento</span><span class="sxs-lookup"><span data-stu-id="e13c1-129">Argument</span></span>  | [<span data-ttu-id="e13c1-130">Binário</span><span class="sxs-lookup"><span data-stu-id="e13c1-130">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e13c1-131">S</span><span class="sxs-lookup"><span data-stu-id="e13c1-131">Y</span></span>   | <span data-ttu-id="e13c1-132">N</span><span class="sxs-lookup"><span data-stu-id="e13c1-132">N</span></span>        |
| <span data-ttu-id="e13c1-133">Condição</span><span class="sxs-lookup"><span data-stu-id="e13c1-133">Condition</span></span> | [<span data-ttu-id="e13c1-134">Condição</span><span class="sxs-lookup"><span data-stu-id="e13c1-134">Condition</span></span>](condition.md)   | <span data-ttu-id="e13c1-135">S</span><span class="sxs-lookup"><span data-stu-id="e13c1-135">Y</span></span>   | <span data-ttu-id="e13c1-136">S</span><span class="sxs-lookup"><span data-stu-id="e13c1-136">Y</span></span>        |
| <span data-ttu-id="e13c1-137">Ordenando</span><span class="sxs-lookup"><span data-stu-id="e13c1-137">Ordering</span></span>  | [<span data-ttu-id="e13c1-138">Inteiro</span><span class="sxs-lookup"><span data-stu-id="e13c1-138">Integer</span></span>](integer.md)       | <span data-ttu-id="e13c1-139">N</span><span class="sxs-lookup"><span data-stu-id="e13c1-139">N</span></span>   | <span data-ttu-id="e13c1-140">S</span><span class="sxs-lookup"><span data-stu-id="e13c1-140">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e13c1-141">Colunas</span><span class="sxs-lookup"><span data-stu-id="e13c1-141">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e13c1-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>'\_</span><span class="sxs-lookup"><span data-stu-id="e13c1-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="e13c1-143">Uma chave externa para a primeira coluna da [tabela de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="e13c1-143">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="e13c1-144">A combinação desse campo com o \_ campo de controle identifica um controle exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e13c1-144">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="e13c1-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controlo\_</span><span class="sxs-lookup"><span data-stu-id="e13c1-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="e13c1-146">Uma chave externa para a segunda coluna da [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="e13c1-146">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="e13c1-147">A combinação deste campo com o campo de caixa de diálogo \_ identifica um controle exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e13c1-147">Combining this field with the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="e13c1-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Circunstância</span><span class="sxs-lookup"><span data-stu-id="e13c1-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="e13c1-149">Um identificador que especifica o tipo de evento que deve ocorrer quando o usuário interage com o controle especificado pela caixa de diálogo \_ e controle \_ .</span><span class="sxs-lookup"><span data-stu-id="e13c1-149">An identifier that specifies the type of event that should take place when the user interacts with the control specified by Dialog\_ and Control\_.</span></span> <span data-ttu-id="e13c1-150">Para obter uma lista de valores possíveis, consulte [visão geral do ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e13c1-150">For a list of possible values see [ControlEvent Overview](controlevent-overview.md).</span></span>

<span data-ttu-id="e13c1-151">Para definir uma propriedade com um controle, coloque \[ \_ o nome \] da propriedade nesse campo e o novo valor no campo argumento.</span><span class="sxs-lookup"><span data-stu-id="e13c1-151">To set a property with a control, put \[Property\_Name\] in this field and the new value in the argument field.</span></span> <span data-ttu-id="e13c1-152">Coloque {} no campo de argumento para inserir o valor nulo.</span><span class="sxs-lookup"><span data-stu-id="e13c1-152">Put { } into the argument field to enter the null value.</span></span>

</dd> <dt>

<span data-ttu-id="e13c1-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento</span><span class="sxs-lookup"><span data-stu-id="e13c1-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="e13c1-154">Um valor usado como um modificador ao disparar um evento específico.</span><span class="sxs-lookup"><span data-stu-id="e13c1-154">A value used as a modifier when triggering a particular event.</span></span>

<span data-ttu-id="e13c1-155">Por exemplo, o argumento de [NewDialog ControlEvent,](newdialog-controlevent.md) ou [SpawnDialog ControlEvent,](spawndialog-controlevent.md) é o nome da caixa de diálogo e o argumento da [ação de instalação](install-action.md) é um número que define o nível de instalação.</span><span class="sxs-lookup"><span data-stu-id="e13c1-155">For example, the argument of the [NewDialog ControlEvent](newdialog-controlevent.md) or the [SpawnDialog ControlEvent](spawndialog-controlevent.md) is the name of the dialog box and the argument of the [Install action](install-action.md) is a number defining the install level.</span></span>

</dd> <dt>

<span data-ttu-id="e13c1-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="e13c1-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="e13c1-157">Uma instrução condicional que determina se o instalador ativa o evento na coluna de evento.</span><span class="sxs-lookup"><span data-stu-id="e13c1-157">A conditional statement that determines whether the installer activates the event in the Event column.</span></span> <span data-ttu-id="e13c1-158">O instalador acionará o evento se a instrução condicional no campo condição for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="e13c1-158">The installer triggers the event if the conditional statement in the Condition field evaluates to True.</span></span> <span data-ttu-id="e13c1-159">Portanto, coloque um 1 nesta coluna para garantir que o instalador dispare o evento.</span><span class="sxs-lookup"><span data-stu-id="e13c1-159">Therefore put a 1 in this column to ensure that the installer triggers the event.</span></span> <span data-ttu-id="e13c1-160">O instalador não acionará o evento se o campo condição contiver uma instrução que seja avaliada como false.</span><span class="sxs-lookup"><span data-stu-id="e13c1-160">The installer does not trigger the event if the Condition field contains a statement that evaluates to False.</span></span> <span data-ttu-id="e13c1-161">O instalador não aciona um evento com um espaço em branco no campo condição, a menos que nenhum outro evento do controle seja avaliado como true.</span><span class="sxs-lookup"><span data-stu-id="e13c1-161">The installer does not trigger an event with a blank in the Condition field unless no other events of the control evaluate to True.</span></span> <span data-ttu-id="e13c1-162">Se nenhum dos campos de condição do controle nomeado no campo de controle \_ for avaliado como true, o instalador acionará um evento com condição em branco e, se mais de um campo de condição estiver em branco, ele acionará um evento com o maior valor no campo de ordenação.</span><span class="sxs-lookup"><span data-stu-id="e13c1-162">If none of the Condition fields for the control named in the Control\_ field evaluate to True, the installer triggers the one event having a blank Condition field, and if more than one Condition field is blank it triggers the one event of these with the largest value in the Ordering field.</span></span> <span data-ttu-id="e13c1-163">Consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e13c1-163">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="e13c1-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordenação</span><span class="sxs-lookup"><span data-stu-id="e13c1-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="e13c1-165">Um inteiro usado para ordenar vários eventos vinculados ao mesmo controle.</span><span class="sxs-lookup"><span data-stu-id="e13c1-165">An integer used to order several events tied to the same control.</span></span> <span data-ttu-id="e13c1-166">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="e13c1-166">This must be a non-negative number.</span></span> <span data-ttu-id="e13c1-167">Este campo pode ser deixado em branco.</span><span class="sxs-lookup"><span data-stu-id="e13c1-167">This field may be left blank.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e13c1-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="e13c1-168">Remarks</span></span>

<span data-ttu-id="e13c1-169">A [tabela EventMappings](eventmapping-table.md) lista os controles que assinam um evento de controle e lista o atributo de controle a ser alterado quando esse evento é publicado por outro controle ou o instalador.</span><span class="sxs-lookup"><span data-stu-id="e13c1-169">The [EventMapping table](eventmapping-table.md) lists the controls that subscribe to some control event and lists the control attribute to be changed when that event is published by the another control or the installer.</span></span>

<span data-ttu-id="e13c1-170">No Windows XP ou em sistemas operacionais anteriores, os usuários podem publicar um evento de controle apenas interagindo com um [controle de caixa de seleção](checkbox-control.md) ou controle de [pressão](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="e13c1-170">On Windows XP or earlier operating systems, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md) or [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="e13c1-171">Com o Windows Server 2003, os usuários podem publicar um evento de controle apenas interagindo com um [controle de caixa de seleção](checkbox-control.md), [controle SelectionTree](selectiontree-control.md)e [controle de supressão](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="e13c1-171">With Windows Server 2003, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md), [SelectionTree Control](selectiontree-control.md), and [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="e13c1-172">A listagem de outros controles no \_ campo de controle não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="e13c1-172">Listing other controls in the Control\_ field has no effect.</span></span>

## <a name="validation"></a><span data-ttu-id="e13c1-173">Validação</span><span class="sxs-lookup"><span data-stu-id="e13c1-173">Validation</span></span>

<dl>

[<span data-ttu-id="e13c1-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="e13c1-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e13c1-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="e13c1-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e13c1-176">ICE17</span><span class="sxs-lookup"><span data-stu-id="e13c1-176">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="e13c1-177">ICE20</span><span class="sxs-lookup"><span data-stu-id="e13c1-177">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="e13c1-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="e13c1-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e13c1-179">ICE44</span><span class="sxs-lookup"><span data-stu-id="e13c1-179">ICE44</span></span>](ice44.md)  
[<span data-ttu-id="e13c1-180">ICE46</span><span class="sxs-lookup"><span data-stu-id="e13c1-180">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="e13c1-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="e13c1-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="e13c1-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="e13c1-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



