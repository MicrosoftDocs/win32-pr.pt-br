---
description: ICE25 valida que um arquivo. msi satisfaz todas as suas dependências e exclusões do módulo de mesclagem interna.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828977"
---
# <a name="ice25"></a><span data-ttu-id="6c3cf-103">ICE25</span><span class="sxs-lookup"><span data-stu-id="6c3cf-103">ICE25</span></span>

<span data-ttu-id="6c3cf-104">ICE25 valida que um arquivo. msi satisfaz todas as suas dependências e exclusões do [módulo de mesclagem](merge-modules.md) interna.</span><span class="sxs-lookup"><span data-stu-id="6c3cf-104">ICE25 validates that a .msi file satisfies all of its internal [merge module](merge-modules.md) dependencies and exclusions.</span></span> <span data-ttu-id="6c3cf-105">O ICE valida o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6c3cf-105">ICE validates the following:</span></span>

-   <span data-ttu-id="6c3cf-106">Todas as dependências do módulo de mesclagem indicadas na [tabela ModuleDependency](moduledependency-table.md) do arquivo. msi são satisfeitas por pelo menos um módulo de mesclagem listado na [tabela ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="6c3cf-106">That all merge module dependencies indicated in the .msi file's [ModuleDependency table](moduledependency-table.md) are satisfied by at least one merge module listed in the [ModuleSignature table](modulesignature-table.md).</span></span>
-   <span data-ttu-id="6c3cf-107">Nenhum dos módulos de mesclagem excluídos na [tabela ModuleExclusion](moduleexclusion-table.md) é incompatível com os módulos de mesclagem listados na [tabela ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="6c3cf-107">That none of the excluded merge modules in the [ModuleExclusion table](moduleexclusion-table.md) are incompatible with the merge modules listed in the [ModuleSignature table](modulesignature-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="6c3cf-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="6c3cf-108">Result</span></span>

<span data-ttu-id="6c3cf-109">O ICE25 posta uma mensagem de erro se o arquivo. msi tiver sido mesclado anteriormente com um módulo de mesclagem incompatível ou se ele não tiver sido mesclado com um módulo de mesclagem necessário.</span><span class="sxs-lookup"><span data-stu-id="6c3cf-109">ICE25 posts an error message if .msi file has previously been merged with an incompatible merge module or if it has not been merged with a necessary merge module.</span></span>

## <a name="example"></a><span data-ttu-id="6c3cf-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6c3cf-110">Example</span></span>

<span data-ttu-id="6c3cf-111">ICE25 posta os erros a seguir para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="6c3cf-111">ICE25 posts the following errors for the example shown.</span></span>

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[<span data-ttu-id="6c3cf-112">Tabela ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="6c3cf-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="6c3cf-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="6c3cf-113">ModuleID</span></span> | <span data-ttu-id="6c3cf-114">Idioma</span><span class="sxs-lookup"><span data-stu-id="6c3cf-114">Language</span></span> | <span data-ttu-id="6c3cf-115">Versão</span><span class="sxs-lookup"><span data-stu-id="6c3cf-115">Version</span></span> |
|----------|----------|---------|
| <span data-ttu-id="6c3cf-116">Móduloa</span><span class="sxs-lookup"><span data-stu-id="6c3cf-116">ModuleA</span></span>  | <span data-ttu-id="6c3cf-117">0</span><span class="sxs-lookup"><span data-stu-id="6c3cf-117">0</span></span>        | <span data-ttu-id="6c3cf-118">1.0</span><span class="sxs-lookup"><span data-stu-id="6c3cf-118">1.0</span></span>     |
| <span data-ttu-id="6c3cf-119">ModuleB</span><span class="sxs-lookup"><span data-stu-id="6c3cf-119">ModuleB</span></span>  | <span data-ttu-id="6c3cf-120">1046</span><span class="sxs-lookup"><span data-stu-id="6c3cf-120">1033</span></span>     | <span data-ttu-id="6c3cf-121">1.0</span><span class="sxs-lookup"><span data-stu-id="6c3cf-121">1.0</span></span>     |



 

[<span data-ttu-id="6c3cf-122">Tabela ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="6c3cf-122">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="6c3cf-123">ModuleID</span><span class="sxs-lookup"><span data-stu-id="6c3cf-123">ModuleID</span></span> | <span data-ttu-id="6c3cf-124">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="6c3cf-124">ModuleLanguage</span></span> | <span data-ttu-id="6c3cf-125">Requeridoid</span><span class="sxs-lookup"><span data-stu-id="6c3cf-125">RequiredID</span></span> | <span data-ttu-id="6c3cf-126">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="6c3cf-126">RequiredLanguage</span></span> | <span data-ttu-id="6c3cf-127">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="6c3cf-127">RequiredVersion</span></span> |
|----------|----------------|------------|------------------|-----------------|
| <span data-ttu-id="6c3cf-128">Móduloa</span><span class="sxs-lookup"><span data-stu-id="6c3cf-128">ModuleA</span></span>  | <span data-ttu-id="6c3cf-129">0</span><span class="sxs-lookup"><span data-stu-id="6c3cf-129">0</span></span>              | <span data-ttu-id="6c3cf-130">ModuleX</span><span class="sxs-lookup"><span data-stu-id="6c3cf-130">ModuleX</span></span>    | <span data-ttu-id="6c3cf-131">0</span><span class="sxs-lookup"><span data-stu-id="6c3cf-131">0</span></span>                | <span data-ttu-id="6c3cf-132">2,0</span><span class="sxs-lookup"><span data-stu-id="6c3cf-132">2.0</span></span>             |



 

[<span data-ttu-id="6c3cf-133">Tabela ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="6c3cf-133">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="6c3cf-134">ModuleID</span><span class="sxs-lookup"><span data-stu-id="6c3cf-134">ModuleID</span></span> | <span data-ttu-id="6c3cf-135">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="6c3cf-135">ModuleLanguage</span></span> | <span data-ttu-id="6c3cf-136">Exclusão excluída</span><span class="sxs-lookup"><span data-stu-id="6c3cf-136">ExcludedID</span></span> | <span data-ttu-id="6c3cf-137">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="6c3cf-137">ExcludedLanguage</span></span> | <span data-ttu-id="6c3cf-138">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="6c3cf-138">ExcludedMinVersion</span></span> | <span data-ttu-id="6c3cf-139">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="6c3cf-139">ExcludedMaxVersion</span></span> |
|----------|----------------|------------|------------------|--------------------|--------------------|
| <span data-ttu-id="6c3cf-140">Móduloa</span><span class="sxs-lookup"><span data-stu-id="6c3cf-140">ModuleA</span></span>  | <span data-ttu-id="6c3cf-141">0</span><span class="sxs-lookup"><span data-stu-id="6c3cf-141">0</span></span>              | <span data-ttu-id="6c3cf-142">ModuleB</span><span class="sxs-lookup"><span data-stu-id="6c3cf-142">ModuleB</span></span>    | <span data-ttu-id="6c3cf-143">1046</span><span class="sxs-lookup"><span data-stu-id="6c3cf-143">1033</span></span>             |                    |                    |



 

## <a name="related-topics"></a><span data-ttu-id="6c3cf-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c3cf-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c3cf-145">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="6c3cf-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



