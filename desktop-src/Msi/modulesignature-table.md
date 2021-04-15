---
description: A tabela ModuleSignature é uma tabela necessária.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: Tabela ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505924"
---
# <a name="modulesignature-table"></a><span data-ttu-id="8c820-103">Tabela ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="8c820-103">ModuleSignature Table</span></span>

<span data-ttu-id="8c820-104">A tabela ModuleSignature é uma tabela necessária.</span><span class="sxs-lookup"><span data-stu-id="8c820-104">The ModuleSignature Table is a required table.</span></span> <span data-ttu-id="8c820-105">Ele contém todas as informações necessárias para identificar um módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8c820-105">It contains all the information necessary to identify a merge module.</span></span> <span data-ttu-id="8c820-106">A ferramenta de mesclagem adicionará essa tabela ao arquivo. msi se ainda não existir uma.</span><span class="sxs-lookup"><span data-stu-id="8c820-106">The merge tool adds this table to the .msi file if one does not already exist.</span></span> <span data-ttu-id="8c820-107">A tabela ModuleSignature em um módulo de mesclagem tem apenas uma linha que contém ModuleID, idioma e versão.</span><span class="sxs-lookup"><span data-stu-id="8c820-107">The ModuleSignature table in a merge module has only one row containing the ModuleID, Language, and Version.</span></span> <span data-ttu-id="8c820-108">No entanto, a tabela ModuleSignature em um arquivo. msi tem uma linha que contém essas informações para cada arquivo. msm que foi mesclado nela.</span><span class="sxs-lookup"><span data-stu-id="8c820-108">However, the ModuleSignature table in an .msi file has a row containing this information for each .msm file that has been merged into it.</span></span>

<span data-ttu-id="8c820-109">Ferramentas de mesclagem e verificação Verifique a tabela ModuleSignature em arquivos. msi para determinar se ele tem todos os módulos de mesclagem dependentes exigidos pelo módulo de mesclagem atual (consulte a [tabela ModuleDependency](moduledependency-table.md)) e se o pacote de instalação foi mesclado anteriormente com quaisquer módulos de mesclagem conflitantes (consulte a [tabela ModuleExclusion](moduleexclusion-table.md)).</span><span class="sxs-lookup"><span data-stu-id="8c820-109">Merge and verification tools check the ModuleSignature table in .msi files to determine if it has all of the dependent merge modules required by the current merge module (see [ModuleDependency Table](moduledependency-table.md)) and whether the installation package was previously merged with any conflicting merge modules (see [ModuleExclusion Table](moduleexclusion-table.md)).</span></span>

<span data-ttu-id="8c820-110">A tabela ModuleSignature tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c820-110">The ModuleSignature table has the following columns.</span></span>



