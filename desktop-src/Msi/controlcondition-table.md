---
description: A tabela ControlCondition permite que um autor especifique ações especiais a serem aplicadas a controles com base no resultado de uma instrução condicional. Por exemplo, usando essa tabela, o autor pode optar por ocultar um controle com base na propriedade VersionNT.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: Tabela ControlCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671dcdee6e2ed1067c51a04084693c276b8db2d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922138"
---
# <a name="controlcondition-table"></a><span data-ttu-id="ab1be-104">Tabela ControlCondition</span><span class="sxs-lookup"><span data-stu-id="ab1be-104">ControlCondition Table</span></span>

<span data-ttu-id="ab1be-105">A tabela ControlCondition permite que um autor especifique ações especiais a serem aplicadas a controles com base no resultado de uma instrução condicional.</span><span class="sxs-lookup"><span data-stu-id="ab1be-105">The ControlCondition table enables an author to specify special actions to be applied to controls based on the result of a conditional statement.</span></span> <span data-ttu-id="ab1be-106">Por exemplo, usando essa tabela, o autor pode optar por ocultar um controle com base na propriedade [**VersionNT**](versionnt.md) .</span><span class="sxs-lookup"><span data-stu-id="ab1be-106">For example, using this table the author could choose to hide a control based on the [**VersionNT**](versionnt.md) property.</span></span>

<span data-ttu-id="ab1be-107">A tabela ControlCondition tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab1be-107">The ControlCondition table has the following columns.</span></span>



