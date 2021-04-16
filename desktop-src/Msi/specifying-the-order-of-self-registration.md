---
description: Observe que você não pode especificar a ordem na qual o instalador registra ou cancela o registro de DLLs de registro automático usando as ações SelfRegModules e SelfUnRegModules.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Especificando a ordem de auto-registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461224"
---
# <a name="specifying-the-order-of-self-registration"></a><span data-ttu-id="c2fe4-103">Especificando a ordem de auto-registro</span><span class="sxs-lookup"><span data-stu-id="c2fe4-103">Specifying the Order of Self Registration</span></span>

<span data-ttu-id="c2fe4-104">Observe que você não pode especificar a ordem na qual o instalador registra ou cancela o registro de DLLs de registro automático usando as ações [SelfRegModules](selfregmodules-action.md) e [SelfUnRegModules](selfunregmodules-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c2fe4-104">Note that you cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="c2fe4-105">Essas ações registram todos os módulos listados na [tabela selfreg](selfreg-table.md).</span><span class="sxs-lookup"><span data-stu-id="c2fe4-105">These actions register all the modules listed in the [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="c2fe4-106">O instalador não registra automaticamente os arquivos. exe.</span><span class="sxs-lookup"><span data-stu-id="c2fe4-106">The installer does not self-register .exe files.</span></span>

<span data-ttu-id="c2fe4-107">Para especificar a ordem na qual o instalador registra ou cancela o registro de módulos, você deve usar duas [ações personalizadas](custom-actions.md) para cada módulo.</span><span class="sxs-lookup"><span data-stu-id="c2fe4-107">To specify the order in which the installer registers or unregisters modules, you must use two [custom actions](custom-actions.md) for each module.</span></span> <span data-ttu-id="c2fe4-108">Uma ação personalizada para DllRegisterServer e um segundo para DllUnregisterServer.</span><span class="sxs-lookup"><span data-stu-id="c2fe4-108">One custom action for DllRegisterServer and a second for DllUnregisterServer.</span></span> <span data-ttu-id="c2fe4-109">Essas ações personalizadas devem então ser criadas na [tabela InstallExecuteSequence](installexecutesequence-table.md) no ponto na sequência onde quer que a dll seja registrada ou cancelada.</span><span class="sxs-lookup"><span data-stu-id="c2fe4-109">These custom actions must then be authored in the [InstallExecuteSequence table](installexecutesequence-table.md) at the point in the sequence wherever the DLL is to be registered or unregistered.</span></span>

<span data-ttu-id="c2fe4-110">O exemplo a seguir ilustra como criar o banco de dados para agendar o auto-registro de uma DLL em um ponto específico na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="c2fe4-110">The following example illustrates how to author the database to schedule the self-registration of a DLL at a particular point in the action sequence.</span></span>

<span data-ttu-id="c2fe4-111">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c2fe4-111">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="c2fe4-112">Arquivo</span><span class="sxs-lookup"><span data-stu-id="c2fe4-112">File</span></span>  | <span data-ttu-id="c2fe4-113">Componente\_</span><span class="sxs-lookup"><span data-stu-id="c2fe4-113">Component\_</span></span> | <span data-ttu-id="c2fe4-114">FileName</span><span class="sxs-lookup"><span data-stu-id="c2fe4-114">FileName</span></span>  | <span data-ttu-id="c2fe4-115">Sequência</span><span class="sxs-lookup"><span data-stu-id="c2fe4-115">Sequence</span></span> |
|-------|-------------|-----------|----------|
| <span data-ttu-id="c2fe4-116">mydll</span><span class="sxs-lookup"><span data-stu-id="c2fe4-116">mydll</span></span> | <span data-ttu-id="c2fe4-117">myComponent</span><span class="sxs-lookup"><span data-stu-id="c2fe4-117">myComponent</span></span> | <span data-ttu-id="c2fe4-118">Mydll.dll</span><span class="sxs-lookup"><span data-stu-id="c2fe4-118">Mydll.dll</span></span> | <span data-ttu-id="c2fe4-119">13</span><span class="sxs-lookup"><span data-stu-id="c2fe4-119">13</span></span>       |



 

<span data-ttu-id="c2fe4-120">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c2fe4-120">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="c2fe4-121">Componente</span><span class="sxs-lookup"><span data-stu-id="c2fe4-121">Component</span></span>   | <span data-ttu-id="c2fe4-122">ComponentId</span><span class="sxs-lookup"><span data-stu-id="c2fe4-122">ComponentId</span></span> | <span data-ttu-id="c2fe4-123">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="c2fe4-123">Directory\_</span></span> | <span data-ttu-id="c2fe4-124">KeyPath</span><span class="sxs-lookup"><span data-stu-id="c2fe4-124">KeyPath</span></span> |
|-------------|-------------|-------------|---------|
| <span data-ttu-id="c2fe4-125">myComponent</span><span class="sxs-lookup"><span data-stu-id="c2fe4-125">myComponent</span></span> | <span data-ttu-id="c2fe4-126">{*GUID*}</span><span class="sxs-lookup"><span data-stu-id="c2fe4-126">{*a GUID*}</span></span>  | <span data-ttu-id="c2fe4-127">myFolder</span><span class="sxs-lookup"><span data-stu-id="c2fe4-127">myFolder</span></span>    | <span data-ttu-id="c2fe4-128">mydll</span><span class="sxs-lookup"><span data-stu-id="c2fe4-128">mydll</span></span>   |



 

[<span data-ttu-id="c2fe4-129">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="c2fe4-129">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="c2fe4-130">Diretório</span><span class="sxs-lookup"><span data-stu-id="c2fe4-130">Directory</span></span> | <span data-ttu-id="c2fe4-131">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="c2fe4-131">Directory\_Parent</span></span> | <span data-ttu-id="c2fe4-132">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="c2fe4-132">DefaultDir</span></span>          |
|-----------|-------------------|---------------------|
| <span data-ttu-id="c2fe4-133">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="c2fe4-133">TARGETDIR</span></span> |                   | <span data-ttu-id="c2fe4-134">SourceDir</span><span class="sxs-lookup"><span data-stu-id="c2fe4-134">SourceDir</span></span>           |
| <span data-ttu-id="c2fe4-135">myFolder</span><span class="sxs-lookup"><span data-stu-id="c2fe4-135">myFolder</span></span>  | <span data-ttu-id="c2fe4-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="c2fe4-136">TARGETDIR</span></span>         | <span data-ttu-id="c2fe4-137">Pasta de \| minha pasta</span><span class="sxs-lookup"><span data-stu-id="c2fe4-137">myFolder\|My Folder</span></span> |



 

[<span data-ttu-id="c2fe4-138">Tabela CustomAction</span><span class="sxs-lookup"><span data-stu-id="c2fe4-138">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="c2fe4-139">Ação</span><span class="sxs-lookup"><span data-stu-id="c2fe4-139">Action</span></span>     | <span data-ttu-id="c2fe4-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2fe4-140">Type</span></span> | <span data-ttu-id="c2fe4-141">Fonte</span><span class="sxs-lookup"><span data-stu-id="c2fe4-141">Source</span></span>   | <span data-ttu-id="c2fe4-142">Destino</span><span class="sxs-lookup"><span data-stu-id="c2fe4-142">Target</span></span>                                     |
|------------|------|----------|--------------------------------------------|
| <span data-ttu-id="c2fe4-143">mydllREG</span><span class="sxs-lookup"><span data-stu-id="c2fe4-143">mydllREG</span></span>   | <span data-ttu-id="c2fe4-144">3170</span><span class="sxs-lookup"><span data-stu-id="c2fe4-144">3170</span></span> | <span data-ttu-id="c2fe4-145">myFolder</span><span class="sxs-lookup"><span data-stu-id="c2fe4-145">myFolder</span></span> | <span data-ttu-id="c2fe4-146">" \[ SystemFolder \] msiexec"/y " \[ \# myDll \] "</span><span class="sxs-lookup"><span data-stu-id="c2fe4-146">"\[SystemFolder\]msiexec" /y "\[\#mydll\]"</span></span> |
| <span data-ttu-id="c2fe4-147">mydllUNREG</span><span class="sxs-lookup"><span data-stu-id="c2fe4-147">mydllUNREG</span></span> | <span data-ttu-id="c2fe4-148">3170</span><span class="sxs-lookup"><span data-stu-id="c2fe4-148">3170</span></span> | <span data-ttu-id="c2fe4-149">myFolder</span><span class="sxs-lookup"><span data-stu-id="c2fe4-149">myFolder</span></span> | <span data-ttu-id="c2fe4-150">" \[ SystemFolder \] msiexec"/z " \[ \# myDll \] "</span><span class="sxs-lookup"><span data-stu-id="c2fe4-150">"\[SystemFolder\]msiexec" /z "\[\#mydll\]"</span></span> |



 

<span data-ttu-id="c2fe4-151">[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c2fe4-151">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="c2fe4-152">Ação</span><span class="sxs-lookup"><span data-stu-id="c2fe4-152">Action</span></span>           | <span data-ttu-id="c2fe4-153">Condição</span><span class="sxs-lookup"><span data-stu-id="c2fe4-153">Condition</span></span>         | <span data-ttu-id="c2fe4-154">Sequência</span><span class="sxs-lookup"><span data-stu-id="c2fe4-154">Sequence</span></span> |
|------------------|-------------------|----------|
| <span data-ttu-id="c2fe4-155">SelfUnregModules</span><span class="sxs-lookup"><span data-stu-id="c2fe4-155">SelfUnregModules</span></span> |                   | <span data-ttu-id="c2fe4-156">2200</span><span class="sxs-lookup"><span data-stu-id="c2fe4-156">2200</span></span>     |
| <span data-ttu-id="c2fe4-157">mydllUNREG</span><span class="sxs-lookup"><span data-stu-id="c2fe4-157">mydllUNREG</span></span>       | <span data-ttu-id="c2fe4-158">$myComponent = 2</span><span class="sxs-lookup"><span data-stu-id="c2fe4-158">$myComponent=2</span></span>    | <span data-ttu-id="c2fe4-159">2201</span><span class="sxs-lookup"><span data-stu-id="c2fe4-159">2201</span></span>     |
| <span data-ttu-id="c2fe4-160">Removes</span><span class="sxs-lookup"><span data-stu-id="c2fe4-160">RemoveFiles</span></span>      |                   | <span data-ttu-id="c2fe4-161">3500</span><span class="sxs-lookup"><span data-stu-id="c2fe4-161">3500</span></span>     |
| <span data-ttu-id="c2fe4-162">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="c2fe4-162">InstallFiles</span></span>     |                   | <span data-ttu-id="c2fe4-163">4000</span><span class="sxs-lookup"><span data-stu-id="c2fe4-163">4000</span></span>     |
| <span data-ttu-id="c2fe4-164">SelfRegModules</span><span class="sxs-lookup"><span data-stu-id="c2fe4-164">SelfRegModules</span></span>   |                   | <span data-ttu-id="c2fe4-165">6500</span><span class="sxs-lookup"><span data-stu-id="c2fe4-165">6500</span></span>     |
| <span data-ttu-id="c2fe4-166">mydllREG</span><span class="sxs-lookup"><span data-stu-id="c2fe4-166">mydllREG</span></span>         | <span data-ttu-id="c2fe4-167">$myComponent>2</span><span class="sxs-lookup"><span data-stu-id="c2fe4-167">$myComponent>2</span></span> | <span data-ttu-id="c2fe4-168">6501</span><span class="sxs-lookup"><span data-stu-id="c2fe4-168">6501</span></span>     |



 

 

 



