---
description: A tabela AdminExecuteSequence lista as ações que o instalador chama em sequência quando a ação de administrador de nível superior é executada.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: Tabela AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770387"
---
# <a name="adminexecutesequence-table"></a><span data-ttu-id="6db31-103">Tabela AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="6db31-103">AdminExecuteSequence Table</span></span>

<span data-ttu-id="6db31-104">A tabela AdminExecuteSequence lista as ações que o instalador chama em sequência quando a ação de [administrador](admin-action.md) de nível superior é executada.</span><span class="sxs-lookup"><span data-stu-id="6db31-104">The AdminExecuteSequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed.</span></span>

<span data-ttu-id="6db31-105">As ações de administrador na sequência de instalação, até a [ação InstallValidate](installvalidate-action.md) e todas as caixas de diálogo de saída, estão localizadas na [tabela AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="6db31-105">ADMIN actions in the install sequence, up to the [InstallValidate action](installvalidate-action.md) and any exit dialog boxes, are located in the [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="6db31-106">As ações de administrador da ação InstallValidate até o final da sequência de instalação estão na tabela AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="6db31-106">ADMIN actions from the InstallValidate action through the end of the install sequence are in the AdminExecuteSequence table.</span></span> <span data-ttu-id="6db31-107">Como a tabela AdminExecuteSequence precisa ser autônoma, ela também contém as ações de inicialização necessárias, como [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="6db31-107">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span>

<span data-ttu-id="6db31-108">As [ações personalizadas](custom-actions.md) que exigem uma interface do usuário devem usar [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) em vez de caixas de diálogo criadas usando a [tabela de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="6db31-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="6db31-109">As colunas são idênticas às da [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="6db31-109">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="6db31-110">A tabela AdminExecuteSequence tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6db31-110">The AdminExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="6db31-111">Coluna</span><span class="sxs-lookup"><span data-stu-id="6db31-111">Column</span></span>    | <span data-ttu-id="6db31-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="6db31-112">Type</span></span>                         | <span data-ttu-id="6db31-113">Chave</span><span class="sxs-lookup"><span data-stu-id="6db31-113">Key</span></span> | <span data-ttu-id="6db31-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="6db31-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="6db31-115">Ação</span><span class="sxs-lookup"><span data-stu-id="6db31-115">Action</span></span>    | [<span data-ttu-id="6db31-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="6db31-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="6db31-117">S</span><span class="sxs-lookup"><span data-stu-id="6db31-117">Y</span></span>   | <span data-ttu-id="6db31-118">N</span><span class="sxs-lookup"><span data-stu-id="6db31-118">N</span></span>        |
| <span data-ttu-id="6db31-119">Condição</span><span class="sxs-lookup"><span data-stu-id="6db31-119">Condition</span></span> | [<span data-ttu-id="6db31-120">Condição</span><span class="sxs-lookup"><span data-stu-id="6db31-120">Condition</span></span>](condition.md)   | <span data-ttu-id="6db31-121">N</span><span class="sxs-lookup"><span data-stu-id="6db31-121">N</span></span>   | <span data-ttu-id="6db31-122">S</span><span class="sxs-lookup"><span data-stu-id="6db31-122">Y</span></span>        |
| <span data-ttu-id="6db31-123">Sequência</span><span class="sxs-lookup"><span data-stu-id="6db31-123">Sequence</span></span>  | [<span data-ttu-id="6db31-124">Inteiro</span><span class="sxs-lookup"><span data-stu-id="6db31-124">Integer</span></span>](integer.md)       | <span data-ttu-id="6db31-125">N</span><span class="sxs-lookup"><span data-stu-id="6db31-125">N</span></span>   | <span data-ttu-id="6db31-126">S</span><span class="sxs-lookup"><span data-stu-id="6db31-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6db31-127">Colunas</span><span class="sxs-lookup"><span data-stu-id="6db31-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6db31-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="6db31-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="6db31-129">Nome da ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="6db31-129">Name of the action to execute.</span></span> <span data-ttu-id="6db31-130">Essa é uma ação padrão ou uma ação personalizada listada na [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="6db31-130">This is either a standard action or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="6db31-131">Chave de tabela primária.</span><span class="sxs-lookup"><span data-stu-id="6db31-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="6db31-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="6db31-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="6db31-133">Expressão lógica.</span><span class="sxs-lookup"><span data-stu-id="6db31-133">Logical expression.</span></span> <span data-ttu-id="6db31-134">Se a expressão for avaliada como false, a ação será ignorada.</span><span class="sxs-lookup"><span data-stu-id="6db31-134">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="6db31-135">Se a sintaxe da expressão for inválida, a sequência será encerrada, retornando iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="6db31-135">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="6db31-136">Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="6db31-136">For information on the syntax of conditional statements see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db31-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem</span><span class="sxs-lookup"><span data-stu-id="6db31-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="6db31-138">Um valor positivo indica a posição da sequência da ação.</span><span class="sxs-lookup"><span data-stu-id="6db31-138">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="6db31-139">Os valores negativos a seguir indicam que a ação será chamada se o instalador retornar o sinalizador de término.</span><span class="sxs-lookup"><span data-stu-id="6db31-139">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="6db31-140">Cada sinalizador de encerramento (valor negativo) pode ser usado com no máximo uma ação.</span><span class="sxs-lookup"><span data-stu-id="6db31-140">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="6db31-141">Várias ações podem ter sinalizadores de encerramento, mas devem ser sinalizadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="6db31-141">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="6db31-142">Os sinalizadores de término (valores negativos) normalmente são usados com [caixas de diálogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="6db31-142">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="6db31-143">Sinalizador de término</span><span class="sxs-lookup"><span data-stu-id="6db31-143">Termination flag</span></span>          | <span data-ttu-id="6db31-144">Valor</span><span class="sxs-lookup"><span data-stu-id="6db31-144">Value</span></span> | <span data-ttu-id="6db31-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="6db31-145">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6db31-146">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="6db31-146">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="6db31-147">-1</span><span class="sxs-lookup"><span data-stu-id="6db31-147">-1</span></span>    | <span data-ttu-id="6db31-148">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6db31-148">Successful completion.</span></span> <span data-ttu-id="6db31-149">Usado com as caixas de diálogo de [saída](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="6db31-149">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="6db31-150">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="6db31-150">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="6db31-151">-2</span><span class="sxs-lookup"><span data-stu-id="6db31-151">-2</span></span>    | <span data-ttu-id="6db31-152">O usuário encerra a instalação.</span><span class="sxs-lookup"><span data-stu-id="6db31-152">User terminates install.</span></span> <span data-ttu-id="6db31-153">Usado com caixas de diálogo [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="6db31-153">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="6db31-154">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="6db31-154">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="6db31-155">-3</span><span class="sxs-lookup"><span data-stu-id="6db31-155">-3</span></span>    | <span data-ttu-id="6db31-156">Encerramentos de saída fatais.</span><span class="sxs-lookup"><span data-stu-id="6db31-156">Fatal exit terminates.</span></span> <span data-ttu-id="6db31-157">Usado com caixas de diálogo [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="6db31-157">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="6db31-158">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="6db31-158">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="6db31-159">-4</span><span class="sxs-lookup"><span data-stu-id="6db31-159">-4</span></span>    | <span data-ttu-id="6db31-160">A instalação está suspensa.</span><span class="sxs-lookup"><span data-stu-id="6db31-160">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="6db31-161">Zero, todos os outros números negativos ou um valor nulo indicam que a ação nunca é chamada.</span><span class="sxs-lookup"><span data-stu-id="6db31-161">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="6db31-162">Validação</span><span class="sxs-lookup"><span data-stu-id="6db31-162">Validation</span></span>

<dl>

[<span data-ttu-id="6db31-163">ICE03</span><span class="sxs-lookup"><span data-stu-id="6db31-163">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6db31-164">ICE06</span><span class="sxs-lookup"><span data-stu-id="6db31-164">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6db31-165">ICE12</span><span class="sxs-lookup"><span data-stu-id="6db31-165">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="6db31-166">ICE13</span><span class="sxs-lookup"><span data-stu-id="6db31-166">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="6db31-167">ICE26</span><span class="sxs-lookup"><span data-stu-id="6db31-167">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="6db31-168">ICE27</span><span class="sxs-lookup"><span data-stu-id="6db31-168">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="6db31-169">ICE28</span><span class="sxs-lookup"><span data-stu-id="6db31-169">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="6db31-170">ICE75</span><span class="sxs-lookup"><span data-stu-id="6db31-170">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="6db31-171">ICE77</span><span class="sxs-lookup"><span data-stu-id="6db31-171">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="6db31-172">ICE79</span><span class="sxs-lookup"><span data-stu-id="6db31-172">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="6db31-173">ICE82</span><span class="sxs-lookup"><span data-stu-id="6db31-173">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="6db31-174">ICE84</span><span class="sxs-lookup"><span data-stu-id="6db31-174">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="6db31-175">ICE86</span><span class="sxs-lookup"><span data-stu-id="6db31-175">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="6db31-176">ICEM04</span><span class="sxs-lookup"><span data-stu-id="6db31-176">ICEM04</span></span>](icem04.md)  
</dl>

 

 



