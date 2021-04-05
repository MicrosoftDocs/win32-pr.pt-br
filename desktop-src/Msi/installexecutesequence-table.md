---
description: A tabela InstallExecuteSequence lista as ações que são executadas quando a ação de instalação de nível superior é executada.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: Tabela InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827001"
---
# <a name="installexecutesequence-table"></a><span data-ttu-id="16041-103">Tabela InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="16041-103">InstallExecuteSequence Table</span></span>

<span data-ttu-id="16041-104">A tabela InstallExecuteSequence lista as ações que são executadas quando a ação de [instalação](install-action.md) de nível superior é executada.</span><span class="sxs-lookup"><span data-stu-id="16041-104">The InstallExecuteSequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed.</span></span>

<span data-ttu-id="16041-105">As ações na sequência de instalação até a [ação InstallValidate](installvalidate-action.md)e todas as caixas de diálogo de saída estão localizadas na [tabela InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="16041-105">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="16041-106">Todas as ações do InstallValidate até o final da sequência de instalação estão na tabela InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="16041-106">All actions from the InstallValidate through the end of the install sequence are in the InstallExecuteSequence table.</span></span> <span data-ttu-id="16041-107">Como a tabela InstallExecuteSequence precisa ser autônoma, ela tem todas as ações de inicialização necessárias, como as ações [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="16041-107">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="16041-108">As [ações personalizadas](custom-actions.md) que exigem uma interface do usuário devem usar [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) em vez de caixas de diálogo criadas usando a [tabela de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="16041-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="16041-109">A tabela InstallExecuteSequence tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="16041-109">The InstallExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="16041-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="16041-110">Column</span></span>    | <span data-ttu-id="16041-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="16041-111">Type</span></span>                         | <span data-ttu-id="16041-112">Chave</span><span class="sxs-lookup"><span data-stu-id="16041-112">Key</span></span> | <span data-ttu-id="16041-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="16041-113">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="16041-114">Ação</span><span class="sxs-lookup"><span data-stu-id="16041-114">Action</span></span>    | [<span data-ttu-id="16041-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="16041-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="16041-116">S</span><span class="sxs-lookup"><span data-stu-id="16041-116">Y</span></span>   | <span data-ttu-id="16041-117">N</span><span class="sxs-lookup"><span data-stu-id="16041-117">N</span></span>        |
| <span data-ttu-id="16041-118">Condição</span><span class="sxs-lookup"><span data-stu-id="16041-118">Condition</span></span> | [<span data-ttu-id="16041-119">Condição</span><span class="sxs-lookup"><span data-stu-id="16041-119">Condition</span></span>](condition.md)   | <span data-ttu-id="16041-120">N</span><span class="sxs-lookup"><span data-stu-id="16041-120">N</span></span>   | <span data-ttu-id="16041-121">S</span><span class="sxs-lookup"><span data-stu-id="16041-121">Y</span></span>        |
| <span data-ttu-id="16041-122">Sequência</span><span class="sxs-lookup"><span data-stu-id="16041-122">Sequence</span></span>  | [<span data-ttu-id="16041-123">Inteiro</span><span class="sxs-lookup"><span data-stu-id="16041-123">Integer</span></span>](integer.md)       | <span data-ttu-id="16041-124">N</span><span class="sxs-lookup"><span data-stu-id="16041-124">N</span></span>   | <span data-ttu-id="16041-125">S</span><span class="sxs-lookup"><span data-stu-id="16041-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="16041-126">Colunas</span><span class="sxs-lookup"><span data-stu-id="16041-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="16041-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="16041-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="16041-128">Nome da ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="16041-128">Name of the action to execute.</span></span> <span data-ttu-id="16041-129">Essa é uma ação interna ou uma ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="16041-129">This is either a built-in action or a custom action.</span></span>

<span data-ttu-id="16041-130">Chave de tabela primária.</span><span class="sxs-lookup"><span data-stu-id="16041-130">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="16041-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="16041-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="16041-132">Este campo contém uma expressão condicional.</span><span class="sxs-lookup"><span data-stu-id="16041-132">This field contains a conditional expression.</span></span> <span data-ttu-id="16041-133">Se a expressão for avaliada como false, a ação será ignorada.</span><span class="sxs-lookup"><span data-stu-id="16041-133">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="16041-134">Se a sintaxe da expressão for inválida, a sequência será encerrada, retornando iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="16041-134">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="16041-135">Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="16041-135">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="16041-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem</span><span class="sxs-lookup"><span data-stu-id="16041-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="16041-137">Número que determina a posição da sequência em que essa ação deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="16041-137">Number that determines the sequence position in which this action is to be executed.</span></span>

<span data-ttu-id="16041-138">Um valor positivo representa a posição da sequência.</span><span class="sxs-lookup"><span data-stu-id="16041-138">A positive value represents the sequence position.</span></span> <span data-ttu-id="16041-139">Um valor nulo indica que a ação não é executada.</span><span class="sxs-lookup"><span data-stu-id="16041-139">A Null value indicates that the action is not executed.</span></span> <span data-ttu-id="16041-140">Os valores negativos a seguir indicam que essa ação deve ser executada se o instalador retornar o sinalizador de encerramento associado.</span><span class="sxs-lookup"><span data-stu-id="16041-140">The following negative values indicate that this action is to be executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="16041-141">Cada sinalizador de encerramento (valor negativo) pode ser usado com no máximo uma ação.</span><span class="sxs-lookup"><span data-stu-id="16041-141">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="16041-142">Várias ações podem ter sinalizadores de encerramento, mas devem ser sinalizadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="16041-142">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="16041-143">Os sinalizadores de término (valores negativos) normalmente são usados com [caixas de diálogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="16041-143">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="16041-144">Sinalizador de término</span><span class="sxs-lookup"><span data-stu-id="16041-144">Termination flag</span></span>          | <span data-ttu-id="16041-145">Valor</span><span class="sxs-lookup"><span data-stu-id="16041-145">Value</span></span> | <span data-ttu-id="16041-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="16041-146">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="16041-147">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="16041-147">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="16041-148">-1</span><span class="sxs-lookup"><span data-stu-id="16041-148">-1</span></span>    | <span data-ttu-id="16041-149">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="16041-149">Successful completion.</span></span> <span data-ttu-id="16041-150">Usado com as caixas de diálogo de [saída](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="16041-150">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="16041-151">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="16041-151">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="16041-152">-2</span><span class="sxs-lookup"><span data-stu-id="16041-152">-2</span></span>    | <span data-ttu-id="16041-153">O usuário encerra a instalação.</span><span class="sxs-lookup"><span data-stu-id="16041-153">User terminates install.</span></span> <span data-ttu-id="16041-154">Usado com caixas de diálogo [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="16041-154">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="16041-155">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="16041-155">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="16041-156">-3</span><span class="sxs-lookup"><span data-stu-id="16041-156">-3</span></span>    | <span data-ttu-id="16041-157">Encerramentos de saída fatais.</span><span class="sxs-lookup"><span data-stu-id="16041-157">Fatal exit terminates.</span></span> <span data-ttu-id="16041-158">Usado com caixas de diálogo [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="16041-158">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="16041-159">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="16041-159">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="16041-160">-4</span><span class="sxs-lookup"><span data-stu-id="16041-160">-4</span></span>    | <span data-ttu-id="16041-161">A instalação está suspensa.</span><span class="sxs-lookup"><span data-stu-id="16041-161">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="16041-162">Zero, todos os outros números negativos ou um valor nulo indicam que a ação nunca é executada.</span><span class="sxs-lookup"><span data-stu-id="16041-162">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16041-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="16041-163">Remarks</span></span>

<span data-ttu-id="16041-164">O texto localizado para exibição de progresso ou registro em log é especificado na [tabela ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="16041-164">Localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="16041-165">Para obter um exemplo de uma tabela de sequência, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="16041-165">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="16041-166">Validação</span><span class="sxs-lookup"><span data-stu-id="16041-166">Validation</span></span>

<dl>

[<span data-ttu-id="16041-167">ICE03</span><span class="sxs-lookup"><span data-stu-id="16041-167">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="16041-168">ICE06</span><span class="sxs-lookup"><span data-stu-id="16041-168">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="16041-169">ICE12</span><span class="sxs-lookup"><span data-stu-id="16041-169">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="16041-170">ICE13</span><span class="sxs-lookup"><span data-stu-id="16041-170">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="16041-171">ICE26</span><span class="sxs-lookup"><span data-stu-id="16041-171">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="16041-172">ICE27</span><span class="sxs-lookup"><span data-stu-id="16041-172">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="16041-173">ICE28</span><span class="sxs-lookup"><span data-stu-id="16041-173">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="16041-174">ICE46</span><span class="sxs-lookup"><span data-stu-id="16041-174">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="16041-175">ICE63</span><span class="sxs-lookup"><span data-stu-id="16041-175">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="16041-176">ICE75</span><span class="sxs-lookup"><span data-stu-id="16041-176">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="16041-177">ICE77</span><span class="sxs-lookup"><span data-stu-id="16041-177">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="16041-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="16041-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="16041-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="16041-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="16041-180">ICE83</span><span class="sxs-lookup"><span data-stu-id="16041-180">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="16041-181">ICE84</span><span class="sxs-lookup"><span data-stu-id="16041-181">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="16041-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="16041-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



