---
description: ICEM02 verifica se todas as dependências e exclusões do módulo estão relacionadas ao módulo atual.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164831"
---
# <a name="icem02"></a><span data-ttu-id="013ef-103">ICEM02</span><span class="sxs-lookup"><span data-stu-id="013ef-103">ICEM02</span></span>

<span data-ttu-id="013ef-104">ICEM02 verifica se todas as dependências e exclusões do módulo estão relacionadas ao módulo atual.</span><span class="sxs-lookup"><span data-stu-id="013ef-104">ICEM02 verifies that all the module dependencies and exclusions are related to the current module.</span></span>

<span data-ttu-id="013ef-105">O módulo de mesclagem ICEs é armazenado em um arquivo. Cub do módulo de mesclagem chamado Mergemod. Cub e não no arquivo. Cub que contém a ICEs usada para a validação do pacote.</span><span class="sxs-lookup"><span data-stu-id="013ef-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="013ef-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="013ef-106">Result</span></span>

<span data-ttu-id="013ef-107">O ICEM02 posta mensagens de erro se o banco de dados do módulo tentar especificar dependências ou exclusões que não estão relacionadas ao módulo atual.</span><span class="sxs-lookup"><span data-stu-id="013ef-107">ICEM02 posts error messages if the module database attempts to specify dependencies or exclusions that do not relate to the current module.</span></span> <span data-ttu-id="013ef-108">ICEM02 posta uma mensagem de erro se o banco de dados do módulo tentar especificar o módulo atual como dependente ou excluído por si só.</span><span class="sxs-lookup"><span data-stu-id="013ef-108">ICEM02 posts an error message if the module database attempts to specify the current module as dependent or as excluded by itself.</span></span>

## <a name="example"></a><span data-ttu-id="013ef-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="013ef-109">Example</span></span>

