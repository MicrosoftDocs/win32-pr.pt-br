---
description: As tabelas a seguir são necessárias em um módulo de mesclagem padrão.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Mesclar tabelas do banco de dados do módulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766392"
---
# <a name="merge-module-database-tables"></a><span data-ttu-id="ef09c-103">Mesclar tabelas do banco de dados do módulo</span><span class="sxs-lookup"><span data-stu-id="ef09c-103">Merge Module Database Tables</span></span>

<span data-ttu-id="ef09c-104">As tabelas a seguir são necessárias em um módulo de mesclagem padrão.</span><span class="sxs-lookup"><span data-stu-id="ef09c-104">The following tables are required in a standard merge module.</span></span>



| <span data-ttu-id="ef09c-105">Nome da tabela</span><span class="sxs-lookup"><span data-stu-id="ef09c-105">Table name</span></span>                                       | <span data-ttu-id="ef09c-106">Comentário</span><span class="sxs-lookup"><span data-stu-id="ef09c-106">Comment</span></span>                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef09c-107">Componente</span><span class="sxs-lookup"><span data-stu-id="ef09c-107">Component</span></span>](component-table.md)                 | <span data-ttu-id="ef09c-108">NECESSÁRIA</span><span class="sxs-lookup"><span data-stu-id="ef09c-108">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="ef09c-109">Diretório</span><span class="sxs-lookup"><span data-stu-id="ef09c-109">Directory</span></span>](directory-table.md)                 | <span data-ttu-id="ef09c-110">NECESSÁRIA</span><span class="sxs-lookup"><span data-stu-id="ef09c-110">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="ef09c-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="ef09c-111">FeatureComponents</span></span>](featurecomponents-table.md) | <span data-ttu-id="ef09c-112">NECESSÁRIA</span><span class="sxs-lookup"><span data-stu-id="ef09c-112">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="ef09c-113">Arquivo</span><span class="sxs-lookup"><span data-stu-id="ef09c-113">File</span></span>](file-table.md)                           | <span data-ttu-id="ef09c-114">NECESSÁRIA</span><span class="sxs-lookup"><span data-stu-id="ef09c-114">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="ef09c-115">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="ef09c-115">ModuleSignature</span></span>](modulesignature-table.md)     | <span data-ttu-id="ef09c-116">NECESSÁRIA Mesclado no banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="ef09c-116">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="ef09c-117">Lista as informações que identificam um módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="ef09c-117">Lists the information identifying a merge module.</span></span> |
| [<span data-ttu-id="ef09c-118">ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="ef09c-118">ModuleComponents</span></span>](modulecomponents-table.md)   | <span data-ttu-id="ef09c-119">NECESSÁRIA Mesclado no banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="ef09c-119">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="ef09c-120">Lista todos os componentes no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="ef09c-120">Lists all the components in the merge module.</span></span>     |



 

<span data-ttu-id="ef09c-121">As tabelas a seguir só ocorrem em módulos de mesclagem ou outros bancos de dados do instalador que já foram combinados com um módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="ef09c-121">The following tables only occur in merge modules or other installer databases that have already been combined with a merge module.</span></span>



| <span data-ttu-id="ef09c-122">Nome da tabela</span><span class="sxs-lookup"><span data-stu-id="ef09c-122">Table name</span></span>                                     | <span data-ttu-id="ef09c-123">Comentário</span><span class="sxs-lookup"><span data-stu-id="ef09c-123">Comment</span></span>                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef09c-124">ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="ef09c-124">ModuleDependency</span></span>](moduledependency-table.md) | <span data-ttu-id="ef09c-125">Mesclado no banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="ef09c-125">Merged into the installer database.</span></span> <span data-ttu-id="ef09c-126">Lista outros módulos de mesclagem exigidos por este módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="ef09c-126">Lists other merge modules required by this merge module.</span></span>                |
| [<span data-ttu-id="ef09c-127">ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="ef09c-127">ModuleExclusion</span></span>](moduleexclusion-table.md)   | <span data-ttu-id="ef09c-128">Mesclado no banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="ef09c-128">Merged into the installer database.</span></span> <span data-ttu-id="ef09c-129">Lista outros módulos de mesclagem que são incompatíveis com esse módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="ef09c-129">Lists other merge modules that are incompatible with this merge module.</span></span> |



 

