---
description: A tabela SFPCatalog contém os catálogos usados pelo Windows me.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Tabela SFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164735"
---
# <a name="sfpcatalog-table"></a><span data-ttu-id="d4ed8-103">Tabela SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="d4ed8-103">SFPCatalog Table</span></span>

<span data-ttu-id="d4ed8-104">A tabela SFPCatalog contém os catálogos usados pelo Windows me.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-104">The SFPCatalog table contains the catalogs used by Windows Me.</span></span>

<span data-ttu-id="d4ed8-105">A tabela SFPCatalog tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-105">The SFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="d4ed8-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="d4ed8-106">Column</span></span>     | <span data-ttu-id="d4ed8-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4ed8-107">Type</span></span>                       | <span data-ttu-id="d4ed8-108">Chave</span><span class="sxs-lookup"><span data-stu-id="d4ed8-108">Key</span></span> | <span data-ttu-id="d4ed8-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="d4ed8-109">Nullable</span></span> |
|------------|----------------------------|-----|----------|
| <span data-ttu-id="d4ed8-110">SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="d4ed8-110">SFPCatalog</span></span> | [<span data-ttu-id="d4ed8-111">Filename</span><span class="sxs-lookup"><span data-stu-id="d4ed8-111">Filename</span></span>](filename.md)   | <span data-ttu-id="d4ed8-112">S</span><span class="sxs-lookup"><span data-stu-id="d4ed8-112">Y</span></span>   | <span data-ttu-id="d4ed8-113">N</span><span class="sxs-lookup"><span data-stu-id="d4ed8-113">N</span></span>        |
| <span data-ttu-id="d4ed8-114">Catálogo</span><span class="sxs-lookup"><span data-stu-id="d4ed8-114">Catalog</span></span>    | [<span data-ttu-id="d4ed8-115">Binary</span><span class="sxs-lookup"><span data-stu-id="d4ed8-115">Binary</span></span>](binary.md)       | <span data-ttu-id="d4ed8-116">N</span><span class="sxs-lookup"><span data-stu-id="d4ed8-116">N</span></span>   | <span data-ttu-id="d4ed8-117">N</span><span class="sxs-lookup"><span data-stu-id="d4ed8-117">N</span></span>        |
| <span data-ttu-id="d4ed8-118">Dependência</span><span class="sxs-lookup"><span data-stu-id="d4ed8-118">Dependency</span></span> | [<span data-ttu-id="d4ed8-119">Binário</span><span class="sxs-lookup"><span data-stu-id="d4ed8-119">Formatted</span></span>](formatted.md) | <span data-ttu-id="d4ed8-120">N</span><span class="sxs-lookup"><span data-stu-id="d4ed8-120">N</span></span>   | <span data-ttu-id="d4ed8-121">S</span><span class="sxs-lookup"><span data-stu-id="d4ed8-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d4ed8-122">Colunas</span><span class="sxs-lookup"><span data-stu-id="d4ed8-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d4ed8-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="d4ed8-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span></span>
</dt> <dd>

<span data-ttu-id="d4ed8-124">O nome de arquivo curto para o catálogo.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-124">The short file name for the catalog.</span></span> <span data-ttu-id="d4ed8-125">Como os catálogos não têm nenhuma versão, o catálogo especificado nessa coluna pode substituir um catálogo que tem o mesmo nome e já está instalado no sistema local.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-125">Because catalogs have no version, the catalog specified in this column can overwrite a catalog that has the same name and is already installed on the local system.</span></span> <span data-ttu-id="d4ed8-126">Consulte o tópico controle de versão do arquivo [nenhum arquivo tem uma versão](neither-file-has-a-version.md).</span><span class="sxs-lookup"><span data-stu-id="d4ed8-126">See the file versioning topic [Neither File Has a Version](neither-file-has-a-version.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4ed8-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span><span class="sxs-lookup"><span data-stu-id="d4ed8-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span>
</dt> <dd>

<span data-ttu-id="d4ed8-128">Dados binários para o catálogo.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-128">Binary data for the catalog.</span></span>

</dd> <dt>

<span data-ttu-id="d4ed8-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Estados</span><span class="sxs-lookup"><span data-stu-id="d4ed8-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dependency</span></span>
</dt> <dd>

<span data-ttu-id="d4ed8-130">O catálogo especificado neste campo é o pai do catálogo dependente especificado no campo SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-130">The catalog specified in this field is the parent of the dependent catalog specified in the SFPCatalog field.</span></span> <span data-ttu-id="d4ed8-131">Insira o nome de arquivo curto do catálogo pai no campo de dependência.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-131">Enter the short file name of the parent catalog into the Dependency field.</span></span> <span data-ttu-id="d4ed8-132">Esse campo é uma chave de volta para a coluna SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-132">This field is a key back into the SFPCatalog column.</span></span> <span data-ttu-id="d4ed8-133">A correspondência de dependência diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-133">The dependency match is case sensitive.</span></span>

<span data-ttu-id="d4ed8-134">Se o campo de dependência fizer referência a outro registro nessa tabela SFPCatalog, o catálogo pai será instalado antes do catálogo dependente.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-134">If the Dependency field references another record in this SFPCatalog table, the parent catalog is installed before the dependent catalog.</span></span>

<span data-ttu-id="d4ed8-135">Se o campo de dependência fizer referência a um catálogo pai que não está presente no campo SFPCatalog desta tabela, e se o catálogo pai ainda não estiver instalado, a instalação falhará.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-135">If the Dependency field references a parent catalog that is not present in the SFPCatalog field of this table, and if the parent catalog is not already installed, the installation fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4ed8-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4ed8-136">Remarks</span></span>

<span data-ttu-id="d4ed8-137">A [ação InstallSFPCatalogFile](installsfpcatalogfile-action.md) consulta a [tabela de componentes](component-table.md), a [tabela de arquivos](file-table.md), a tabela [FileSFPCatalog](filesfpcatalog-table.md) e a tabela SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="d4ed8-137">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and SFPCatalog table.</span></span>

## <a name="validation"></a><span data-ttu-id="d4ed8-138">Validação</span><span class="sxs-lookup"><span data-stu-id="d4ed8-138">Validation</span></span>

<dl>

[<span data-ttu-id="d4ed8-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="d4ed8-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d4ed8-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="d4ed8-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d4ed8-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="d4ed8-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="d4ed8-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="d4ed8-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d4ed8-143">ICE46</span><span class="sxs-lookup"><span data-stu-id="d4ed8-143">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="d4ed8-144">ICE66</span><span class="sxs-lookup"><span data-stu-id="d4ed8-144">ICE66</span></span>](ice66.md)  
</dl>

 

 



