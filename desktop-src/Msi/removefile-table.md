---
description: A tabela RemoveFile contém uma lista de arquivos a serem removidos pela ação removidas. A definição da coluna FileName desta tabela como NULL dá suporte à remoção de pastas vazias.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: Remover Tabelafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723e42582821d79842686678c5b310e95cd1e944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829187"
---
# <a name="removefile-table"></a><span data-ttu-id="c083d-104">Remover Tabelafile</span><span class="sxs-lookup"><span data-stu-id="c083d-104">RemoveFile Table</span></span>

<span data-ttu-id="c083d-105">A tabela RemoveFile contém uma lista de arquivos a serem removidos pela [ação](removefiles-action.md)removidas.</span><span class="sxs-lookup"><span data-stu-id="c083d-105">The RemoveFile table contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span> <span data-ttu-id="c083d-106">A definição da coluna FileName desta tabela como NULL dá suporte à remoção de pastas vazias.</span><span class="sxs-lookup"><span data-stu-id="c083d-106">Setting the FileName column of this table to Null supports the removal of empty folders.</span></span>

<span data-ttu-id="c083d-107">A tabela RemoveFile tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c083d-107">The RemoveFile table has the following columns.</span></span>



| <span data-ttu-id="c083d-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="c083d-108">Column</span></span>      | <span data-ttu-id="c083d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c083d-109">Type</span></span>                                     | <span data-ttu-id="c083d-110">Chave</span><span class="sxs-lookup"><span data-stu-id="c083d-110">Key</span></span> | <span data-ttu-id="c083d-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="c083d-111">Nullable</span></span> |
|-------------|------------------------------------------|-----|----------|
| <span data-ttu-id="c083d-112">FileKey</span><span class="sxs-lookup"><span data-stu-id="c083d-112">FileKey</span></span>     | [<span data-ttu-id="c083d-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="c083d-113">Identifier</span></span>](identifier.md)             | <span data-ttu-id="c083d-114">S</span><span class="sxs-lookup"><span data-stu-id="c083d-114">Y</span></span>   | <span data-ttu-id="c083d-115">N</span><span class="sxs-lookup"><span data-stu-id="c083d-115">N</span></span>        |
| <span data-ttu-id="c083d-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="c083d-116">Component\_</span></span> | [<span data-ttu-id="c083d-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="c083d-117">Identifier</span></span>](identifier.md)             | <span data-ttu-id="c083d-118">N</span><span class="sxs-lookup"><span data-stu-id="c083d-118">N</span></span>   | <span data-ttu-id="c083d-119">N</span><span class="sxs-lookup"><span data-stu-id="c083d-119">N</span></span>        |
| <span data-ttu-id="c083d-120">FileName</span><span class="sxs-lookup"><span data-stu-id="c083d-120">FileName</span></span>    | [<span data-ttu-id="c083d-121">WildCardFilename</span><span class="sxs-lookup"><span data-stu-id="c083d-121">WildCardFilename</span></span>](wildcardfilename.md) | <span data-ttu-id="c083d-122">N</span><span class="sxs-lookup"><span data-stu-id="c083d-122">N</span></span>   | <span data-ttu-id="c083d-123">S</span><span class="sxs-lookup"><span data-stu-id="c083d-123">Y</span></span>        |
| <span data-ttu-id="c083d-124">DirProperty</span><span class="sxs-lookup"><span data-stu-id="c083d-124">DirProperty</span></span> | [<span data-ttu-id="c083d-125">Identificador</span><span class="sxs-lookup"><span data-stu-id="c083d-125">Identifier</span></span>](identifier.md)             | <span data-ttu-id="c083d-126">N</span><span class="sxs-lookup"><span data-stu-id="c083d-126">N</span></span>   | <span data-ttu-id="c083d-127">N</span><span class="sxs-lookup"><span data-stu-id="c083d-127">N</span></span>        |
| <span data-ttu-id="c083d-128">InstallMode</span><span class="sxs-lookup"><span data-stu-id="c083d-128">InstallMode</span></span> | [<span data-ttu-id="c083d-129">Inteiro</span><span class="sxs-lookup"><span data-stu-id="c083d-129">Integer</span></span>](integer.md)                   | <span data-ttu-id="c083d-130">N</span><span class="sxs-lookup"><span data-stu-id="c083d-130">N</span></span>   | <span data-ttu-id="c083d-131">N</span><span class="sxs-lookup"><span data-stu-id="c083d-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c083d-132">Colunas</span><span class="sxs-lookup"><span data-stu-id="c083d-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c083d-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="c083d-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="c083d-134">Chave primária usada para identificar essa entrada de tabela específica.</span><span class="sxs-lookup"><span data-stu-id="c083d-134">Primary key used to identify this particular table entry.</span></span>

</dd> <dt>

