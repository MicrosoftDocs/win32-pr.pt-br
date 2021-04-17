---
description: A tabela InstallUISequence lista as ações que são executadas quando a ação de instalação de nível superior é executada e o nível de interface do usuário interno é definido como interface de usuários completa ou interface reduzida.
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: Tabela InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a4d8d3033645ac1f414e3aff67be2a26d7a6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787082"
---
# <a name="installuisequence-table"></a><span data-ttu-id="ab5b2-103">Tabela InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="ab5b2-103">InstallUISequence Table</span></span>

<span data-ttu-id="ab5b2-104">A tabela InstallUISequence lista as ações que são executadas quando a ação de [instalação](install-action.md) de nível superior é executada e o nível de interface do usuário interno é definido como interface de usuários completa ou interface reduzida.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-104">The InstallUISequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="ab5b2-105">O instalador ignorará as ações nesta tabela se o nível da interface do usuário estiver definido como interface básica ou não.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="ab5b2-106">Consulte [sobre a interface do usuário](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="ab5b2-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="ab5b2-107">As ações na sequência de instalação até a [ação InstallValidate](installvalidate-action.md)e as caixas de diálogo de saída estão localizadas na tabela InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-107">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and the exit dialog boxes, are located in the InstallUISequence table.</span></span> <span data-ttu-id="ab5b2-108">Todas as ações do InstallValidate até o final da sequência de instalação estão na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab5b2-108">All actions from the InstallValidate through the end of the install sequence are in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="ab5b2-109">Como a tabela InstallExecuteSequence precisa ser autônoma, ela tem todas as ações de inicialização necessárias, como a ação [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [Filecost](filecost-action.md)e [CostFinalize](costfinalize-action.md)e [ExecuteAction](executeaction-action.md).</span><span class="sxs-lookup"><span data-stu-id="ab5b2-109">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and the [CostFinalize](costfinalize-action.md), and [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="ab5b2-110">A tabela InstallUISequence tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-110">The InstallUISequence table has the following columns.</span></span>



| <span data-ttu-id="ab5b2-111">Coluna</span><span class="sxs-lookup"><span data-stu-id="ab5b2-111">Column</span></span>    | <span data-ttu-id="ab5b2-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab5b2-112">Type</span></span>                         | <span data-ttu-id="ab5b2-113">Chave</span><span class="sxs-lookup"><span data-stu-id="ab5b2-113">Key</span></span> | <span data-ttu-id="ab5b2-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="ab5b2-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="ab5b2-115">Ação</span><span class="sxs-lookup"><span data-stu-id="ab5b2-115">Action</span></span>    | [<span data-ttu-id="ab5b2-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="ab5b2-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="ab5b2-117">S</span><span class="sxs-lookup"><span data-stu-id="ab5b2-117">Y</span></span>   | <span data-ttu-id="ab5b2-118">N</span><span class="sxs-lookup"><span data-stu-id="ab5b2-118">N</span></span>        |
| <span data-ttu-id="ab5b2-119">Condição</span><span class="sxs-lookup"><span data-stu-id="ab5b2-119">Condition</span></span> | [<span data-ttu-id="ab5b2-120">Condição</span><span class="sxs-lookup"><span data-stu-id="ab5b2-120">Condition</span></span>](condition.md)   | <span data-ttu-id="ab5b2-121">N</span><span class="sxs-lookup"><span data-stu-id="ab5b2-121">N</span></span>   | <span data-ttu-id="ab5b2-122">S</span><span class="sxs-lookup"><span data-stu-id="ab5b2-122">Y</span></span>        |
| <span data-ttu-id="ab5b2-123">Sequência</span><span class="sxs-lookup"><span data-stu-id="ab5b2-123">Sequence</span></span>  | [<span data-ttu-id="ab5b2-124">Inteiro</span><span class="sxs-lookup"><span data-stu-id="ab5b2-124">Integer</span></span>](integer.md)       | <span data-ttu-id="ab5b2-125">N</span><span class="sxs-lookup"><span data-stu-id="ab5b2-125">N</span></span>   | <span data-ttu-id="ab5b2-126">S</span><span class="sxs-lookup"><span data-stu-id="ab5b2-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ab5b2-127">Colunas</span><span class="sxs-lookup"><span data-stu-id="ab5b2-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ab5b2-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="ab5b2-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="ab5b2-129">Nome da ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-129">Name of the action to execute.</span></span> <span data-ttu-id="ab5b2-130">Essa é uma ação interna, uma ação personalizada ou um assistente de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-130">This is either a built-in action, a custom action, or a user interface wizard.</span></span>

<span data-ttu-id="ab5b2-131">Chave de tabela primária.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="ab5b2-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="ab5b2-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="ab5b2-133">Este campo contém uma expressão condicional.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-133">This field contains a conditional expression.</span></span> <span data-ttu-id="ab5b2-134">Se a expressão for avaliada como false, a ação será ignorada.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-134">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="ab5b2-135">Se a sintaxe da expressão for inválida, a sequência será encerrada, retornando iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-135">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="ab5b2-136">Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="ab5b2-136">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab5b2-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem</span><span class="sxs-lookup"><span data-stu-id="ab5b2-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="ab5b2-138">O número nesta coluna determina a posição da sequência em que essa ação é executada.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-138">The number in this column determines the sequence position in which this action is run.</span></span>

<span data-ttu-id="ab5b2-139">Um valor positivo representa a posição da sequência.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-139">A positive value represents the sequence position.</span></span> <span data-ttu-id="ab5b2-140">Um valor nulo indica que a ação nunca é executada.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-140">A Null value indicates that the action is never run.</span></span> <span data-ttu-id="ab5b2-141">Os valores negativos a seguir indicam que essa ação será executada se o instalador retornar o sinalizador de encerramento associado.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-141">The following negative values indicate that this action is executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="ab5b2-142">Cada sinalizador de encerramento (valor negativo) pode ser usado com no máximo uma ação.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="ab5b2-143">Várias ações podem ter sinalizadores de encerramento, mas devem ser sinalizadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="ab5b2-144">Os sinalizadores de término (valores negativos) normalmente são usados com [caixas de diálogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="ab5b2-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="ab5b2-145">Sinalizador de término</span><span class="sxs-lookup"><span data-stu-id="ab5b2-145">Termination flag</span></span>          | <span data-ttu-id="ab5b2-146">Valor</span><span class="sxs-lookup"><span data-stu-id="ab5b2-146">Value</span></span> | <span data-ttu-id="ab5b2-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab5b2-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ab5b2-148">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="ab5b2-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="ab5b2-149">-1</span><span class="sxs-lookup"><span data-stu-id="ab5b2-149">-1</span></span>    | <span data-ttu-id="ab5b2-150">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-150">Successful completion.</span></span> <span data-ttu-id="ab5b2-151">Usado com as caixas de diálogo de [saída](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="ab5b2-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="ab5b2-152">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="ab5b2-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="ab5b2-153">-2</span><span class="sxs-lookup"><span data-stu-id="ab5b2-153">-2</span></span>    | <span data-ttu-id="ab5b2-154">O usuário encerra a instalação.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-154">User terminates install.</span></span> <span data-ttu-id="ab5b2-155">Usado com caixas de diálogo [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="ab5b2-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="ab5b2-156">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="ab5b2-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="ab5b2-157">-3</span><span class="sxs-lookup"><span data-stu-id="ab5b2-157">-3</span></span>    | <span data-ttu-id="ab5b2-158">Encerramentos de saída fatais.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-158">Fatal exit terminates.</span></span> <span data-ttu-id="ab5b2-159">Usado com caixas de diálogo [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="ab5b2-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="ab5b2-160">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="ab5b2-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="ab5b2-161">-4</span><span class="sxs-lookup"><span data-stu-id="ab5b2-161">-4</span></span>    | <span data-ttu-id="ab5b2-162">A instalação está suspensa.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="ab5b2-163">Zero, todos os outros números negativos ou um valor nulo indicam que a ação nunca é executada.</span><span class="sxs-lookup"><span data-stu-id="ab5b2-163">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab5b2-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab5b2-164">Remarks</span></span>

<span data-ttu-id="ab5b2-165">O texto localizado associado para exibição de progresso ou registro em log está especificado na [tabela ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab5b2-165">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="ab5b2-166">Para obter um exemplo de uma tabela de sequência, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab5b2-166">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="ab5b2-167">Validação</span><span class="sxs-lookup"><span data-stu-id="ab5b2-167">Validation</span></span>

<dl>

[<span data-ttu-id="ab5b2-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="ab5b2-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ab5b2-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="ab5b2-169">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ab5b2-170">ICE12</span><span class="sxs-lookup"><span data-stu-id="ab5b2-170">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="ab5b2-171">ICE13</span><span class="sxs-lookup"><span data-stu-id="ab5b2-171">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="ab5b2-172">ICE20</span><span class="sxs-lookup"><span data-stu-id="ab5b2-172">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="ab5b2-173">ICE26</span><span class="sxs-lookup"><span data-stu-id="ab5b2-173">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="ab5b2-174">ICE27</span><span class="sxs-lookup"><span data-stu-id="ab5b2-174">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="ab5b2-175">ICE28</span><span class="sxs-lookup"><span data-stu-id="ab5b2-175">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="ab5b2-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="ab5b2-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="ab5b2-177">ICE75</span><span class="sxs-lookup"><span data-stu-id="ab5b2-177">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="ab5b2-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="ab5b2-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="ab5b2-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="ab5b2-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="ab5b2-180">ICE86</span><span class="sxs-lookup"><span data-stu-id="ab5b2-180">ICE86</span></span>](ice86.md)  
</dl>

 

 



