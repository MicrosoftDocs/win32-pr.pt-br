---
description: A tabela AdvtExecuteSequence lista ações que o instalador chama quando a ação de notificação de nível superior é executada.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: Tabela AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b68a3f69cc7473b2364f169545743941d752f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828082"
---
# <a name="advtexecutesequence-table"></a><span data-ttu-id="c9268-103">Tabela AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="c9268-103">AdvtExecuteSequence Table</span></span>

<span data-ttu-id="c9268-104">A tabela AdvtExecuteSequence lista ações que o instalador chama quando a ação de [notificação](advertise-action.md) de nível superior é executada.</span><span class="sxs-lookup"><span data-stu-id="c9268-104">The AdvtExecuteSequence table lists actions the installer calls when the top-level [ADVERTISE action](advertise-action.md) is executed.</span></span>

<span data-ttu-id="c9268-105">Somente as ações a seguir podem ser usadas na tabela AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="c9268-105">Only the following actions can be used in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="c9268-106">Não é possível usar ações personalizadas nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="c9268-106">Custom actions cannot be used in this table.</span></span>

[<span data-ttu-id="c9268-107">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="c9268-107">CostFinalize</span></span>](costfinalize-action.md)

[<span data-ttu-id="c9268-108">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="c9268-108">CostInitialize</span></span>](costinitialize-action.md)

[<span data-ttu-id="c9268-109">Createatalhos</span><span class="sxs-lookup"><span data-stu-id="c9268-109">CreateShortcuts</span></span>](createshortcuts-action.md)

[<span data-ttu-id="c9268-110">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="c9268-110">InstallFinalize</span></span>](installfinalize-action.md)

[<span data-ttu-id="c9268-111">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="c9268-111">InstallInitialize</span></span>](installinitialize-action.md)

[<span data-ttu-id="c9268-112">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="c9268-112">InstallValidate</span></span>](installvalidate-action.md)

[<span data-ttu-id="c9268-113">MsiPublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="c9268-113">MsiPublishAssemblies</span></span>](msipublishassemblies-action.md)

[<span data-ttu-id="c9268-114">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="c9268-114">PublishComponents</span></span>](publishcomponents-action.md)

[<span data-ttu-id="c9268-115">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="c9268-115">PublishFeatures</span></span>](publishfeatures-action.md)

[<span data-ttu-id="c9268-116">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="c9268-116">PublishProduct</span></span>](publishproduct-action.md)

[<span data-ttu-id="c9268-117">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="c9268-117">RegisterClassInfo</span></span>](registerclassinfo-action.md)

[<span data-ttu-id="c9268-118">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="c9268-118">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)

