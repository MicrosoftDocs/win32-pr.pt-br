---
description: ICEM09 verifica se o módulo de mesclagem trata com segurança os diretórios predefinidos.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b4d2d52c35d6dd3670daff5150a785e19d0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170430"
---
# <a name="icem09"></a><span data-ttu-id="94c24-103">ICEM09</span><span class="sxs-lookup"><span data-stu-id="94c24-103">ICEM09</span></span>

<span data-ttu-id="94c24-104">ICEM09 verifica se o módulo de mesclagem trata com segurança os diretórios predefinidos.</span><span class="sxs-lookup"><span data-stu-id="94c24-104">ICEM09 verifies the merge module safely handles predefined directories.</span></span> <span data-ttu-id="94c24-105">Ele faz isso verificando se nenhum componente no módulo instala um diretório em um diretório de sistema predefinido, como "ProgramFilesFolder" ou "StartMenuFolder".</span><span class="sxs-lookup"><span data-stu-id="94c24-105">It does this by verifying that no component in the module installs a directory to a predefined system directory such as "ProgramFilesFolder" or "StartMenuFolder".</span></span> <span data-ttu-id="94c24-106">Em vez disso, os módulos devem usar diretórios com nomes exclusivos (criados com a Convenção de nomenclatura do módulo de mesclagem) e usar ações personalizadas para direcionar o diretório de destino apropriado.</span><span class="sxs-lookup"><span data-stu-id="94c24-106">Instead, modules should use directories with unique names (created with the merge module naming convention) and use custom actions to target the appropriate target directory.</span></span> <span data-ttu-id="94c24-107">Essa abordagem impede que os módulos entrem em conflito com uma estrutura de diretório existente no banco de dados final.</span><span class="sxs-lookup"><span data-stu-id="94c24-107">This approach prevents modules from conflicting with an existing directory structure in the final database.</span></span> <span data-ttu-id="94c24-108">ICEM09 verifica se as ações personalizadas necessárias para que essa técnica funcione não existem (para que a ferramenta de mesclagem possa gerá-las) ou exista no formato correto (para que funcionem conforme o esperado).</span><span class="sxs-lookup"><span data-stu-id="94c24-108">ICEM09 checks that the custom actions needed for this technique to work either do not exist (so that the merge tool can generate them) or exist in the correct form (so that they work as expected).</span></span>

<span data-ttu-id="94c24-109">Falha ao corrigir um aviso ou erro relatado pelo ICEM09 pode causar problemas para os clientes do seu módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="94c24-109">Failure to fix a warning or error reported by ICEM09 could cause problems for the clients of your merge module.</span></span> <span data-ttu-id="94c24-110">As linhas da tabela de diretório com chaves primárias, como ProgramFilesFolder, geralmente existem em um banco de dados; Portanto, se os componentes em seu módulo forem instalados diretamente em diretórios predefinidos, como ProgramFilesFolder, as entradas de diretório no módulo poderão colidir com linhas já existentes.</span><span class="sxs-lookup"><span data-stu-id="94c24-110">Directory table rows with primary keys such as ProgramFilesFolder often exist in a database; therefore, if components in your module install directly to predefined directories such as ProgramFilesFolder, the directory entries in the module may collide with already existing rows.</span></span> <span data-ttu-id="94c24-111">Essa condição exige que o usuário do seu módulo divida os arquivos de origem do seu módulo para corresponder ao diretório de origem existente.</span><span class="sxs-lookup"><span data-stu-id="94c24-111">This condition would require the user of your module to split the source files from your module in order to match the existing source directory.</span></span>

## <a name="result"></a><span data-ttu-id="94c24-112">Resultado</span><span class="sxs-lookup"><span data-stu-id="94c24-112">Result</span></span>

<span data-ttu-id="94c24-113">O ICEM09 relata um erro ou aviso quando um componente de módulo instala um diretório em um diretório de sistema predefinido, causando um conflito de nome possível com a estrutura de diretório existente.</span><span class="sxs-lookup"><span data-stu-id="94c24-113">ICEM09 reports an error or warning when a module component installs a directory to a pre-defined system directory, causing a possible name conflict with the existing directory structure.</span></span>

## <a name="example"></a><span data-ttu-id="94c24-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="94c24-114">Example</span></span>

<span data-ttu-id="94c24-115">ICEM09 posta os seguintes avisos para um módulo que contém as entradas de banco de dados mostradas.</span><span class="sxs-lookup"><span data-stu-id="94c24-115">ICEM09 posts the following warnings for a module containing the database entries shown.</span></span>

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