<span data-ttu-id="013ef-110">ICEM02 postaria as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="013ef-110">ICEM02 would post the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[<span data-ttu-id="013ef-111">Tabela ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="013ef-111">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="013ef-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="013ef-112">ModuleID</span></span>         | <span data-ttu-id="013ef-113">Idioma</span><span class="sxs-lookup"><span data-stu-id="013ef-113">Language</span></span> | <span data-ttu-id="013ef-114">Versão</span><span class="sxs-lookup"><span data-stu-id="013ef-114">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="013ef-115">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="013ef-115">MyModule.*GUID1*</span></span> | <span data-ttu-id="013ef-116">1046</span><span class="sxs-lookup"><span data-stu-id="013ef-116">1033</span></span>     | <span data-ttu-id="013ef-117">1.0</span><span class="sxs-lookup"><span data-stu-id="013ef-117">1.0</span></span>     |



 

[<span data-ttu-id="013ef-118">Tabela ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="013ef-118">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="013ef-119">ModuleID</span><span class="sxs-lookup"><span data-stu-id="013ef-119">ModuleID</span></span>            | <span data-ttu-id="013ef-120">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="013ef-120">ModuleLanguage</span></span> | <span data-ttu-id="013ef-121">Requeridoid</span><span class="sxs-lookup"><span data-stu-id="013ef-121">RequiredID</span></span>          | <span data-ttu-id="013ef-122">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="013ef-122">RequiredLanguage</span></span> | <span data-ttu-id="013ef-123">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="013ef-123">RequiredVersion</span></span> |
|---------------------|----------------|---------------------|------------------|-----------------|
| <span data-ttu-id="013ef-124">OtherModule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="013ef-124">OtherModule.*GUID2*</span></span> | <span data-ttu-id="013ef-125">1046</span><span class="sxs-lookup"><span data-stu-id="013ef-125">1033</span></span>           | <span data-ttu-id="013ef-126">OtherModule. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="013ef-126">OtherModule.*GUID3*</span></span> | <span data-ttu-id="013ef-127">0</span><span class="sxs-lookup"><span data-stu-id="013ef-127">0</span></span>                | <span data-ttu-id="013ef-128">1.0</span><span class="sxs-lookup"><span data-stu-id="013ef-128">1.0</span></span>             |
| <span data-ttu-id="013ef-129">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="013ef-129">MyModule.*GUID1*</span></span>    | <span data-ttu-id="013ef-130">1046</span><span class="sxs-lookup"><span data-stu-id="013ef-130">1033</span></span>           | <span data-ttu-id="013ef-131">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="013ef-131">MyModule.*GUID1*</span></span>    | <span data-ttu-id="013ef-132">1046</span><span class="sxs-lookup"><span data-stu-id="013ef-132">1033</span></span>             | <span data-ttu-id="013ef-133">1.2</span><span class="sxs-lookup"><span data-stu-id="013ef-133">1.2</span></span>             |



 

<span data-ttu-id="013ef-134">[Tabela ModuleExclusion](moduleexclusion-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="013ef-134">[ModuleExclusion Table](moduleexclusion-table.md) (partial)</span></span>



| <span data-ttu-id="013ef-135">ModuleID</span><span class="sxs-lookup"><span data-stu-id="013ef-135">ModuleID</span></span>            | <span data-ttu-id="013ef-136">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="013ef-136">ModuleLanguage</span></span> | <span data-ttu-id="013ef-137">Exclusão excluída</span><span class="sxs-lookup"><span data-stu-id="013ef-137">ExcludedID</span></span>          | <span data-ttu-id="013ef-138">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="013ef-138">ExcludedLanguage</span></span> |
|---------------------|----------------|---------------------|------------------|
| <span data-ttu-id="013ef-139">OtherModule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="013ef-139">OtherModule.*GUID2*</span></span> | <span data-ttu-id="013ef-140">1046</span><span class="sxs-lookup"><span data-stu-id="013ef-140">1033</span></span>           | <span data-ttu-id="013ef-141">OtherModule. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="013ef-141">OtherModule.*GUID3*</span></span> | <span data-ttu-id="013ef-142">0</span><span class="sxs-lookup"><span data-stu-id="013ef-142">0</span></span>                |
| <span data-ttu-id="013ef-143">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="013ef-143">MyModule.*GUID1*</span></span>    | <span data-ttu-id="013ef-144">1046</span><span class="sxs-lookup"><span data-stu-id="013ef-144">1033</span></span>           | <span data-ttu-id="013ef-145">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="013ef-145">MyModule.*GUID1*</span></span>    | <span data-ttu-id="013ef-146">1046</span><span class="sxs-lookup"><span data-stu-id="013ef-146">1033</span></span>             |



 

<span data-ttu-id="013ef-147">O ICE do módulo de mesclagem lança o primeiro erro porque a da primeira linha na tabela ModuleDependency, que não especifica uma dependência necessária para o módulo atual especificado na tabela ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="013ef-147">The merge module ICE posts the first error because the of the first row in the ModuleDependency table, which does not specify a required dependency for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="013ef-148">As dependências de um módulo só podem ser especificadas em sua própria tabela ModuleDependency.</span><span class="sxs-lookup"><span data-stu-id="013ef-148">The dependencies of a module can only be specified in its own ModuleDependency table.</span></span> <span data-ttu-id="013ef-149">Se OtherModule. *GUID3* é exigido pelo módulo atual, substitua as duas primeiras colunas da linha pelos dados da tabela ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="013ef-149">If OtherModule.*GUID3* is required by the current module, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="013ef-150">Se OtherModule. *GUID3* não é exigido por este módulo, exclua esta linha.</span><span class="sxs-lookup"><span data-stu-id="013ef-150">If OtherModule.*GUID3* is not required by this module, delete this row.</span></span>

<span data-ttu-id="013ef-151">O ICE do módulo de mesclagem lança o segundo erro porque um módulo não pode especificar uma dependência em si mesmo.</span><span class="sxs-lookup"><span data-stu-id="013ef-151">The merge module ICE posts the second error because a module cannot specify a dependency upon itself.</span></span>

<span data-ttu-id="013ef-152">O ICE do módulo de mesclagem posta o terceiro erro devido à primeira linha na tabela ModuleExclusion, que não especifica uma exclusão necessária para o módulo atual especificado na tabela ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="013ef-152">The merge module ICE posts the third error because of the first row in the ModuleExclusion table, which does not specify a required exclusion for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="013ef-153">As exclusões de um módulo só podem ser especificadas em sua própria tabela ModuleExclusion.</span><span class="sxs-lookup"><span data-stu-id="013ef-153">The exclusions of a module can only be specified in its own ModuleExclusion table.</span></span> <span data-ttu-id="013ef-154">Se o módulo atual excluir OtherModule. *GUID3*, substitua as duas primeiras colunas da linha pelos dados da tabela ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="013ef-154">If the current module excludes OtherModule.*GUID3*, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="013ef-155">Se o módulo atual não excluir OtherModule. *GUID3*, exclua esta linha.</span><span class="sxs-lookup"><span data-stu-id="013ef-155">If the current module does not exclude OtherModule.*GUID3*, delete this row.</span></span>

<span data-ttu-id="013ef-156">O ICE do módulo de mesclagem posta o quarto erro, pois um módulo não pode especificar que ele seja excluído.</span><span class="sxs-lookup"><span data-stu-id="013ef-156">The merge module ICE posts the fourth error because a module cannot specify that it exclude itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="013ef-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="013ef-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="013ef-158">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="013ef-158">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