<span data-ttu-id="ef09c-130">As tabelas ModuleSequence a seguir só ocorrem em módulos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="ef09c-130">The following ModuleSequence tables only occur in merge modules.</span></span>



| <span data-ttu-id="ef09c-131">Nome da tabela</span><span class="sxs-lookup"><span data-stu-id="ef09c-131">Table name</span></span>                                                             | <span data-ttu-id="ef09c-132">Comentário</span><span class="sxs-lookup"><span data-stu-id="ef09c-132">Comment</span></span>                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef09c-133">ModuleAdminUISequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-133">ModuleAdminUISequence</span></span>](moduleadminuisequence-table.md)               | <span data-ttu-id="ef09c-134">Mescla ações na [tabela AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef09c-134">Merges actions into the [AdminUISequence table](adminuisequence-table.md).</span></span>               |
| [<span data-ttu-id="ef09c-135">ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-135">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)     | <span data-ttu-id="ef09c-136">Mescla ações na [tabela AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef09c-136">Merges actions into the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>     |
| [<span data-ttu-id="ef09c-137">ModuleAdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-137">ModuleAdvtUISequence</span></span>](moduleadvtuisequence-table.md)                 | <span data-ttu-id="ef09c-138">Não use esta tabela.</span><span class="sxs-lookup"><span data-stu-id="ef09c-138">Do not use this table.</span></span> <span data-ttu-id="ef09c-139">Para obter detalhes, consulte [tabela AdvtUISequence](advtuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef09c-139">For details, see [AdvtUISequence table](advtuisequence-table.md).</span></span> |
| [<span data-ttu-id="ef09c-140">ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-140">ModuleAdvtExecuteSequence</span></span>](moduleadvtexecutesequence-table.md)       | <span data-ttu-id="ef09c-141">Mescla ações na [tabela AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef09c-141">Merges actions into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>       |
| [<span data-ttu-id="ef09c-142">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="ef09c-142">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)                       | <span data-ttu-id="ef09c-143">Lista as tabelas no módulo que não são mescladas no arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="ef09c-143">Lists tables in the module that are not merged into the .msi file.</span></span>                        |
| [<span data-ttu-id="ef09c-144">ModuleInstallUISequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-144">ModuleInstallUISequence</span></span>](moduleinstalluisequence-table.md)           | <span data-ttu-id="ef09c-145">Mescla ações na [tabela InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef09c-145">Merges actions into the [InstallUISequence table](installuisequence-table.md).</span></span>           |
| [<span data-ttu-id="ef09c-146">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-146">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md) | <span data-ttu-id="ef09c-147">Mescla ações na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef09c-147">Merges actions into the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> |



 

<span data-ttu-id="ef09c-148">As tabelas a seguir são necessárias em todos os módulos de mesclagem configuráveis.</span><span class="sxs-lookup"><span data-stu-id="ef09c-148">The following tables are required in every configurable merge module.</span></span> <span data-ttu-id="ef09c-149">Mergemod.dll 2,0 ou posterior é necessário para criar um módulo de mesclagem configurável.</span><span class="sxs-lookup"><span data-stu-id="ef09c-149">Mergemod.dll 2.0 or later is required to create configurable merge module.</span></span> <span data-ttu-id="ef09c-150">Para obter detalhes, consulte [módulos de mesclagem configuráveis](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="ef09c-150">For details, see [Configurable Merge Modules](configurable-merge-modules.md).</span></span>



| <span data-ttu-id="ef09c-151">Nome da tabela</span><span class="sxs-lookup"><span data-stu-id="ef09c-151">Table name</span></span>                                                 | <span data-ttu-id="ef09c-152">Comentário</span><span class="sxs-lookup"><span data-stu-id="ef09c-152">Comment</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef09c-153">Tabela ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="ef09c-153">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)   | <span data-ttu-id="ef09c-154">NECESSÁRIA Essa tabela não é mesclada no banco de dados de instalação de destino.</span><span class="sxs-lookup"><span data-stu-id="ef09c-154">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="ef09c-155">Especifica os campos configuráveis no banco de dados de destino e fornece um modelo para a configuração de cada campo.</span><span class="sxs-lookup"><span data-stu-id="ef09c-155">Specifies the configurable fields in the target database and provides a template for the configuration of each field.</span></span> |
| [<span data-ttu-id="ef09c-156">Tabela ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef09c-156">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md) | <span data-ttu-id="ef09c-157">NECESSÁRIA Essa tabela não é mesclada no banco de dados de instalação de destino.</span><span class="sxs-lookup"><span data-stu-id="ef09c-157">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="ef09c-158">Identifica os atributos configuráveis do módulo.</span><span class="sxs-lookup"><span data-stu-id="ef09c-158">Identifies the configurable attributes of the module.</span></span>                                                                 |



 

<span data-ttu-id="ef09c-159">As tabelas do instalador a seguir não podem ocorrer em um módulo de mesclagem padrão.</span><span class="sxs-lookup"><span data-stu-id="ef09c-159">The following installer tables cannot occur in a standard merge module.</span></span>

-   [<span data-ttu-id="ef09c-160">BBControl</span><span class="sxs-lookup"><span data-stu-id="ef09c-160">BBControl</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="ef09c-161">Mensagem</span><span class="sxs-lookup"><span data-stu-id="ef09c-161">Billboard</span></span>](billboard-table.md)
-   [<span data-ttu-id="ef09c-162">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="ef09c-162">CCPSearch</span></span>](ccpsearch-table.md)
-   [<span data-ttu-id="ef09c-163">Erro</span><span class="sxs-lookup"><span data-stu-id="ef09c-163">Error</span></span>](error-table.md)
-   [<span data-ttu-id="ef09c-164">Recurso</span><span class="sxs-lookup"><span data-stu-id="ef09c-164">Feature</span></span>](feature-table.md)
-   [<span data-ttu-id="ef09c-165">Tabela LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="ef09c-165">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="ef09c-166">Mídia</span><span class="sxs-lookup"><span data-stu-id="ef09c-166">Media</span></span>](media-table.md)
-   [<span data-ttu-id="ef09c-167">Patch</span><span class="sxs-lookup"><span data-stu-id="ef09c-167">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="ef09c-168">Atualizar</span><span class="sxs-lookup"><span data-stu-id="ef09c-168">Upgrade</span></span>](upgrade-table.md)

<span data-ttu-id="ef09c-169">As tabelas do instalador a seguir são opcionais em módulos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="ef09c-169">The following installer tables are optional in merge modules.</span></span>

-   [<span data-ttu-id="ef09c-170">ActionText</span><span class="sxs-lookup"><span data-stu-id="ef09c-170">ActionText</span></span>](actiontext-table.md)
-   [<span data-ttu-id="ef09c-171">AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-171">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="ef09c-172">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-172">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="ef09c-173">AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-173">AdvtExecuteSequence</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="ef09c-174">AdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-174">AdvtUISequence</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="ef09c-175">AppId</span><span class="sxs-lookup"><span data-stu-id="ef09c-175">AppId</span></span>](appid-table.md)
-   [<span data-ttu-id="ef09c-176">AppSearch</span><span class="sxs-lookup"><span data-stu-id="ef09c-176">AppSearch</span></span>](appsearch-table.md)
-   [<span data-ttu-id="ef09c-177">BindImage</span><span class="sxs-lookup"><span data-stu-id="ef09c-177">BindImage</span></span>](bindimage-table.md)
-   [<span data-ttu-id="ef09c-178">CheckBox</span><span class="sxs-lookup"><span data-stu-id="ef09c-178">CheckBox</span></span>](checkbox-table.md)
-   [<span data-ttu-id="ef09c-179">Classe</span><span class="sxs-lookup"><span data-stu-id="ef09c-179">Class</span></span>](class-table.md)
-   [<span data-ttu-id="ef09c-180">ComboBox</span><span class="sxs-lookup"><span data-stu-id="ef09c-180">ComboBox</span></span>](combobox-table.md)
-   [<span data-ttu-id="ef09c-181">CompLocator</span><span class="sxs-lookup"><span data-stu-id="ef09c-181">CompLocator</span></span>](complocator-table.md)
-   [<span data-ttu-id="ef09c-182">Controle</span><span class="sxs-lookup"><span data-stu-id="ef09c-182">Control</span></span>](control-table.md)
-   [<span data-ttu-id="ef09c-183">ControlCondition</span><span class="sxs-lookup"><span data-stu-id="ef09c-183">ControlCondition</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="ef09c-184">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ef09c-184">CreateFolder</span></span>](createfolder-table.md)
-   [<span data-ttu-id="ef09c-185">CustomAction</span><span class="sxs-lookup"><span data-stu-id="ef09c-185">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="ef09c-186">Diálogo</span><span class="sxs-lookup"><span data-stu-id="ef09c-186">Dialog</span></span>](dialog-table.md)
-   [<span data-ttu-id="ef09c-187">DrLocator</span><span class="sxs-lookup"><span data-stu-id="ef09c-187">DrLocator</span></span>](drlocator-table.md)
-   [<span data-ttu-id="ef09c-188">Duplicatafile</span><span class="sxs-lookup"><span data-stu-id="ef09c-188">DuplicateFile</span></span>](duplicatefile-table.md)
-   [<span data-ttu-id="ef09c-189">Ambiente</span><span class="sxs-lookup"><span data-stu-id="ef09c-189">Environment</span></span>](environment-table.md)
-   [<span data-ttu-id="ef09c-190">EventMappings</span><span class="sxs-lookup"><span data-stu-id="ef09c-190">EventMapping</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="ef09c-191">Extensão</span><span class="sxs-lookup"><span data-stu-id="ef09c-191">Extension</span></span>](extension-table.md)
-   [<span data-ttu-id="ef09c-192">Fonte</span><span class="sxs-lookup"><span data-stu-id="ef09c-192">Font</span></span>](font-table.md)
-   [<span data-ttu-id="ef09c-193">Ícone</span><span class="sxs-lookup"><span data-stu-id="ef09c-193">Icon</span></span>](icon-table.md)
-   [<span data-ttu-id="ef09c-194">IniFile</span><span class="sxs-lookup"><span data-stu-id="ef09c-194">IniFile</span></span>](inifile-table.md)
-   [<span data-ttu-id="ef09c-195">IniLocator</span><span class="sxs-lookup"><span data-stu-id="ef09c-195">IniLocator</span></span>](inilocator-table.md)
-   [<span data-ttu-id="ef09c-196">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-196">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="ef09c-197">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="ef09c-197">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="ef09c-198">ListBox</span><span class="sxs-lookup"><span data-stu-id="ef09c-198">ListBox</span></span>](listbox-table.md)
-   [<span data-ttu-id="ef09c-199">ListView</span><span class="sxs-lookup"><span data-stu-id="ef09c-199">ListView</span></span>](listview-table.md)
-   [<span data-ttu-id="ef09c-200">MIME</span><span class="sxs-lookup"><span data-stu-id="ef09c-200">MIME</span></span>](mime-table.md)
-   [<span data-ttu-id="ef09c-201">MoveFile</span><span class="sxs-lookup"><span data-stu-id="ef09c-201">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="ef09c-202">ODBCattribute</span><span class="sxs-lookup"><span data-stu-id="ef09c-202">ODBCAttribute</span></span>](odbcattribute-table.md)
-   [<span data-ttu-id="ef09c-203">ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="ef09c-203">ODBCDataSource</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="ef09c-204">ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="ef09c-204">ODBCDriver</span></span>](odbcdriver-table.md)
-   [<span data-ttu-id="ef09c-205">ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="ef09c-205">ODBCSourceAttribute</span></span>](odbcsourceattribute-table.md)
-   [<span data-ttu-id="ef09c-206">ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="ef09c-206">ODBCTranslator</span></span>](odbctranslator-table.md)
-   [<span data-ttu-id="ef09c-207">Tabela ProgID</span><span class="sxs-lookup"><span data-stu-id="ef09c-207">ProgID Table</span></span>](progid-table.md)
-   [<span data-ttu-id="ef09c-208">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ef09c-208">Property</span></span>](property-table.md)
-   [<span data-ttu-id="ef09c-209">PublishComponent</span><span class="sxs-lookup"><span data-stu-id="ef09c-209">PublishComponent</span></span>](publishcomponent-table.md)
-   [<span data-ttu-id="ef09c-210">RadioButton</span><span class="sxs-lookup"><span data-stu-id="ef09c-210">RadioButton</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="ef09c-211">Tabela do registro</span><span class="sxs-lookup"><span data-stu-id="ef09c-211">Registry Table</span></span>](registry-table.md)
-   [<span data-ttu-id="ef09c-212">RegLocator</span><span class="sxs-lookup"><span data-stu-id="ef09c-212">RegLocator</span></span>](reglocator-table.md)
-   [<span data-ttu-id="ef09c-213">RemoveFile</span><span class="sxs-lookup"><span data-stu-id="ef09c-213">RemoveFile</span></span>](removefile-table.md)
-   [<span data-ttu-id="ef09c-214">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="ef09c-214">RemoveIniFile</span></span>](removeinifile-table.md)
-   [<span data-ttu-id="ef09c-215">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="ef09c-215">RemoveRegistry</span></span>](removeregistry-table.md)
-   [<span data-ttu-id="ef09c-216">ReserveCost</span><span class="sxs-lookup"><span data-stu-id="ef09c-216">ReserveCost</span></span>](reservecost-table.md)
-   [<span data-ttu-id="ef09c-217">SelfReg</span><span class="sxs-lookup"><span data-stu-id="ef09c-217">SelfReg</span></span>](selfreg-table.md)
-   [<span data-ttu-id="ef09c-218">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="ef09c-218">ServiceControl</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="ef09c-219">Instalar o</span><span class="sxs-lookup"><span data-stu-id="ef09c-219">ServiceInstall</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="ef09c-220">Atalho</span><span class="sxs-lookup"><span data-stu-id="ef09c-220">Shortcut</span></span>](shortcut-table.md)
-   [<span data-ttu-id="ef09c-221">Signature</span><span class="sxs-lookup"><span data-stu-id="ef09c-221">Signature</span></span>](signature-table.md)
-   <span data-ttu-id="ef09c-222">[Estilo]](textstyle-table.md)</span><span class="sxs-lookup"><span data-stu-id="ef09c-222">[TextStyle](textstyle-table.md)</span></span>
-   [<span data-ttu-id="ef09c-223">Importação</span><span class="sxs-lookup"><span data-stu-id="ef09c-223">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="ef09c-224">UIText</span><span class="sxs-lookup"><span data-stu-id="ef09c-224">UIText</span></span>](uitext-table.md)
-   [<span data-ttu-id="ef09c-225">Verbo</span><span class="sxs-lookup"><span data-stu-id="ef09c-225">Verb</span></span>](verb-table.md)

 

 