<span data-ttu-id="94c24-116">Renomeie o diretório do módulo de mesclagem para que ele não corresponda a uma propriedade Windows Installer e, portanto, seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="94c24-116">Rename the merge module directory so it does not match a Windows Installer property and therefore is unique.</span></span> <span data-ttu-id="94c24-117">Em seguida, defina uma propriedade com o mesmo nome para o valor do diretório Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="94c24-117">Then set a property of the same name to the value of the Windows Installer directory.</span></span> <span data-ttu-id="94c24-118">Quando ocorre a resolução de diretório, o diretório tem uma propriedade de mesmo nome, portanto, o local de instalação do diretório é o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="94c24-118">When directory resolution takes place, the directory has a property of the same name, so the install location of the directory is the value of the property.</span></span> <span data-ttu-id="94c24-119">Os arquivos são movidos do local de origem distinto para o mesmo local de destino.</span><span class="sxs-lookup"><span data-stu-id="94c24-119">Files move from the distinct source location to the same target location.</span></span> <span data-ttu-id="94c24-120">Esse processo deve remover completamente os conflitos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="94c24-120">This process should completely remove the merge conflicts.</span></span>

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

<span data-ttu-id="94c24-121">Se a ação não tiver o número de sequência 1, ela não poderá ser mesclada ao banco de dados de destino desde o início suficiente na sequência para funcionar com eficiência.</span><span class="sxs-lookup"><span data-stu-id="94c24-121">If the action does not have sequence number 1, it may not merge in to the target database early enough in the sequence to work effectively.</span></span>

<span data-ttu-id="94c24-122">Para corrigir esse aviso, defina o número de sequência como 1.</span><span class="sxs-lookup"><span data-stu-id="94c24-122">To fix this warning, set the sequence number to 1.</span></span> <span data-ttu-id="94c24-123">Observe que a maioria das ferramentas de mesclagem atuais (mas não algumas versões mais antigas) gerará essas ações personalizadas no momento da mesclagem, de modo que nem sempre é necessário criar explicitamente as ações no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="94c24-123">Note that most current merge tools (but not some older versions) will generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

<span data-ttu-id="94c24-124">Como a coluna CustomAction é a chave primária da tabela CustomAction, algumas ferramentas de mesclagem podem gerar ações duplicadas porque o nome da ação previamente criada é diferente.</span><span class="sxs-lookup"><span data-stu-id="94c24-124">Because the CustomAction column is the primary key of CustomAction table, some merge tools may generate duplicate actions because the pre-authored action name is different.</span></span>

<span data-ttu-id="94c24-125">Para corrigir esse aviso, nomeie a ação da mesma forma que o diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="94c24-125">To fix this warning, name the action the same as the target directory.</span></span> <span data-ttu-id="94c24-126">Observe que a maioria das ferramentas de mesclagem atuais (mas não algumas versões mais antigas) gera essas ações personalizadas no momento da mesclagem, de modo que nem sempre é necessário criar explicitamente as ações no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="94c24-126">Note that most current merge tools (but not some older versions) generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