| <span data-ttu-id="ab1be-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="ab1be-108">Column</span></span>    | <span data-ttu-id="ab1be-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab1be-109">Type</span></span>                         | <span data-ttu-id="ab1be-110">Chave</span><span class="sxs-lookup"><span data-stu-id="ab1be-110">Key</span></span> | <span data-ttu-id="ab1be-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="ab1be-111">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="ab1be-112">caixa de diálogo\_</span><span class="sxs-lookup"><span data-stu-id="ab1be-112">Dialog\_</span></span>  | [<span data-ttu-id="ab1be-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="ab1be-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="ab1be-114">S</span><span class="sxs-lookup"><span data-stu-id="ab1be-114">Y</span></span>   | <span data-ttu-id="ab1be-115">N</span><span class="sxs-lookup"><span data-stu-id="ab1be-115">N</span></span>        |
| <span data-ttu-id="ab1be-116">controle\_</span><span class="sxs-lookup"><span data-stu-id="ab1be-116">Control\_</span></span> | [<span data-ttu-id="ab1be-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="ab1be-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="ab1be-118">S</span><span class="sxs-lookup"><span data-stu-id="ab1be-118">Y</span></span>   | <span data-ttu-id="ab1be-119">N</span><span class="sxs-lookup"><span data-stu-id="ab1be-119">N</span></span>        |
| <span data-ttu-id="ab1be-120">Ação</span><span class="sxs-lookup"><span data-stu-id="ab1be-120">Action</span></span>    | [<span data-ttu-id="ab1be-121">Text</span><span class="sxs-lookup"><span data-stu-id="ab1be-121">Text</span></span>](text.md)             | <span data-ttu-id="ab1be-122">S</span><span class="sxs-lookup"><span data-stu-id="ab1be-122">Y</span></span>   | <span data-ttu-id="ab1be-123">N</span><span class="sxs-lookup"><span data-stu-id="ab1be-123">N</span></span>        |
| <span data-ttu-id="ab1be-124">Condição</span><span class="sxs-lookup"><span data-stu-id="ab1be-124">Condition</span></span> | [<span data-ttu-id="ab1be-125">Condição</span><span class="sxs-lookup"><span data-stu-id="ab1be-125">Condition</span></span>](condition.md)   | <span data-ttu-id="ab1be-126">S</span><span class="sxs-lookup"><span data-stu-id="ab1be-126">Y</span></span>   | <span data-ttu-id="ab1be-127">N</span><span class="sxs-lookup"><span data-stu-id="ab1be-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ab1be-128">Colunas</span><span class="sxs-lookup"><span data-stu-id="ab1be-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ab1be-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>'\_</span><span class="sxs-lookup"><span data-stu-id="ab1be-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="ab1be-130">Uma chave externa para a primeira coluna da [tabela de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab1be-130">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="ab1be-131">A combinação desse campo com o \_ campo de controle identifica um controle exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ab1be-131">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="ab1be-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controlo\_</span><span class="sxs-lookup"><span data-stu-id="ab1be-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="ab1be-133">Uma chave externa para a segunda coluna da [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab1be-133">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="ab1be-134">Combinando este campo, o campo de caixa de diálogo \_ identifica um controle exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ab1be-134">Combining this field the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="ab1be-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="ab1be-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="ab1be-136">A ação a ser executada no controle.</span><span class="sxs-lookup"><span data-stu-id="ab1be-136">The action that is to be taken on the control.</span></span> <span data-ttu-id="ab1be-137">As ações possíveis são mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab1be-137">The possible actions are shown in the following table.</span></span>



| <span data-ttu-id="ab1be-138">Valor</span><span class="sxs-lookup"><span data-stu-id="ab1be-138">Value</span></span>   | <span data-ttu-id="ab1be-139">Significado</span><span class="sxs-lookup"><span data-stu-id="ab1be-139">Meaning</span></span>                     |
|---------|-----------------------------|
| <span data-ttu-id="ab1be-140">Padrão</span><span class="sxs-lookup"><span data-stu-id="ab1be-140">Default</span></span> | <span data-ttu-id="ab1be-141">Defina o controle como o padrão.</span><span class="sxs-lookup"><span data-stu-id="ab1be-141">Set control as the default.</span></span> |
| <span data-ttu-id="ab1be-142">Desabilitar</span><span class="sxs-lookup"><span data-stu-id="ab1be-142">Disable</span></span> | <span data-ttu-id="ab1be-143">Desabilite o controle.</span><span class="sxs-lookup"><span data-stu-id="ab1be-143">Disable the control.</span></span>        |
| <span data-ttu-id="ab1be-144">Habilitar</span><span class="sxs-lookup"><span data-stu-id="ab1be-144">Enable</span></span>  | <span data-ttu-id="ab1be-145">Habilite o controle.</span><span class="sxs-lookup"><span data-stu-id="ab1be-145">Enable the control.</span></span>         |
| <span data-ttu-id="ab1be-146">Ocultar</span><span class="sxs-lookup"><span data-stu-id="ab1be-146">Hide</span></span>    | <span data-ttu-id="ab1be-147">Ocultar o controle.</span><span class="sxs-lookup"><span data-stu-id="ab1be-147">Hide the control.</span></span>           |
| <span data-ttu-id="ab1be-148">Mostrar</span><span class="sxs-lookup"><span data-stu-id="ab1be-148">Show</span></span>    | <span data-ttu-id="ab1be-149">Exibir o controle.</span><span class="sxs-lookup"><span data-stu-id="ab1be-149">Display the control.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="ab1be-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="ab1be-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="ab1be-151">Uma instrução condicional que especifica sob quais condições a ação deve ser disparada.</span><span class="sxs-lookup"><span data-stu-id="ab1be-151">A conditional statement that specifies under which conditions the action should be triggered.</span></span> <span data-ttu-id="ab1be-152">Esta coluna não pode ser deixada em branco.</span><span class="sxs-lookup"><span data-stu-id="ab1be-152">This column may not be left blank.</span></span> <span data-ttu-id="ab1be-153">Se essa instrução não for avaliada como TRUE, a ação não ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="ab1be-153">If this statement does not evaluate to TRUE, the action does not take place.</span></span> <span data-ttu-id="ab1be-154">Se estiver definido como 1, a ação sempre será aplicada.</span><span class="sxs-lookup"><span data-stu-id="ab1be-154">If it is set to 1, the action is always applied.</span></span> <span data-ttu-id="ab1be-155">Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="ab1be-155">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab1be-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab1be-156">Remarks</span></span>

<span data-ttu-id="ab1be-157">Se você quiser ocultar e desabilitar um controle de [pressão](pushbutton-control.md) ou [controle de caixa de seleção](checkbox-control.md) com base em uma instrução condicional no campo condição da tabela ControlCondition, deverá usar quatro registros para cada controle para desabilitar e ocultar o controle.</span><span class="sxs-lookup"><span data-stu-id="ab1be-157">If you want to hide and disable a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) based on a conditional statement in the Condition field of the ControlCondition table, you should use four records for each control to disable as well as hide the control.</span></span> <span data-ttu-id="ab1be-158">Os controles de pressão ou caixa de seleção que só foram ocultos ainda podem ser acessados por teclas de atalho.</span><span class="sxs-lookup"><span data-stu-id="ab1be-158">PushButton or CheckBox controls that have only been hidden can still be accessed by shortcut keys.</span></span>

<span data-ttu-id="ab1be-159">Por exemplo, os seguintes registros ocultam e desabilitam o ControlA na caixa de diálogo quando o produto é instalado.</span><span class="sxs-lookup"><span data-stu-id="ab1be-159">For example, the following records hide and disable ControlA on DialogA when the product is installed.</span></span> <span data-ttu-id="ab1be-160">O controle ficará visível e habilitado quando o produto não estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="ab1be-160">The control will be visible and enabled when the product is not installed.</span></span>



| <span data-ttu-id="ab1be-161">caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="ab1be-161">Dialog</span></span>  | <span data-ttu-id="ab1be-162">Control</span><span class="sxs-lookup"><span data-stu-id="ab1be-162">Control</span></span>  | <span data-ttu-id="ab1be-163">Ação</span><span class="sxs-lookup"><span data-stu-id="ab1be-163">Action</span></span>  | <span data-ttu-id="ab1be-164">Condição</span><span class="sxs-lookup"><span data-stu-id="ab1be-164">Condition</span></span>                      |
|---------|----------|---------|--------------------------------|
| <span data-ttu-id="ab1be-165">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="ab1be-165">DialogA</span></span> | <span data-ttu-id="ab1be-166">ControlA</span><span class="sxs-lookup"><span data-stu-id="ab1be-166">ControlA</span></span> | <span data-ttu-id="ab1be-167">Ocultar</span><span class="sxs-lookup"><span data-stu-id="ab1be-167">Hide</span></span>    | [<span data-ttu-id="ab1be-168">**Instalado**</span><span class="sxs-lookup"><span data-stu-id="ab1be-168">**Installed**</span></span>](installed.md) |
| <span data-ttu-id="ab1be-169">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="ab1be-169">DialogA</span></span> | <span data-ttu-id="ab1be-170">ControlA</span><span class="sxs-lookup"><span data-stu-id="ab1be-170">ControlA</span></span> | <span data-ttu-id="ab1be-171">Desabilitar</span><span class="sxs-lookup"><span data-stu-id="ab1be-171">Disable</span></span> | <span data-ttu-id="ab1be-172">Instalado</span><span class="sxs-lookup"><span data-stu-id="ab1be-172">Installed</span></span>                      |
| <span data-ttu-id="ab1be-173">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="ab1be-173">DialogA</span></span> | <span data-ttu-id="ab1be-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="ab1be-174">ControlA</span></span> | <span data-ttu-id="ab1be-175">Mostrar</span><span class="sxs-lookup"><span data-stu-id="ab1be-175">Show</span></span>    | <span data-ttu-id="ab1be-176">NÃO instalado</span><span class="sxs-lookup"><span data-stu-id="ab1be-176">NOT Installed</span></span>                  |
| <span data-ttu-id="ab1be-177">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="ab1be-177">DialogA</span></span> | <span data-ttu-id="ab1be-178">ControlA</span><span class="sxs-lookup"><span data-stu-id="ab1be-178">ControlA</span></span> | <span data-ttu-id="ab1be-179">Habilitar</span><span class="sxs-lookup"><span data-stu-id="ab1be-179">Enable</span></span>  | <span data-ttu-id="ab1be-180">NÃO instalado</span><span class="sxs-lookup"><span data-stu-id="ab1be-180">NOT Installed</span></span>                  |



 

## <a name="validation"></a><span data-ttu-id="ab1be-181">Validação</span><span class="sxs-lookup"><span data-stu-id="ab1be-181">Validation</span></span>

<dl>

[<span data-ttu-id="ab1be-182">ICE03</span><span class="sxs-lookup"><span data-stu-id="ab1be-182">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ab1be-183">ICE06</span><span class="sxs-lookup"><span data-stu-id="ab1be-183">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ab1be-184">ICE17</span><span class="sxs-lookup"><span data-stu-id="ab1be-184">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="ab1be-185">ICE32</span><span class="sxs-lookup"><span data-stu-id="ab1be-185">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ab1be-186">ICE46</span><span class="sxs-lookup"><span data-stu-id="ab1be-186">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="ab1be-187">ICE79</span><span class="sxs-lookup"><span data-stu-id="ab1be-187">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="ab1be-188">ICE86</span><span class="sxs-lookup"><span data-stu-id="ab1be-188">ICE86</span></span>](ice86.md)  
</dl>

 

 



