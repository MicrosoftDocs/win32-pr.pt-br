---
description: O procedimento a seguir descreve as etapas gerais para criar módulos de mesclagem.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Criando módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169199"
---
# <a name="authoring-merge-modules"></a><span data-ttu-id="1642b-103">Criando módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-103">Authoring Merge Modules</span></span>

<span data-ttu-id="1642b-104">O procedimento a seguir descreve as etapas gerais para criar módulos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1642b-104">The following procedure describes the general steps to authoring merge modules.</span></span>

<span data-ttu-id="1642b-105">**Para criar um novo módulo de mesclagem**</span><span class="sxs-lookup"><span data-stu-id="1642b-105">**To create a new merge module**</span></span>

1.  <span data-ttu-id="1642b-106">Obtenha uma ferramenta de software que você pode usar para editar o banco de dados do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1642b-106">Obtain a software tool you can use to edit the merge module database.</span></span>
2.  <span data-ttu-id="1642b-107">Obtenha um banco de dados de módulo de mesclagem em branco.</span><span class="sxs-lookup"><span data-stu-id="1642b-107">Obtain a blank merge module database.</span></span>
3.  <span data-ttu-id="1642b-108">Gere um [GUID](guid.md) para o módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1642b-108">Generate a [GUID](guid.md) for the merge module.</span></span> <span data-ttu-id="1642b-109">Você precisa usar esse GUID ao criar as chaves primárias das tabelas de banco de dados no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1642b-109">You need to use this GUID when authoring the primary keys of database tables in the merge module.</span></span>
4.  <span data-ttu-id="1642b-110">Adicione um registro à [tabela de componentes](component-table.md) para cada componente entregue pela mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1642b-110">Add a record to the [Component table](component-table.md) for each component delivered by the merge.</span></span> <span data-ttu-id="1642b-111">Uma tabela de componentes é necessária em cada módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1642b-111">A Component table is required in every merge module.</span></span> <span data-ttu-id="1642b-112">Observe que os módulos de mesclagem operam com componentes e não com recursos.</span><span class="sxs-lookup"><span data-stu-id="1642b-112">Note that merge modules operate with components and not with features.</span></span> <span data-ttu-id="1642b-113">Em alguns casos, no entanto, uma entrada de tabela de banco de dados pode precisar fazer referência a um recurso.</span><span class="sxs-lookup"><span data-stu-id="1642b-113">In certain cases, however, a database table entry may need to reference a feature.</span></span> <span data-ttu-id="1642b-114">Para obter detalhes, consulte [Referenciando recursos em módulos de mesclagem](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="1642b-114">For details, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>
5.  <span data-ttu-id="1642b-115">Adicione uma [tabela de diretórios](directory-table.md) ao módulo de mesclagem que especifica o layout dos diretórios que o módulo de mesclagem adiciona ao banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="1642b-115">Add a [Directory table](directory-table.md) to the merge module that specifies the layout of directories the merge module adds to the target database.</span></span> <span data-ttu-id="1642b-116">Uma tabela de diretório é necessária em cada módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1642b-116">A Directory table is required in every merge module.</span></span>
6.  <span data-ttu-id="1642b-117">Importe uma [tabela FeatureComponents](featurecomponents-table.md) em branco para o banco de dados do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1642b-117">Import a blank [FeatureComponents table](featurecomponents-table.md) into the merge module database.</span></span> <span data-ttu-id="1642b-118">Esta tabela vazia fornece uma diretriz para a ferramenta de mesclagem em casos em que o arquivo. msi não contém sua própria tabela FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="1642b-118">This empty table provides a guideline for the merge tool in cases where the .msi file does not contain its own FeatureComponents table.</span></span>
7.  <span data-ttu-id="1642b-119">Colete todos os arquivos entregues por esse módulo de mesclagem e crie o arquivo de gabinete [MergeModule.CABinet](mergemodule-cabinet.md) .</span><span class="sxs-lookup"><span data-stu-id="1642b-119">Collect all the files delivered by this merge module and create the [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file.</span></span> <span data-ttu-id="1642b-120">Adicione o gabinete ao módulo de mesclagem como um fluxo dentro do arquivo. msm.</span><span class="sxs-lookup"><span data-stu-id="1642b-120">Add the cabinet to the merge module as a stream inside the .msm file.</span></span>
8.  <span data-ttu-id="1642b-121">Adicione um registro à tabela de arquivos para cada arquivo armazenado no MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="1642b-121">Add a record to the File table for every file stored in MergeModule.CABinet.</span></span>
9.  <span data-ttu-id="1642b-122">Adicione as informações necessárias para identificar o módulo de mesclagem na [tabela ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="1642b-122">Add the information necessary to identify the merge module in the [ModuleSignature table](modulesignature-table.md).</span></span> <span data-ttu-id="1642b-123">Cada módulo de mesclagem requer uma tabela ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="1642b-123">Every merge module requires a ModuleSignature table.</span></span>
10. <span data-ttu-id="1642b-124">Liste os componentes no módulo mesclar na [tabela ModuleComponents](modulecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="1642b-124">List the components in the merge module in the [ModuleComponents table](modulecomponents-table.md).</span></span> <span data-ttu-id="1642b-125">Cada módulo de mesclagem requer uma tabela ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="1642b-125">Every merge module requires a ModuleComponents table.</span></span>
11. <span data-ttu-id="1642b-126">Adicione tabelas de sequência do módulo de mesclagem ao arquivo. msm somente se o módulo de mesclagem precisar modificar as [*tabelas de sequência*](s-gly.md) do banco de dados de instalação de destino.</span><span class="sxs-lookup"><span data-stu-id="1642b-126">Add merge module sequence tables to the .msm file only if the merge module needs to modify the [*sequence tables*](s-gly.md) of the target installation database.</span></span>
12. <span data-ttu-id="1642b-127">Adicione uma \_ tabela de validação ao módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1642b-127">Add a \_Validation table to the merge module.</span></span> <span data-ttu-id="1642b-128">Um módulo de mesclagem requer uma \_ tabela de validação para passar na validação.</span><span class="sxs-lookup"><span data-stu-id="1642b-128">A merge module requires a \_Validation table to pass validation.</span></span>
13. <span data-ttu-id="1642b-129">Os módulos de mesclagem exigem uma interface do usuário somente em casos raros.</span><span class="sxs-lookup"><span data-stu-id="1642b-129">Merge modules require a user interface in only rare cases.</span></span> <span data-ttu-id="1642b-130">Não é recomendável incluir uma interface do usuário com um módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1642b-130">Including a UI with a merge module is not recommended.</span></span> <span data-ttu-id="1642b-131">Nos casos em que uma interface de usuário é necessária, as tabelas de interface do usuário podem ser mescladas no arquivo. msi da mesma forma que outras tabelas.</span><span class="sxs-lookup"><span data-stu-id="1642b-131">In cases where a user interface is required, the UI tables can be merged into the .msi file the same as other tables.</span></span>
14. <span data-ttu-id="1642b-132">Adicione informações de registro às tabelas de registro apropriadas no banco de dados do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1642b-132">Add registry information to the appropriate registry tables in the merge module database.</span></span> <span data-ttu-id="1642b-133">Adicione informações de registro para bibliotecas de tipos, classes, extensões e verbos nas tabelas [TypeLib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [extensão](extension-table.md), [verbo](verb-table.md)ou [MIME](mime-table.md) .</span><span class="sxs-lookup"><span data-stu-id="1642b-133">Add registry information for type libraries, classes, extensions, and verbs into the [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="1642b-134">Todas as outras informações do registro podem entrar na [tabela do registro](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="1642b-134">All other registry information can go into the [Registry table](registry-table.md).</span></span> <span data-ttu-id="1642b-135">O uso da tabela SelfReg não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="1642b-135">The use of the SelfReg table is not recommended.</span></span>
15. <span data-ttu-id="1642b-136">Adicione as informações de resumo ao [fluxo de informações resumidas do módulo de mesclagem](merge-module-summary-information-stream-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1642b-136">Add the summary information to the [Merge Module Summary Information Stream](merge-module-summary-information-stream-reference.md).</span></span>
16. <span data-ttu-id="1642b-137">Execute a validação em todos os módulos de mesclagem antes de tentar instalar o.</span><span class="sxs-lookup"><span data-stu-id="1642b-137">Run validation on all merge modules before attempting to install.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1642b-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1642b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1642b-139">Obtendo bancos de dados de módulo de mesclagem em branco</span><span class="sxs-lookup"><span data-stu-id="1642b-139">Obtaining Blank Merge Module Databases</span></span>](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="1642b-140">Obtendo ferramentas de criação de módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-140">Obtaining Merge Module Authoring Tools</span></span>](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[<span data-ttu-id="1642b-141">Nomeando chaves primárias em bancos de dados do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-141">Naming Primary Keys in Merge Module Databases</span></span>](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="1642b-142">Criando tabelas de componentes do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-142">Authoring Merge Module Component Tables</span></span>](authoring-merge-module-component-tables.md)
</dt> <dt>

[<span data-ttu-id="1642b-143">Criando tabelas de diretório do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-143">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="1642b-144">Criando tabelas FeatureComponents do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-144">Authoring Merge Module FeatureComponents Tables</span></span>](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="1642b-145">Gerando MergeModule.CABarquivos de gabinete inet</span><span class="sxs-lookup"><span data-stu-id="1642b-145">Generating MergeModule.CABinet Cabinet Files</span></span>](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[<span data-ttu-id="1642b-146">Criando tabelas de arquivos do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-146">Authoring Merge Module File Tables</span></span>](authoring-merge-module-file-tables.md)
</dt> <dt>

[<span data-ttu-id="1642b-147">Criando tabelas ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="1642b-147">Authoring ModuleSignature Tables</span></span>](authoring-modulesignature-tables.md)
</dt> <dt>

[<span data-ttu-id="1642b-148">Criando tabelas ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="1642b-148">Authoring ModuleComponents Tables</span></span>](authoring-modulecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="1642b-149">Criando tabelas de sequências do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-149">Authoring Merge Module Sequence Tables</span></span>](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[<span data-ttu-id="1642b-150">Validando módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-150">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="1642b-151">Criando interfaces de usuário em módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-151">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="1642b-152">Criando tabelas de registro do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-152">Authoring Merge Module Registry Tables</span></span>](authoring-merge-module-registry-tables.md)
</dt> <dt>

[<span data-ttu-id="1642b-153">Criando fluxos de informações de resumo do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-153">Authoring Merge Module Summary Information Streams</span></span>](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[<span data-ttu-id="1642b-154">Referência de fluxo de informações de resumo do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-154">Merge Module Summary Information Stream Reference</span></span>](merge-module-summary-information-stream-reference.md)
</dt> <dt>

<span data-ttu-id="1642b-155">Validando módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="1642b-155">Validating Merge Modules</span></span>
</dt> <dt>

[<span data-ttu-id="1642b-156">Usando módulos de mesclagem de 64 bits</span><span class="sxs-lookup"><span data-stu-id="1642b-156">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



