---
description: ICEM12 verifica que, em uma tabela ModuleSequence, as ações padrão têm números de sequência e as ações personalizadas têm os valores Baseaction e After.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010630"
---
# <a name="icem12"></a><span data-ttu-id="6a371-103">ICEM12</span><span class="sxs-lookup"><span data-stu-id="6a371-103">ICEM12</span></span>

<span data-ttu-id="6a371-104">ICEM12 verifica que, em uma tabela ModuleSequence, as ações padrão têm números de sequência e as ações personalizadas têm os valores Baseaction e After.</span><span class="sxs-lookup"><span data-stu-id="6a371-104">ICEM12 verifies that in a ModuleSequence table, standard actions have sequence numbers and custom actions have BaseAction and After values.</span></span>

<span data-ttu-id="6a371-105">Esse ICEM está disponível no arquivo Mergemod. Cub fornecido no SDK do Windows Installer 2,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="6a371-105">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="6a371-106">Para obter detalhes, consulte [SDK do Windows components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="6a371-106">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="6a371-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="6a371-107">Result</span></span>

<span data-ttu-id="6a371-108">ICEM12 posta um erro nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="6a371-108">ICEM12 posts an error in the following cases:</span></span>

-   <span data-ttu-id="6a371-109">Ele descobre que o módulo contém uma [ação padrão](standard-actions.md) sem um número de sequência.</span><span class="sxs-lookup"><span data-stu-id="6a371-109">It finds the module contains a [standard action](standard-actions.md) without a sequence number.</span></span>
-   <span data-ttu-id="6a371-110">Ele descobre que uma ação padrão tem valores inseridos nos campos Baseaction ou After da [tabela ModuleAdminUISequence](moduleadminuisequence-table.md), [tabela ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), tabela [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), tabela [ModuleInstallUISequence](moduleinstalluisequence-table.md)ou [tabela ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="6a371-110">It finds that a standard action has values entered in the BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>
-   <span data-ttu-id="6a371-111">Ele descobre que o módulo contém uma [ação personalizada](custom-actions.md) sem quaisquer valores inseridos nos campos Sequence, baseaction ou After da [tabela ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), tabela [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), tabela [ModuleInstallUISequence](moduleinstalluisequence-table.md)ou [tabela ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="6a371-111">It finds the module contains a [custom action](custom-actions.md) without any values entered into the Sequence, BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>

<span data-ttu-id="6a371-112">ICEM12 lançará um aviso se encontrar uma ação personalizada que tenha um número de sequência especificado, mas nenhum valor nos campos Baseaction ou After.</span><span class="sxs-lookup"><span data-stu-id="6a371-112">ICEM12 posts a warning if it finds a custom action that has a Sequence number specified, but no value in the BaseAction or After fields.</span></span>

<span data-ttu-id="6a371-113">Observe que todas as ações encontradas na [tabela CustomAction](customaction-table.md) são consideradas ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6a371-113">Note that all actions found in the [CustomAction table](customaction-table.md) are considered custom actions.</span></span> <span data-ttu-id="6a371-114">Todas as outras ações são consideradas ações padrão.</span><span class="sxs-lookup"><span data-stu-id="6a371-114">All other action are considered standard actions.</span></span>

## <a name="example"></a><span data-ttu-id="6a371-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6a371-115">Example</span></span>

<span data-ttu-id="6a371-116">ICEM12 posta as mensagens de erro e de aviso a seguir para um módulo que contém as entradas de banco de dados mostradas abaixo:</span><span class="sxs-lookup"><span data-stu-id="6a371-116">ICEM12 posts the following error and warning messages for a module that contains the database entries shown below:</span></span>

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[<span data-ttu-id="6a371-117">CustomAction</span><span class="sxs-lookup"><span data-stu-id="6a371-117">CustomAction</span></span>](customaction-table.md)



| <span data-ttu-id="6a371-118">Ação</span><span class="sxs-lookup"><span data-stu-id="6a371-118">Action</span></span>  | <span data-ttu-id="6a371-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a371-119">Type</span></span> | <span data-ttu-id="6a371-120">Fonte</span><span class="sxs-lookup"><span data-stu-id="6a371-120">Source</span></span>  | <span data-ttu-id="6a371-121">Destino</span><span class="sxs-lookup"><span data-stu-id="6a371-121">Target</span></span>  |
|---------|------|---------|---------|
| <span data-ttu-id="6a371-122">Action1</span><span class="sxs-lookup"><span data-stu-id="6a371-122">Action1</span></span> | <span data-ttu-id="6a371-123">30</span><span class="sxs-lookup"><span data-stu-id="6a371-123">30</span></span>   | <span data-ttu-id="6a371-124">origem1</span><span class="sxs-lookup"><span data-stu-id="6a371-124">source1</span></span> | <span data-ttu-id="6a371-125">target1</span><span class="sxs-lookup"><span data-stu-id="6a371-125">target1</span></span> |
| <span data-ttu-id="6a371-126">Action3</span><span class="sxs-lookup"><span data-stu-id="6a371-126">Action3</span></span> | <span data-ttu-id="6a371-127">30</span><span class="sxs-lookup"><span data-stu-id="6a371-127">30</span></span>   | <span data-ttu-id="6a371-128">source3</span><span class="sxs-lookup"><span data-stu-id="6a371-128">source3</span></span> | <span data-ttu-id="6a371-129">target3</span><span class="sxs-lookup"><span data-stu-id="6a371-129">target3</span></span> |



 

[<span data-ttu-id="6a371-130">ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="6a371-130">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)



| <span data-ttu-id="6a371-131">Ação</span><span class="sxs-lookup"><span data-stu-id="6a371-131">Action</span></span>  | <span data-ttu-id="6a371-132">Sequência</span><span class="sxs-lookup"><span data-stu-id="6a371-132">Sequence</span></span> | <span data-ttu-id="6a371-133">Baseaction</span><span class="sxs-lookup"><span data-stu-id="6a371-133">BaseAction</span></span> | <span data-ttu-id="6a371-134">After (após)</span><span class="sxs-lookup"><span data-stu-id="6a371-134">After</span></span> | <span data-ttu-id="6a371-135">Condição</span><span class="sxs-lookup"><span data-stu-id="6a371-135">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="6a371-136">Action2</span><span class="sxs-lookup"><span data-stu-id="6a371-136">Action2</span></span> |          | <span data-ttu-id="6a371-137">Action1</span><span class="sxs-lookup"><span data-stu-id="6a371-137">Action1</span></span>    | <span data-ttu-id="6a371-138">1</span><span class="sxs-lookup"><span data-stu-id="6a371-138">1</span></span>     | <span data-ttu-id="6a371-139">true</span><span class="sxs-lookup"><span data-stu-id="6a371-139">true</span></span>      |
| <span data-ttu-id="6a371-140">Action3</span><span class="sxs-lookup"><span data-stu-id="6a371-140">Action3</span></span> |          |            |       | <span data-ttu-id="6a371-141">true</span><span class="sxs-lookup"><span data-stu-id="6a371-141">true</span></span>      |



 

[<span data-ttu-id="6a371-142">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="6a371-142">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="6a371-143">Ação</span><span class="sxs-lookup"><span data-stu-id="6a371-143">Action</span></span>  | <span data-ttu-id="6a371-144">Sequência</span><span class="sxs-lookup"><span data-stu-id="6a371-144">Sequence</span></span> | <span data-ttu-id="6a371-145">Baseaction</span><span class="sxs-lookup"><span data-stu-id="6a371-145">BaseAction</span></span> | <span data-ttu-id="6a371-146">After (após)</span><span class="sxs-lookup"><span data-stu-id="6a371-146">After</span></span> | <span data-ttu-id="6a371-147">Condição</span><span class="sxs-lookup"><span data-stu-id="6a371-147">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="6a371-148">Action1</span><span class="sxs-lookup"><span data-stu-id="6a371-148">Action1</span></span> | <span data-ttu-id="6a371-149">1</span><span class="sxs-lookup"><span data-stu-id="6a371-149">1</span></span>        |            |       | <span data-ttu-id="6a371-150">true</span><span class="sxs-lookup"><span data-stu-id="6a371-150">true</span></span>      |



 

<span data-ttu-id="6a371-151">Para corrigir esses erros, tente o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6a371-151">To fix these errors try the following:</span></span>

-   <span data-ttu-id="6a371-152">Remova o número de sequência para a ação personalizada Action1 e use os campos Baseaction e After em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6a371-152">Remove the sequence number for the custom action Action1 and use the BaseAction and After fields instead.</span></span>
-   <span data-ttu-id="6a371-153">Insira valores nos campos Sequence, Baseaction ou After para a ação personalizada Action3.</span><span class="sxs-lookup"><span data-stu-id="6a371-153">Enter values into the Sequence, BaseAction, or After fields for the custom action Action3.</span></span> <span data-ttu-id="6a371-154">Deixe os campos Baseaction e After vazios para a ação padrão Action2.</span><span class="sxs-lookup"><span data-stu-id="6a371-154">Leave the BaseAction and After fields empty for standard action Action2.</span></span>
-   <span data-ttu-id="6a371-155">Não deixe o campo de sequência Vazio para a ação padrão Action2.</span><span class="sxs-lookup"><span data-stu-id="6a371-155">Do not leave the Sequence field empty for standard action Action2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a371-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a371-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a371-157">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="6a371-157">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



