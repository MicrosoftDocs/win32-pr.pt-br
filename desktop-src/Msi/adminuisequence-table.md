---
description: A tabela AdminUISequence lista as ações que o instalador chama em sequência quando a ação de administrador de nível superior é executada e o nível da interface do usuário interna é definido como interface de usuários completa ou redução da IU.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: Tabela AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8fb460f65d223e75ebd50a7587f5b3f4adeced8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748169"
---
# <a name="adminuisequence-table"></a><span data-ttu-id="d53f3-103">Tabela AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="d53f3-103">AdminUISequence Table</span></span>

<span data-ttu-id="d53f3-104">A tabela AdminUISequence lista as ações que o instalador chama em sequência quando a ação de [administrador](admin-action.md) de nível superior é executada e o nível da interface do usuário interna é definido como interface de usuários completa ou redução da IU.</span><span class="sxs-lookup"><span data-stu-id="d53f3-104">The AdminUISequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="d53f3-105">O instalador ignorará as ações nesta tabela se o nível da interface do usuário estiver definido como interface básica ou não.</span><span class="sxs-lookup"><span data-stu-id="d53f3-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="d53f3-106">Consulte [sobre a interface do usuário](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="d53f3-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="d53f3-107">As ações de administrador na sequência de instalação até a [ação InstallValidate](installvalidate-action.md)e todas as caixas de diálogo de saída estão localizadas na tabela AdminUISequence.</span><span class="sxs-lookup"><span data-stu-id="d53f3-107">ADMIN actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the AdminUISequence table.</span></span> <span data-ttu-id="d53f3-108">Todas as ações do InstallValidate até o final da sequência de instalação estão na [tabela AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="d53f3-108">All actions from the InstallValidate through the end of the install sequence are in the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="d53f3-109">Como a tabela AdminExecuteSequence precisa ser autônoma, ela também contém as ações de inicialização necessárias, como [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="d53f3-109">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span> <span data-ttu-id="d53f3-110">Ele também tem a [ação ExecuteAction](executeaction-action.md).</span><span class="sxs-lookup"><span data-stu-id="d53f3-110">It also has the [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="d53f3-111">As colunas são idênticas às da [tabela InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="d53f3-111">The columns are identical to those of the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="d53f3-112">A tabela AdminUISequence tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d53f3-112">The AdminUISequence table has the following columns.</span></span>



| <span data-ttu-id="d53f3-113">Coluna</span><span class="sxs-lookup"><span data-stu-id="d53f3-113">Column</span></span>    | <span data-ttu-id="d53f3-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="d53f3-114">Type</span></span>                         | <span data-ttu-id="d53f3-115">Chave</span><span class="sxs-lookup"><span data-stu-id="d53f3-115">Key</span></span> | <span data-ttu-id="d53f3-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="d53f3-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="d53f3-117">Ação</span><span class="sxs-lookup"><span data-stu-id="d53f3-117">Action</span></span>    | [<span data-ttu-id="d53f3-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="d53f3-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="d53f3-119">S</span><span class="sxs-lookup"><span data-stu-id="d53f3-119">Y</span></span>   | <span data-ttu-id="d53f3-120">N</span><span class="sxs-lookup"><span data-stu-id="d53f3-120">N</span></span>        |
| <span data-ttu-id="d53f3-121">Condição</span><span class="sxs-lookup"><span data-stu-id="d53f3-121">Condition</span></span> | [<span data-ttu-id="d53f3-122">Condição</span><span class="sxs-lookup"><span data-stu-id="d53f3-122">Condition</span></span>](condition.md)   | <span data-ttu-id="d53f3-123">N</span><span class="sxs-lookup"><span data-stu-id="d53f3-123">N</span></span>   | <span data-ttu-id="d53f3-124">S</span><span class="sxs-lookup"><span data-stu-id="d53f3-124">Y</span></span>        |
| <span data-ttu-id="d53f3-125">Sequência</span><span class="sxs-lookup"><span data-stu-id="d53f3-125">Sequence</span></span>  | [<span data-ttu-id="d53f3-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="d53f3-126">Integer</span></span>](integer.md)       | <span data-ttu-id="d53f3-127">N</span><span class="sxs-lookup"><span data-stu-id="d53f3-127">N</span></span>   | <span data-ttu-id="d53f3-128">S</span><span class="sxs-lookup"><span data-stu-id="d53f3-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d53f3-129">Colunas</span><span class="sxs-lookup"><span data-stu-id="d53f3-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d53f3-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="d53f3-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="d53f3-131">Nome da ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="d53f3-131">Name of the action to execute.</span></span> <span data-ttu-id="d53f3-132">Essa é uma ação padrão, um assistente de interface do usuário ou uma ação personalizada listada na [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="d53f3-132">This is either a standard action, a user interface wizard, or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="d53f3-133">Chave de tabela primária.</span><span class="sxs-lookup"><span data-stu-id="d53f3-133">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="d53f3-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="d53f3-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="d53f3-135">Expressão lógica.</span><span class="sxs-lookup"><span data-stu-id="d53f3-135">Logical expression.</span></span> <span data-ttu-id="d53f3-136">Se a expressão for avaliada como false, a ação será ignorada.</span><span class="sxs-lookup"><span data-stu-id="d53f3-136">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="d53f3-137">Se a sintaxe da expressão for inválida, a sequência será encerrada, retornando iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="d53f3-137">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="d53f3-138">Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="d53f3-138">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="d53f3-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem</span><span class="sxs-lookup"><span data-stu-id="d53f3-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="d53f3-140">Um valor positivo indica a posição da sequência da ação.</span><span class="sxs-lookup"><span data-stu-id="d53f3-140">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="d53f3-141">Os valores negativos a seguir indicam que a ação será chamada se o instalador retornar o sinalizador de término.</span><span class="sxs-lookup"><span data-stu-id="d53f3-141">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="d53f3-142">Cada sinalizador de encerramento (valor negativo) pode ser usado com no máximo uma ação.</span><span class="sxs-lookup"><span data-stu-id="d53f3-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="d53f3-143">Várias ações podem ter sinalizadores de encerramento, mas devem ser sinalizadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="d53f3-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="d53f3-144">Os sinalizadores de término (valores negativos) normalmente são usados com [caixas de diálogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="d53f3-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="d53f3-145">Sinalizador de término</span><span class="sxs-lookup"><span data-stu-id="d53f3-145">Termination flag</span></span>          | <span data-ttu-id="d53f3-146">Valor</span><span class="sxs-lookup"><span data-stu-id="d53f3-146">Value</span></span> | <span data-ttu-id="d53f3-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="d53f3-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d53f3-148">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="d53f3-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="d53f3-149">-1</span><span class="sxs-lookup"><span data-stu-id="d53f3-149">-1</span></span>    | <span data-ttu-id="d53f3-150">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d53f3-150">Successful completion.</span></span> <span data-ttu-id="d53f3-151">Usado com as caixas de diálogo de [saída](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="d53f3-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="d53f3-152">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="d53f3-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="d53f3-153">-2</span><span class="sxs-lookup"><span data-stu-id="d53f3-153">-2</span></span>    | <span data-ttu-id="d53f3-154">O usuário encerra a instalação.</span><span class="sxs-lookup"><span data-stu-id="d53f3-154">User terminates install.</span></span> <span data-ttu-id="d53f3-155">Usado com caixas de diálogo [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="d53f3-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="d53f3-156">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="d53f3-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="d53f3-157">-3</span><span class="sxs-lookup"><span data-stu-id="d53f3-157">-3</span></span>    | <span data-ttu-id="d53f3-158">Encerramentos de saída fatais.</span><span class="sxs-lookup"><span data-stu-id="d53f3-158">Fatal exit terminates.</span></span> <span data-ttu-id="d53f3-159">Usado com caixas de diálogo [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="d53f3-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="d53f3-160">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="d53f3-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="d53f3-161">-4</span><span class="sxs-lookup"><span data-stu-id="d53f3-161">-4</span></span>    | <span data-ttu-id="d53f3-162">A instalação está suspensa.</span><span class="sxs-lookup"><span data-stu-id="d53f3-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="d53f3-163">Zero, todos os outros números negativos ou um valor nulo indicam que a ação nunca é chamada.</span><span class="sxs-lookup"><span data-stu-id="d53f3-163">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="d53f3-164">Validação</span><span class="sxs-lookup"><span data-stu-id="d53f3-164">Validation</span></span>

<dl>

[<span data-ttu-id="d53f3-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="d53f3-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d53f3-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="d53f3-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d53f3-167">ICE12</span><span class="sxs-lookup"><span data-stu-id="d53f3-167">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="d53f3-168">ICE13</span><span class="sxs-lookup"><span data-stu-id="d53f3-168">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="d53f3-169">ICE20</span><span class="sxs-lookup"><span data-stu-id="d53f3-169">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="d53f3-170">ICE26</span><span class="sxs-lookup"><span data-stu-id="d53f3-170">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="d53f3-171">ICE27</span><span class="sxs-lookup"><span data-stu-id="d53f3-171">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="d53f3-172">ICE28</span><span class="sxs-lookup"><span data-stu-id="d53f3-172">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="d53f3-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="d53f3-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="d53f3-174">ICE75</span><span class="sxs-lookup"><span data-stu-id="d53f3-174">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="d53f3-175">ICE79</span><span class="sxs-lookup"><span data-stu-id="d53f3-175">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="d53f3-176">ICE82</span><span class="sxs-lookup"><span data-stu-id="d53f3-176">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="d53f3-177">ICE84</span><span class="sxs-lookup"><span data-stu-id="d53f3-177">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="d53f3-178">ICE86</span><span class="sxs-lookup"><span data-stu-id="d53f3-178">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="d53f3-179">ICE96</span><span class="sxs-lookup"><span data-stu-id="d53f3-179">ICE96</span></span>](ice96.md)  
[<span data-ttu-id="d53f3-180">ICEM04</span><span class="sxs-lookup"><span data-stu-id="d53f3-180">ICEM04</span></span>](icem04.md)  
</dl>

 

 