<span data-ttu-id="c083d-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="c083d-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="c083d-136">Chave externa a primeira coluna da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c083d-136">External key the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="c083d-137">Este campo faz referência ao componente que controla o arquivo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="c083d-137">This field references the component that controls the file to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="c083d-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="c083d-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="c083d-139">Esta coluna contém o nome localizável do arquivo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="c083d-139">This column contains the localizable name of the file to be removed.</span></span> <span data-ttu-id="c083d-140">Se essa coluna for nula, a pasta especificada será removida se estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="c083d-140">If this column is null, then the specified folder will be removed if it is empty.</span></span> <span data-ttu-id="c083d-141">Todos os arquivos que correspondem ao curinga serão removidos do diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="c083d-141">All of the files that match the wildcard will be removed from the specified directory.</span></span>

</dd> <dt>

<span data-ttu-id="c083d-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="c083d-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="c083d-143">Nome de uma propriedade cujo valor é considerado para ser resolvido para o caminho completo da pasta do arquivo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="c083d-143">Name of a property whose value is assumed to resolve to the full path to the folder of the file to be removed.</span></span> <span data-ttu-id="c083d-144">A propriedade pode ser o nome de um diretório na [tabela de diretórios](directory-table.md), uma propriedade definida pela [tabela AppSearch](appsearch-table.md)ou qualquer outra propriedade que represente um caminho completo.</span><span class="sxs-lookup"><span data-stu-id="c083d-144">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="c083d-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span><span class="sxs-lookup"><span data-stu-id="c083d-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span></span>
</dt> <dd>

<span data-ttu-id="c083d-146">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c083d-146">Must be one of the following values.</span></span>



| <span data-ttu-id="c083d-147">Constante</span><span class="sxs-lookup"><span data-stu-id="c083d-147">Constant</span></span>                                | <span data-ttu-id="c083d-148">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="c083d-148">Hexadecimal</span></span> | <span data-ttu-id="c083d-149">Decimal</span><span class="sxs-lookup"><span data-stu-id="c083d-149">Decimal</span></span> | <span data-ttu-id="c083d-150">Description</span><span class="sxs-lookup"><span data-stu-id="c083d-150">Description</span></span>                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c083d-151">**msidbRemoveFileInstallModeOnInstall**</span><span class="sxs-lookup"><span data-stu-id="c083d-151">**msidbRemoveFileInstallModeOnInstall**</span></span> | <span data-ttu-id="c083d-152">0x001</span><span class="sxs-lookup"><span data-stu-id="c083d-152">0x001</span></span>       | <span data-ttu-id="c083d-153">1</span><span class="sxs-lookup"><span data-stu-id="c083d-153">1</span></span>       | <span data-ttu-id="c083d-154">Remover somente quando o componente associado estiver sendo instalado (msiInstallStateLocal ou msiInstallStateSource).</span><span class="sxs-lookup"><span data-stu-id="c083d-154">Remove only when the associated component is being installed (msiInstallStateLocal or msiInstallStateSource).</span></span> |
| <span data-ttu-id="c083d-155">**msidbRemoveFileInstallModeOnRemove**</span><span class="sxs-lookup"><span data-stu-id="c083d-155">**msidbRemoveFileInstallModeOnRemove**</span></span>  | <span data-ttu-id="c083d-156">0x002</span><span class="sxs-lookup"><span data-stu-id="c083d-156">0x002</span></span>       | <span data-ttu-id="c083d-157">2</span><span class="sxs-lookup"><span data-stu-id="c083d-157">2</span></span>       | <span data-ttu-id="c083d-158">Remover somente quando o componente associado estiver sendo removido (msiInstallStateAbsent).</span><span class="sxs-lookup"><span data-stu-id="c083d-158">Remove only when the associated component is being removed (msiInstallStateAbsent).</span></span>                           |
| <span data-ttu-id="c083d-159">**msidbRemoveFileInstallModeOnBoth**</span><span class="sxs-lookup"><span data-stu-id="c083d-159">**msidbRemoveFileInstallModeOnBoth**</span></span>    | <span data-ttu-id="c083d-160">0x003</span><span class="sxs-lookup"><span data-stu-id="c083d-160">0x003</span></span>       | <span data-ttu-id="c083d-161">3</span><span class="sxs-lookup"><span data-stu-id="c083d-161">3</span></span>       | <span data-ttu-id="c083d-162">Remova um dos casos acima.</span><span class="sxs-lookup"><span data-stu-id="c083d-162">Remove in either of the above cases.</span></span>                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c083d-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="c083d-163">Remarks</span></span>

<span data-ttu-id="c083d-164">As referências de arquivo nesta tabela são processadas pela [ação RemoveFiles](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="c083d-164">The file references in this table are processed by the [RemoveFiles action](removefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="c083d-165">Validação</span><span class="sxs-lookup"><span data-stu-id="c083d-165">Validation</span></span>

<dl>

[<span data-ttu-id="c083d-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="c083d-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c083d-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="c083d-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c083d-168">ICE18</span><span class="sxs-lookup"><span data-stu-id="c083d-168">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="c083d-169">ICE32</span><span class="sxs-lookup"><span data-stu-id="c083d-169">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c083d-170">ICE45</span><span class="sxs-lookup"><span data-stu-id="c083d-170">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="c083d-171">ICE64</span><span class="sxs-lookup"><span data-stu-id="c083d-171">ICE64</span></span>](ice64.md)  
</dl>

 

 



