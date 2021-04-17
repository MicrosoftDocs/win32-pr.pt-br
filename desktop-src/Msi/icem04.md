---
description: ICEM04 verifica se as tabelas vazias necessárias do módulo de mesclagem estão vazias. Falha ao corrigir um erro que os relatórios de ICEM04 podem resultar na mesclagem incorreta do módulo de mesclagem.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ef993690ae690e0651db1538196998c4dd28c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752648"
---
# <a name="icem04"></a><span data-ttu-id="563cc-104">ICEM04</span><span class="sxs-lookup"><span data-stu-id="563cc-104">ICEM04</span></span>

<span data-ttu-id="563cc-105">ICEM04 verifica se as tabelas vazias necessárias do módulo de mesclagem estão vazias.</span><span class="sxs-lookup"><span data-stu-id="563cc-105">ICEM04 verifies that the merge module's required empty tables are empty.</span></span> <span data-ttu-id="563cc-106">Falha ao corrigir um erro que os relatórios de ICEM04 podem resultar na mesclagem incorreta do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="563cc-106">Failure to fix an error that ICEM04 reports can result in incorrect merging of the merge module.</span></span>

## <a name="result"></a><span data-ttu-id="563cc-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="563cc-107">Result</span></span>

<span data-ttu-id="563cc-108">ICEM04 posta um erro quando as tabelas vazias necessárias do módulo de mesclagem não estão vazias.</span><span class="sxs-lookup"><span data-stu-id="563cc-108">ICEM04 posts an error when the merge module's required empty tables are not empty.</span></span>

## <a name="example"></a><span data-ttu-id="563cc-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="563cc-109">Example</span></span>

<span data-ttu-id="563cc-110">ICEM04 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas.</span><span class="sxs-lookup"><span data-stu-id="563cc-110">ICEM04 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

<span data-ttu-id="563cc-111">A tabela a seguir mostra uma [tabela AdvtExecuteSequence](advtexecutesequence-table.md)parcial.</span><span class="sxs-lookup"><span data-stu-id="563cc-111">The following table shows you a partial [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>



| <span data-ttu-id="563cc-112">Ação</span><span class="sxs-lookup"><span data-stu-id="563cc-112">Action</span></span>         | <span data-ttu-id="563cc-113">Sequência</span><span class="sxs-lookup"><span data-stu-id="563cc-113">Sequence</span></span> |
|----------------|----------|
| <span data-ttu-id="563cc-114">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="563cc-114">CostInitialize</span></span> | <span data-ttu-id="563cc-115">1</span><span class="sxs-lookup"><span data-stu-id="563cc-115">1</span></span>        |



 

<span data-ttu-id="563cc-116">A lista a seguir mostra o conteúdo parcial de MergeModule:</span><span class="sxs-lookup"><span data-stu-id="563cc-116">The following list shows you the partial contents of MergeModule:</span></span>

-   <span data-ttu-id="563cc-117">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="563cc-117">ModuleInstallExecuteSequence</span></span>
-   <span data-ttu-id="563cc-118">ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="563cc-118">ModuleAdvtExecuteSequence</span></span>
-   <span data-ttu-id="563cc-119">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="563cc-119">InstallUISequence</span></span>

<span data-ttu-id="563cc-120">O exemplo a seguir mostra outro erro possível.</span><span class="sxs-lookup"><span data-stu-id="563cc-120">The following example shows you another possible error.</span></span>

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

<span data-ttu-id="563cc-121">Se um módulo de mesclagem contiver uma tabela de sequência de módulo, ela deverá conter a tabela de sequência vazia correspondente, independentemente de a tabela de sequência de módulo estar vazia ou não.</span><span class="sxs-lookup"><span data-stu-id="563cc-121">If a merge module contains a module sequence table, it must contain the corresponding empty sequence table, whether or not the module sequence table is empty.</span></span> <span data-ttu-id="563cc-122">Por exemplo, se o módulo de mesclagem contiver a [tabela ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), ela também deverá conter uma tabela AdminExecuteSequence vazia.</span><span class="sxs-lookup"><span data-stu-id="563cc-122">For example, if the merge module contains the [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), it must also contain an empty AdminExecuteSequence table.</span></span>

<span data-ttu-id="563cc-123">A [tabela FeatureComponents](featurecomponents-table.md) é necessária em todos os módulos de mesclagem e deve estar vazia.</span><span class="sxs-lookup"><span data-stu-id="563cc-123">The [FeatureComponents Table](featurecomponents-table.md) is required in all merge modules and must be empty.</span></span>

<span data-ttu-id="563cc-124">O procedimento a seguir mostra como corrigir erros.</span><span class="sxs-lookup"><span data-stu-id="563cc-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="563cc-125">**Para corrigir erros**</span><span class="sxs-lookup"><span data-stu-id="563cc-125">**To fix errors**</span></span>

1.  <span data-ttu-id="563cc-126">Adicione uma [tabela FeatureComponents](featurecomponents-table.md) vazia ao módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="563cc-126">Add an empty [FeatureComponents Table](featurecomponents-table.md) to the merge module.</span></span>
2.  <span data-ttu-id="563cc-127">Adicione uma [tabela InstallExecuteSequence](installexecutesequence-table.md) vazia ao módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="563cc-127">Add an empty [InstallExecuteSequence Table](installexecutesequence-table.md) to the merge module.</span></span>
3.  <span data-ttu-id="563cc-128">Remova a ação ' CostInitialize ' da [tabela AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="563cc-128">Remove the 'CostInitialize' action from the [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="563cc-129">Essa tabela deve estar vazia em um módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="563cc-129">This table must be empty in a merge module.</span></span> <span data-ttu-id="563cc-130">As ações só devem aparecer na tabela ModuleAdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="563cc-130">Actions should only appear in the ModuleAdvtExecuteSequence table.</span></span>

     

## <a name="tables-used-during-execution"></a><span data-ttu-id="563cc-131">Tabelas usadas durante a execução</span><span class="sxs-lookup"><span data-stu-id="563cc-131">Tables Used During Execution</span></span>

<span data-ttu-id="563cc-132">A lista a seguir identifica as tabelas que são usadas durante a execução:</span><span class="sxs-lookup"><span data-stu-id="563cc-132">The following list identifies the tables that are used during execution:</span></span>

-   [<span data-ttu-id="563cc-133">Tabela FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="563cc-133">FeatureComponents Table</span></span>](featurecomponents-table.md)
-   <span data-ttu-id="563cc-134">\*Tabelas de sequência de módulo e \* tabelas de sequência correspondentes.</span><span class="sxs-lookup"><span data-stu-id="563cc-134">Module\*Sequence tables and corresponding \*Sequence tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="563cc-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="563cc-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="563cc-136">Sobre módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="563cc-136">About Merge Modules</span></span>](about-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="563cc-137">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="563cc-137">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