| <span data-ttu-id="8c820-111">Coluna</span><span class="sxs-lookup"><span data-stu-id="8c820-111">Column</span></span>   | <span data-ttu-id="8c820-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c820-112">Type</span></span>                         | <span data-ttu-id="8c820-113">Chave</span><span class="sxs-lookup"><span data-stu-id="8c820-113">Key</span></span> | <span data-ttu-id="8c820-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="8c820-114">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="8c820-115">ModuleID</span><span class="sxs-lookup"><span data-stu-id="8c820-115">ModuleID</span></span> | [<span data-ttu-id="8c820-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="8c820-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="8c820-117">S</span><span class="sxs-lookup"><span data-stu-id="8c820-117">Y</span></span>   | <span data-ttu-id="8c820-118">N</span><span class="sxs-lookup"><span data-stu-id="8c820-118">N</span></span>        |
| <span data-ttu-id="8c820-119">Idioma</span><span class="sxs-lookup"><span data-stu-id="8c820-119">Language</span></span> | [<span data-ttu-id="8c820-120">Inteiro</span><span class="sxs-lookup"><span data-stu-id="8c820-120">Integer</span></span>](integer.md)       | <span data-ttu-id="8c820-121">S</span><span class="sxs-lookup"><span data-stu-id="8c820-121">Y</span></span>   | <span data-ttu-id="8c820-122">N</span><span class="sxs-lookup"><span data-stu-id="8c820-122">N</span></span>        |
| <span data-ttu-id="8c820-123">Versão</span><span class="sxs-lookup"><span data-stu-id="8c820-123">Version</span></span>  | [<span data-ttu-id="8c820-124">Versão</span><span class="sxs-lookup"><span data-stu-id="8c820-124">Version</span></span>](version.md)       |     | <span data-ttu-id="8c820-125">N</span><span class="sxs-lookup"><span data-stu-id="8c820-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8c820-126">Colunas</span><span class="sxs-lookup"><span data-stu-id="8c820-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8c820-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="8c820-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="8c820-128">Um identificador que identifica exclusivamente o módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8c820-128">An identifier that uniquely identifies the merge module.</span></span> <span data-ttu-id="8c820-129">Dois módulos de mesclagem não podem ter a mesma ModuleID, a menos que o módulo de mesclagem seja totalmente compatível com o seu antecessor.</span><span class="sxs-lookup"><span data-stu-id="8c820-129">Two merge modules cannot have the same ModuleID unless the merge module is entirely backward compatible with its predecessor.</span></span> <span data-ttu-id="8c820-130">Você pode criar um GUID para esse campo usando um utilitário como o GUIDGEN.</span><span class="sxs-lookup"><span data-stu-id="8c820-130">You can create a GUID for this field using a utility such as GUIDGEN.</span></span> <span data-ttu-id="8c820-131">A coluna ModuleID é uma chave primária para a tabela e, portanto, deve seguir a Convenção de nomenclatura na [nomenclatura de chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="8c820-131">The ModuleID column is a primary key for the table and therefore it must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="8c820-132">Por exemplo, se o nome legível do módulo de mesclagem for MyLibrary e o GUID for {880DE2F0-CDD8-11D1-A849-006097ABDE17}, a entrada na coluna ModuleID se tornará MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.</span><span class="sxs-lookup"><span data-stu-id="8c820-132">For example, if the readable name of the merge module is MyLibrary and the GUID is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

</dd> <dt>

<span data-ttu-id="8c820-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Idioma</span><span class="sxs-lookup"><span data-stu-id="8c820-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="8c820-134">O identificador de idioma especifica o idioma padrão para o módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8c820-134">The Language identifier specifies the default language for the merge module.</span></span> <span data-ttu-id="8c820-135">O identificador de idioma está em formato decimal, por exemplo, o inglês dos EUA é 1033.</span><span class="sxs-lookup"><span data-stu-id="8c820-135">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="8c820-136">O idioma usado pelo módulo de mesclagem pode ser alterado com a aplicação de uma transformação ao módulo de mesclagem antes da mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8c820-136">The language used by the merge module can be changed by applying a transform to the merge module before merging.</span></span>

</dd> <dt>

<span data-ttu-id="8c820-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versão</span><span class="sxs-lookup"><span data-stu-id="8c820-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="8c820-138">O campo versão contém uma cadeia de caracteres que descreve as versões principal e secundária do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8c820-138">The Version field contains a string that describes the major and minor versions of the merge module.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="8c820-139">Validação</span><span class="sxs-lookup"><span data-stu-id="8c820-139">Validation</span></span>

<dl>

[<span data-ttu-id="8c820-140">ICE03</span><span class="sxs-lookup"><span data-stu-id="8c820-140">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8c820-141">ICE06</span><span class="sxs-lookup"><span data-stu-id="8c820-141">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8c820-142">ICE25</span><span class="sxs-lookup"><span data-stu-id="8c820-142">ICE25</span></span>](ice25.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="8c820-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c820-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c820-144">Vários módulos de mesclagem de idioma</span><span class="sxs-lookup"><span data-stu-id="8c820-144">Multiple Language Merge Modules</span></span>](multiple-language-merge-modules.md)
</dt> </dl>

 

 



