---
description: A tabela ModuleDependency mantém uma lista de outros módulos de mesclagem que são necessários para que esse módulo de mesclagem opere corretamente.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Tabela ModuleDependency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758774"
---
# <a name="moduledependency-table"></a><span data-ttu-id="8dd4d-103">Tabela ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="8dd4d-103">ModuleDependency Table</span></span>

<span data-ttu-id="8dd4d-104">A tabela ModuleDependency mantém uma lista de outros módulos de mesclagem que são necessários para que esse módulo de mesclagem opere corretamente.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-104">The ModuleDependency table keeps a list of other merge modules that are required for this merge module to operate properly.</span></span> <span data-ttu-id="8dd4d-105">Esta tabela habilita uma ferramenta de mesclagem ou verificação para garantir que os módulos de mesclagem necessários sejam incluídos no banco de dados do instalador do usuário.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-105">This table enables a merge or verification tool to ensure that the necessary merge modules are in fact included in the user's installer database.</span></span> <span data-ttu-id="8dd4d-106">A ferramenta verifica através da referência cruzada desta tabela com a tabela ModuleSignature no banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-106">The tool checks by cross referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="8dd4d-107">A tabela ModuleDependency tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-107">The ModuleDependency table has the following columns.</span></span>



| <span data-ttu-id="8dd4d-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="8dd4d-108">Column</span></span>           | <span data-ttu-id="8dd4d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8dd4d-109">Type</span></span>                         | <span data-ttu-id="8dd4d-110">Chave</span><span class="sxs-lookup"><span data-stu-id="8dd4d-110">Key</span></span> | <span data-ttu-id="8dd4d-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="8dd4d-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="8dd4d-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="8dd4d-112">ModuleID</span></span>         | [<span data-ttu-id="8dd4d-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="8dd4d-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="8dd4d-114">S</span><span class="sxs-lookup"><span data-stu-id="8dd4d-114">Y</span></span>   | <span data-ttu-id="8dd4d-115">N</span><span class="sxs-lookup"><span data-stu-id="8dd4d-115">N</span></span>        |
| <span data-ttu-id="8dd4d-116">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="8dd4d-116">ModuleLanguage</span></span>   | [<span data-ttu-id="8dd4d-117">Inteiro</span><span class="sxs-lookup"><span data-stu-id="8dd4d-117">Integer</span></span>](integer.md)       | <span data-ttu-id="8dd4d-118">S</span><span class="sxs-lookup"><span data-stu-id="8dd4d-118">Y</span></span>   | <span data-ttu-id="8dd4d-119">N</span><span class="sxs-lookup"><span data-stu-id="8dd4d-119">N</span></span>        |
| <span data-ttu-id="8dd4d-120">Requeridoid</span><span class="sxs-lookup"><span data-stu-id="8dd4d-120">RequiredID</span></span>       | [<span data-ttu-id="8dd4d-121">Identificador</span><span class="sxs-lookup"><span data-stu-id="8dd4d-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="8dd4d-122">S</span><span class="sxs-lookup"><span data-stu-id="8dd4d-122">Y</span></span>   | <span data-ttu-id="8dd4d-123">N</span><span class="sxs-lookup"><span data-stu-id="8dd4d-123">N</span></span>        |
| <span data-ttu-id="8dd4d-124">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="8dd4d-124">RequiredLanguage</span></span> | [<span data-ttu-id="8dd4d-125">Inteiro</span><span class="sxs-lookup"><span data-stu-id="8dd4d-125">Integer</span></span>](integer.md)       | <span data-ttu-id="8dd4d-126">S</span><span class="sxs-lookup"><span data-stu-id="8dd4d-126">Y</span></span>   | <span data-ttu-id="8dd4d-127">N</span><span class="sxs-lookup"><span data-stu-id="8dd4d-127">N</span></span>        |
| <span data-ttu-id="8dd4d-128">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="8dd4d-128">RequiredVersion</span></span>  | [<span data-ttu-id="8dd4d-129">Versão</span><span class="sxs-lookup"><span data-stu-id="8dd4d-129">Version</span></span>](version.md)       |     | <span data-ttu-id="8dd4d-130">S</span><span class="sxs-lookup"><span data-stu-id="8dd4d-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8dd4d-131">Colunas</span><span class="sxs-lookup"><span data-stu-id="8dd4d-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8dd4d-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="8dd4d-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="8dd4d-133">Identificador do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-133">Identifier of the merge module.</span></span> <span data-ttu-id="8dd4d-134">Essa é uma chave estrangeira na [tabela ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8dd4d-134">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dd4d-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="8dd4d-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="8dd4d-136">ID de idioma decimal do módulo de mesclagem em ModuleID.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-136">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="8dd4d-137">Essa é uma chave estrangeira na [tabela ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8dd4d-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dd4d-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>Requeridoid</span><span class="sxs-lookup"><span data-stu-id="8dd4d-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID</span></span>
</dt> <dd>

<span data-ttu-id="8dd4d-139">Identificador do módulo de mesclagem exigido pelo módulo de mesclagem em ModuleID.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-139">Identifier of the merge module required by the merge module in ModuleID.</span></span>

</dd> <dt>

<span data-ttu-id="8dd4d-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="8dd4d-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span></span>
</dt> <dd>

<span data-ttu-id="8dd4d-141">ID de idioma numérico do módulo de mesclagem em requeridoid.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-141">Numeric language ID of the merge module in RequiredID.</span></span> <span data-ttu-id="8dd4d-142">A coluna RequiredLanguage pode especificar a ID de idioma para um único idioma, como 1033 para inglês americano, ou especificar a ID de idioma para um grupo de idiomas, como 9 para qualquer inglês.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-142">The RequiredLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="8dd4d-143">Se o campo contiver uma ID de idioma de grupo, qualquer módulo de mesclagem com um código de idioma nesse grupo satisfizer a dependência.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-143">If the field contains a group language ID, any merge module with having a language code in that group satisfies the dependency.</span></span> <span data-ttu-id="8dd4d-144">Se o RequiredLanguage for definido como 0, qualquer módulo de mesclagem preenchendo os outros requisitos atenderá à dependência.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-144">If the RequiredLanguage is set to 0, any merge module filling the other requirements satisfies the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="8dd4d-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="8dd4d-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span></span>
</dt> <dd>

<span data-ttu-id="8dd4d-146">Versão do módulo de mesclagem em requeridoid.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-146">Version of the merge module in RequiredID.</span></span> <span data-ttu-id="8dd4d-147">Se esse campo for nulo, qualquer versão preencherá a dependência.</span><span class="sxs-lookup"><span data-stu-id="8dd4d-147">If this field is Null, any version fills the dependency.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="8dd4d-148">Validação</span><span class="sxs-lookup"><span data-stu-id="8dd4d-148">Validation</span></span>

<dl>

[<span data-ttu-id="8dd4d-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="8dd4d-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8dd4d-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="8dd4d-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8dd4d-151">ICE25</span><span class="sxs-lookup"><span data-stu-id="8dd4d-151">ICE25</span></span>](ice25.md)  
</dl>

 

 



