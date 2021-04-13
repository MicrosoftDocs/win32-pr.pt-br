---
description: A tabela ModuleExclusion mantém uma lista de outros módulos de mesclagem que são incompatíveis no mesmo banco de dados do instalador.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Tabela ModuleExclusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370761"
---
# <a name="moduleexclusion-table"></a><span data-ttu-id="d3415-103">Tabela ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="d3415-103">ModuleExclusion Table</span></span>

<span data-ttu-id="d3415-104">A tabela ModuleExclusion mantém uma lista de outros módulos de mesclagem que são incompatíveis no mesmo banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="d3415-104">The ModuleExclusion table keeps a list of other merge modules that are incompatible in the same installer database.</span></span> <span data-ttu-id="d3415-105">Esta tabela permite que uma ferramenta de mesclagem ou verificação Verifique se os módulos de mesclagem conflitantes não são mesclados no banco de dados do instalador do usuário.</span><span class="sxs-lookup"><span data-stu-id="d3415-105">This table enables a merge or verification tool to check that conflicting merge modules are not merged in the user's installer database.</span></span> <span data-ttu-id="d3415-106">A ferramenta verifica através da referência cruzada desta tabela com a tabela ModuleSignature no banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="d3415-106">The tool checks by cross-referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="d3415-107">A tabela ModuleExclusion tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3415-107">The ModuleExclusion table has the following columns.</span></span>