[<span data-ttu-id="94c24-127">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="94c24-127">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="94c24-128">Diretório</span><span class="sxs-lookup"><span data-stu-id="94c24-128">Directory</span></span>          | <span data-ttu-id="94c24-129">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="94c24-129">Directory\_Parent</span></span> | <span data-ttu-id="94c24-130">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="94c24-130">DefaultDir</span></span> |
|--------------------|-------------------|------------|
| <span data-ttu-id="94c24-131">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="94c24-131">ProgramFilesFolder</span></span> | <span data-ttu-id="94c24-132">Directory1</span><span class="sxs-lookup"><span data-stu-id="94c24-132">Directory1</span></span>        | <span data-ttu-id="94c24-133">Um</span><span class="sxs-lookup"><span data-stu-id="94c24-133">A</span></span>          |
| <span data-ttu-id="94c24-134">StartMenuFolder</span><span class="sxs-lookup"><span data-stu-id="94c24-134">StartMenuFolder</span></span>    | <span data-ttu-id="94c24-135">Directory2</span><span class="sxs-lookup"><span data-stu-id="94c24-135">Directory2</span></span>        | <span data-ttu-id="94c24-136">B:C</span><span class="sxs-lookup"><span data-stu-id="94c24-136">B:C</span></span>        |
| <span data-ttu-id="94c24-137">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="94c24-137">AppDataFolder</span></span>      | <span data-ttu-id="94c24-138">Directory3</span><span class="sxs-lookup"><span data-stu-id="94c24-138">Directory3</span></span>        | <span data-ttu-id="94c24-139">D</span><span class="sxs-lookup"><span data-stu-id="94c24-139">D</span></span>          |
| <span data-ttu-id="94c24-140">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="94c24-140">MyPicturesFolder</span></span>   | <span data-ttu-id="94c24-141">Directory4</span><span class="sxs-lookup"><span data-stu-id="94c24-141">Directory4</span></span>        | <span data-ttu-id="94c24-142">E</span><span class="sxs-lookup"><span data-stu-id="94c24-142">E</span></span>          |



 

[<span data-ttu-id="94c24-143">Tabela de componentes</span><span class="sxs-lookup"><span data-stu-id="94c24-143">Component Table</span></span>](component-table.md)



| <span data-ttu-id="94c24-144">Componente</span><span class="sxs-lookup"><span data-stu-id="94c24-144">Component</span></span>               | <span data-ttu-id="94c24-145">Diretório</span><span class="sxs-lookup"><span data-stu-id="94c24-145">Directory</span></span>          |
|-------------------------|--------------------|
| <span data-ttu-id="94c24-146">Component1.<GUID></span><span class="sxs-lookup"><span data-stu-id="94c24-146">Component1.<GUID></span></span> | <span data-ttu-id="94c24-147">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="94c24-147">ProgramFilesFolder</span></span> |
| <span data-ttu-id="94c24-148">Component2.<GUID></span><span class="sxs-lookup"><span data-stu-id="94c24-148">Component2.<GUID></span></span> | <span data-ttu-id="94c24-149">StartMenuFolder</span><span class="sxs-lookup"><span data-stu-id="94c24-149">StartMenuFolder</span></span>    |
| <span data-ttu-id="94c24-150">Component3.<GUID></span><span class="sxs-lookup"><span data-stu-id="94c24-150">Component3.<GUID></span></span> | <span data-ttu-id="94c24-151">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="94c24-151">AppDataFolder</span></span>      |
| <span data-ttu-id="94c24-152">Component4.<GUID></span><span class="sxs-lookup"><span data-stu-id="94c24-152">Component4.<GUID></span></span> | <span data-ttu-id="94c24-153">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="94c24-153">MyPicturesFolder</span></span>   |



 

[<span data-ttu-id="94c24-154">Tabela CustomAction</span><span class="sxs-lookup"><span data-stu-id="94c24-154">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="94c24-155">CustomAction</span><span class="sxs-lookup"><span data-stu-id="94c24-155">CustomAction</span></span>                 | <span data-ttu-id="94c24-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="94c24-156">Type</span></span> | <span data-ttu-id="94c24-157">Fonte</span><span class="sxs-lookup"><span data-stu-id="94c24-157">Source</span></span>                       | <span data-ttu-id="94c24-158">Destino</span><span class="sxs-lookup"><span data-stu-id="94c24-158">Target</span></span>              |
|------------------------------|------|------------------------------|---------------------|
| <span data-ttu-id="94c24-159">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="94c24-159">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="94c24-160">51</span><span class="sxs-lookup"><span data-stu-id="94c24-160">51</span></span>   | <span data-ttu-id="94c24-161">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="94c24-161">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="94c24-162">\[StartMenuFolder\]</span><span class="sxs-lookup"><span data-stu-id="94c24-162">\[StartMenuFolder\]</span></span> |
| <span data-ttu-id="94c24-163">MyAppDataFolderAction</span><span class="sxs-lookup"><span data-stu-id="94c24-163">MyAppDataFolderAction</span></span>        | <span data-ttu-id="94c24-164">51</span><span class="sxs-lookup"><span data-stu-id="94c24-164">51</span></span>   | <span data-ttu-id="94c24-165">AppDataFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="94c24-165">AppDataFolder.<GUID></span></span>   | <span data-ttu-id="94c24-166">\[AppDataFolder\]</span><span class="sxs-lookup"><span data-stu-id="94c24-166">\[AppDataFolder\]</span></span>   |



 

[<span data-ttu-id="94c24-167">Tabela ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="94c24-167">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="94c24-168">Ação</span><span class="sxs-lookup"><span data-stu-id="94c24-168">Action</span></span>                       | <span data-ttu-id="94c24-169">Sequência</span><span class="sxs-lookup"><span data-stu-id="94c24-169">Sequence</span></span> | <span data-ttu-id="94c24-170">Baseaction</span><span class="sxs-lookup"><span data-stu-id="94c24-170">BaseAction</span></span> | <span data-ttu-id="94c24-171">After (após)</span><span class="sxs-lookup"><span data-stu-id="94c24-171">After</span></span> | <span data-ttu-id="94c24-172">Condição</span><span class="sxs-lookup"><span data-stu-id="94c24-172">Condition</span></span> |
|------------------------------|----------|------------|-------|-----------|
| <span data-ttu-id="94c24-173">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="94c24-173">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="94c24-174">100</span><span class="sxs-lookup"><span data-stu-id="94c24-174">100</span></span>      |            |       |           |



 

## <a name="related-topics"></a><span data-ttu-id="94c24-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94c24-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94c24-176">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="94c24-176">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