[<span data-ttu-id="c9268-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="c9268-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

[<span data-ttu-id="c9268-120">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="c9268-120">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="c9268-121">As colunas são idênticas às da [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="c9268-121">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="c9268-122">A tabela AdvtExecuteSequence tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9268-122">The AdvtExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="c9268-123">Coluna</span><span class="sxs-lookup"><span data-stu-id="c9268-123">Column</span></span>    | <span data-ttu-id="c9268-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9268-124">Type</span></span>                         | <span data-ttu-id="c9268-125">Chave</span><span class="sxs-lookup"><span data-stu-id="c9268-125">Key</span></span> | <span data-ttu-id="c9268-126">Nullable</span><span class="sxs-lookup"><span data-stu-id="c9268-126">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="c9268-127">Ação</span><span class="sxs-lookup"><span data-stu-id="c9268-127">Action</span></span>    | [<span data-ttu-id="c9268-128">Identificador</span><span class="sxs-lookup"><span data-stu-id="c9268-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="c9268-129">S</span><span class="sxs-lookup"><span data-stu-id="c9268-129">Y</span></span>   | <span data-ttu-id="c9268-130">N</span><span class="sxs-lookup"><span data-stu-id="c9268-130">N</span></span>        |
| <span data-ttu-id="c9268-131">Condição</span><span class="sxs-lookup"><span data-stu-id="c9268-131">Condition</span></span> | [<span data-ttu-id="c9268-132">Condição</span><span class="sxs-lookup"><span data-stu-id="c9268-132">Condition</span></span>](condition.md)   | <span data-ttu-id="c9268-133">N</span><span class="sxs-lookup"><span data-stu-id="c9268-133">N</span></span>   | <span data-ttu-id="c9268-134">S</span><span class="sxs-lookup"><span data-stu-id="c9268-134">Y</span></span>        |
| <span data-ttu-id="c9268-135">Sequência</span><span class="sxs-lookup"><span data-stu-id="c9268-135">Sequence</span></span>  | [<span data-ttu-id="c9268-136">Inteiro</span><span class="sxs-lookup"><span data-stu-id="c9268-136">Integer</span></span>](integer.md)       | <span data-ttu-id="c9268-137">N</span><span class="sxs-lookup"><span data-stu-id="c9268-137">N</span></span>   | <span data-ttu-id="c9268-138">S</span><span class="sxs-lookup"><span data-stu-id="c9268-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c9268-139">Colunas</span><span class="sxs-lookup"><span data-stu-id="c9268-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c9268-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="c9268-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="c9268-141">Nome da [ação padrão](standard-actions.md) que o instalador deve executar.</span><span class="sxs-lookup"><span data-stu-id="c9268-141">Name of the [standard action](standard-actions.md) the installer is to execute.</span></span> <span data-ttu-id="c9268-142">Esta é a chave primária da tabela.</span><span class="sxs-lookup"><span data-stu-id="c9268-142">This is the primary key of the table.</span></span>

</dd> <dt>

<span data-ttu-id="c9268-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="c9268-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="c9268-144">Expressão lógica.</span><span class="sxs-lookup"><span data-stu-id="c9268-144">Logical expression.</span></span> <span data-ttu-id="c9268-145">Se a expressão for avaliada como false, a ação será ignorada.</span><span class="sxs-lookup"><span data-stu-id="c9268-145">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="c9268-146">Se a sintaxe da expressão for inválida, a sequência será encerrada, retornando iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="c9268-146">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="c9268-147">Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="c9268-147">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9268-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem</span><span class="sxs-lookup"><span data-stu-id="c9268-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="c9268-149">Um valor positivo indica a posição da sequência da ação.</span><span class="sxs-lookup"><span data-stu-id="c9268-149">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="c9268-150">Os valores negativos a seguir indicam que a ação será chamada se o instalador retornar o sinalizador de término.</span><span class="sxs-lookup"><span data-stu-id="c9268-150">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="c9268-151">Cada sinalizador de encerramento (valor negativo) pode ser usado com no máximo uma ação.</span><span class="sxs-lookup"><span data-stu-id="c9268-151">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="c9268-152">Várias ações podem ter sinalizadores de encerramento, mas devem ser sinalizadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="c9268-152">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="c9268-153">Os sinalizadores de término (valores negativos) normalmente são usados com [caixas de diálogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="c9268-153">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="c9268-154">Sinalizador de término</span><span class="sxs-lookup"><span data-stu-id="c9268-154">Termination flag</span></span>          | <span data-ttu-id="c9268-155">Valor</span><span class="sxs-lookup"><span data-stu-id="c9268-155">Value</span></span> | <span data-ttu-id="c9268-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9268-156">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c9268-157">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="c9268-157">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="c9268-158">-1</span><span class="sxs-lookup"><span data-stu-id="c9268-158">-1</span></span>    | <span data-ttu-id="c9268-159">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c9268-159">Successful completion.</span></span> <span data-ttu-id="c9268-160">Usado com as caixas de diálogo de [saída](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="c9268-160">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="c9268-161">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="c9268-161">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="c9268-162">-2</span><span class="sxs-lookup"><span data-stu-id="c9268-162">-2</span></span>    | <span data-ttu-id="c9268-163">O usuário encerra a instalação.</span><span class="sxs-lookup"><span data-stu-id="c9268-163">User terminates install.</span></span> <span data-ttu-id="c9268-164">Usado com caixas de diálogo [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="c9268-164">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="c9268-165">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="c9268-165">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="c9268-166">-3</span><span class="sxs-lookup"><span data-stu-id="c9268-166">-3</span></span>    | <span data-ttu-id="c9268-167">Encerramentos de saída fatais.</span><span class="sxs-lookup"><span data-stu-id="c9268-167">Fatal exit terminates.</span></span> <span data-ttu-id="c9268-168">Usado com caixas de diálogo [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="c9268-168">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="c9268-169">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="c9268-169">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="c9268-170">-4</span><span class="sxs-lookup"><span data-stu-id="c9268-170">-4</span></span>    | <span data-ttu-id="c9268-171">A instalação está suspensa.</span><span class="sxs-lookup"><span data-stu-id="c9268-171">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="c9268-172">Zero, todos os outros números negativos ou um valor nulo indicam que a ação nunca é chamada.</span><span class="sxs-lookup"><span data-stu-id="c9268-172">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="c9268-173">Validação</span><span class="sxs-lookup"><span data-stu-id="c9268-173">Validation</span></span>

<dl>

[<span data-ttu-id="c9268-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="c9268-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c9268-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="c9268-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c9268-176">ICE12</span><span class="sxs-lookup"><span data-stu-id="c9268-176">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="c9268-177">ICE13</span><span class="sxs-lookup"><span data-stu-id="c9268-177">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="c9268-178">ICE27</span><span class="sxs-lookup"><span data-stu-id="c9268-178">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="c9268-179">ICE46</span><span class="sxs-lookup"><span data-stu-id="c9268-179">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="c9268-180">ICE72</span><span class="sxs-lookup"><span data-stu-id="c9268-180">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="c9268-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="c9268-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="c9268-182">ICE82</span><span class="sxs-lookup"><span data-stu-id="c9268-182">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="c9268-183">ICE83</span><span class="sxs-lookup"><span data-stu-id="c9268-183">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="c9268-184">ICE84</span><span class="sxs-lookup"><span data-stu-id="c9268-184">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="c9268-185">ICE86</span><span class="sxs-lookup"><span data-stu-id="c9268-185">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="c9268-186">ICEM04</span><span class="sxs-lookup"><span data-stu-id="c9268-186">ICEM04</span></span>](icem04.md)  
</dl>

 

 