| <span data-ttu-id="d3415-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="d3415-108">Column</span></span>             | <span data-ttu-id="d3415-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3415-109">Type</span></span>                         | <span data-ttu-id="d3415-110">Chave</span><span class="sxs-lookup"><span data-stu-id="d3415-110">Key</span></span> | <span data-ttu-id="d3415-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="d3415-111">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="d3415-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="d3415-112">ModuleID</span></span>           | [<span data-ttu-id="d3415-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="d3415-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="d3415-114">S</span><span class="sxs-lookup"><span data-stu-id="d3415-114">Y</span></span>   | <span data-ttu-id="d3415-115">N</span><span class="sxs-lookup"><span data-stu-id="d3415-115">N</span></span>        |
| <span data-ttu-id="d3415-116">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="d3415-116">ModuleLanguage</span></span>     | [<span data-ttu-id="d3415-117">Inteiro</span><span class="sxs-lookup"><span data-stu-id="d3415-117">Integer</span></span>](integer.md)       | <span data-ttu-id="d3415-118">S</span><span class="sxs-lookup"><span data-stu-id="d3415-118">Y</span></span>   | <span data-ttu-id="d3415-119">N</span><span class="sxs-lookup"><span data-stu-id="d3415-119">N</span></span>        |
| <span data-ttu-id="d3415-120">Exclusão excluída</span><span class="sxs-lookup"><span data-stu-id="d3415-120">ExcludedID</span></span>         | [<span data-ttu-id="d3415-121">Identificador</span><span class="sxs-lookup"><span data-stu-id="d3415-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="d3415-122">S</span><span class="sxs-lookup"><span data-stu-id="d3415-122">Y</span></span>   | <span data-ttu-id="d3415-123">N</span><span class="sxs-lookup"><span data-stu-id="d3415-123">N</span></span>        |
| <span data-ttu-id="d3415-124">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="d3415-124">ExcludedLanguage</span></span>   | [<span data-ttu-id="d3415-125">Inteiro</span><span class="sxs-lookup"><span data-stu-id="d3415-125">Integer</span></span>](integer.md)       | <span data-ttu-id="d3415-126">S</span><span class="sxs-lookup"><span data-stu-id="d3415-126">Y</span></span>   | <span data-ttu-id="d3415-127">N</span><span class="sxs-lookup"><span data-stu-id="d3415-127">N</span></span>        |
| <span data-ttu-id="d3415-128">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="d3415-128">ExcludedMinVersion</span></span> | [<span data-ttu-id="d3415-129">Versão</span><span class="sxs-lookup"><span data-stu-id="d3415-129">Version</span></span>](version.md)       |     | <span data-ttu-id="d3415-130">S</span><span class="sxs-lookup"><span data-stu-id="d3415-130">Y</span></span>        |
| <span data-ttu-id="d3415-131">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="d3415-131">ExcludedMaxVersion</span></span> | [<span data-ttu-id="d3415-132">Versão</span><span class="sxs-lookup"><span data-stu-id="d3415-132">Version</span></span>](version.md)       |     | <span data-ttu-id="d3415-133">S</span><span class="sxs-lookup"><span data-stu-id="d3415-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d3415-134">Colunas</span><span class="sxs-lookup"><span data-stu-id="d3415-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d3415-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="d3415-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="d3415-136">Identificador do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="d3415-136">Identifier of the merge module.</span></span> <span data-ttu-id="d3415-137">Essa é uma chave estrangeira na [tabela ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="d3415-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3415-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="d3415-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="d3415-139">ID de idioma decimal do módulo de mesclagem em ModuleID.</span><span class="sxs-lookup"><span data-stu-id="d3415-139">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="d3415-140">Essa é uma chave estrangeira na [tabela ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="d3415-140">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3415-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>Exclusão excluída</span><span class="sxs-lookup"><span data-stu-id="d3415-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID</span></span>
</dt> <dd>

<span data-ttu-id="d3415-142">Identificador de um módulo de mesclagem excluído.</span><span class="sxs-lookup"><span data-stu-id="d3415-142">Identifier of an excluded merge module.</span></span>

</dd> <dt>

<span data-ttu-id="d3415-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="d3415-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span></span>
</dt> <dd>

<span data-ttu-id="d3415-144">ID de idioma numérico do módulo de mesclagem em Excluídoid.</span><span class="sxs-lookup"><span data-stu-id="d3415-144">Numeric language ID of the merge module in ExcludedID.</span></span> <span data-ttu-id="d3415-145">A coluna ExcludedLanguage pode especificar a ID de idioma para um único idioma, como 1033 para inglês americano, ou especificar a ID de idioma para um grupo de idiomas, como 9 para qualquer inglês.</span><span class="sxs-lookup"><span data-stu-id="d3415-145">The ExcludedLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="d3415-146">A coluna ExcludedLanguage pode aceitar IDs de idioma negativas.</span><span class="sxs-lookup"><span data-stu-id="d3415-146">The ExcludedLanguage column can accept negative language IDs.</span></span> <span data-ttu-id="d3415-147">O significado do valor na coluna ExcludedLanguage é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="d3415-147">The meaning of the value in the ExcludedLanguage column is as follows.</span></span>



| <span data-ttu-id="d3415-148">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="d3415-148">ExcludedLanguage</span></span> | <span data-ttu-id="d3415-149">Significado</span><span class="sxs-lookup"><span data-stu-id="d3415-149">Meaning</span></span>                                                              |
|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="d3415-150">> 0</span><span class="sxs-lookup"><span data-stu-id="d3415-150">> 0</span></span>           | <span data-ttu-id="d3415-151">Exclua as IDs de idioma especificadas por ExcludedLanguage.</span><span class="sxs-lookup"><span data-stu-id="d3415-151">Exclude the language IDs specified by ExcludedLanguage.</span></span>              |
| <span data-ttu-id="d3415-152">= 0</span><span class="sxs-lookup"><span data-stu-id="d3415-152">= 0</span></span>              | <span data-ttu-id="d3415-153">Não exclua nenhuma ID de idioma.</span><span class="sxs-lookup"><span data-stu-id="d3415-153">Exclude no language IDs.</span></span>                                             |
| <span data-ttu-id="d3415-154">< 0</span><span class="sxs-lookup"><span data-stu-id="d3415-154">< 0</span></span>           | <span data-ttu-id="d3415-155">Exclua todas as IDs de idioma, exceto aquelas especificadas por ExcludedLanguage.</span><span class="sxs-lookup"><span data-stu-id="d3415-155">Exclude all language IDs except those specified by ExcludedLanguage.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d3415-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="d3415-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span></span>
</dt> <dd>

<span data-ttu-id="d3415-157">Versão mínima excluída de um intervalo.</span><span class="sxs-lookup"><span data-stu-id="d3415-157">Minimum version excluded from a range.</span></span> <span data-ttu-id="d3415-158">Se o campo ExcludedMinVersion for nulo, todas as versões antes de ExcludedMaxVersion serão excluídas.</span><span class="sxs-lookup"><span data-stu-id="d3415-158">If the ExcludedMinVersion field is Null, all versions before ExcludedMaxVersion are excluded.</span></span> <span data-ttu-id="d3415-159">Se ExcludedMinVersion e ExcludedMaxVersion forem nulos, não haverá nenhuma exclusão com base na versão.</span><span class="sxs-lookup"><span data-stu-id="d3415-159">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> <dt>

<span data-ttu-id="d3415-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="d3415-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="d3415-161">Versão máxima excluída de um intervalo.</span><span class="sxs-lookup"><span data-stu-id="d3415-161">Maximum version excluded from a range.</span></span> <span data-ttu-id="d3415-162">Se o campo ExcludedMaxVersion for nulo, todas as versões após ExcludedMinVersion serão excluídas.</span><span class="sxs-lookup"><span data-stu-id="d3415-162">If the ExcludedMaxVersion field is Null, all versions after ExcludedMinVersion are excluded.</span></span> <span data-ttu-id="d3415-163">Se ExcludedMinVersion e ExcludedMaxVersion forem nulos, não haverá nenhuma exclusão com base na versão.</span><span class="sxs-lookup"><span data-stu-id="d3415-163">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="d3415-164">Validação</span><span class="sxs-lookup"><span data-stu-id="d3415-164">Validation</span></span>

<dl>

[<span data-ttu-id="d3415-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="d3415-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d3415-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="d3415-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d3415-167">ICE25</span><span class="sxs-lookup"><span data-stu-id="d3415-167">ICE25</span></span>](ice25.md)  
</dl>

 

 



