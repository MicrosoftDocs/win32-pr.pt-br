---
description: A tabela Replicafile contém uma lista de arquivos que devem ser duplicados, seja para um diretório diferente do arquivo original ou para o mesmo diretório, mas com um nome diferente. O arquivo original deve ser um arquivo instalado pela ação InstallFiles.
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: Tabela replicafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011153"
---
# <a name="duplicatefile-table"></a><span data-ttu-id="73f72-104">Tabela replicafile</span><span class="sxs-lookup"><span data-stu-id="73f72-104">DuplicateFile Table</span></span>

<span data-ttu-id="73f72-105">A tabela Replicafile contém uma lista de arquivos que devem ser duplicados, seja para um diretório diferente do arquivo original ou para o mesmo diretório, mas com um nome diferente.</span><span class="sxs-lookup"><span data-stu-id="73f72-105">The DuplicateFile table contains a list of files that are to be duplicated, either to a different directory than the original file or to the same directory but with a different name.</span></span> <span data-ttu-id="73f72-106">O arquivo original deve ser um arquivo instalado pela [ação InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="73f72-106">The original file must be a file installed by the [InstallFiles action](installfiles-action.md).</span></span>

<span data-ttu-id="73f72-107">A tabela Replicafile tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="73f72-107">The DuplicateFile table has the following columns.</span></span>



| <span data-ttu-id="73f72-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="73f72-108">Column</span></span>      | <span data-ttu-id="73f72-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="73f72-109">Type</span></span>                         | <span data-ttu-id="73f72-110">Chave</span><span class="sxs-lookup"><span data-stu-id="73f72-110">Key</span></span> | <span data-ttu-id="73f72-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="73f72-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="73f72-112">FileKey</span><span class="sxs-lookup"><span data-stu-id="73f72-112">FileKey</span></span>     | [<span data-ttu-id="73f72-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="73f72-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="73f72-114">S</span><span class="sxs-lookup"><span data-stu-id="73f72-114">Y</span></span>   | <span data-ttu-id="73f72-115">N</span><span class="sxs-lookup"><span data-stu-id="73f72-115">N</span></span>        |
| <span data-ttu-id="73f72-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="73f72-116">Component\_</span></span> | [<span data-ttu-id="73f72-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="73f72-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="73f72-118">N</span><span class="sxs-lookup"><span data-stu-id="73f72-118">N</span></span>   | <span data-ttu-id="73f72-119">N</span><span class="sxs-lookup"><span data-stu-id="73f72-119">N</span></span>        |
| <span data-ttu-id="73f72-120">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="73f72-120">File\_</span></span>      | [<span data-ttu-id="73f72-121">Identificador</span><span class="sxs-lookup"><span data-stu-id="73f72-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="73f72-122">N</span><span class="sxs-lookup"><span data-stu-id="73f72-122">N</span></span>   | <span data-ttu-id="73f72-123">N</span><span class="sxs-lookup"><span data-stu-id="73f72-123">N</span></span>        |
| <span data-ttu-id="73f72-124">Destname</span><span class="sxs-lookup"><span data-stu-id="73f72-124">DestName</span></span>    | [<span data-ttu-id="73f72-125">Filename</span><span class="sxs-lookup"><span data-stu-id="73f72-125">Filename</span></span>](filename.md)     | <span data-ttu-id="73f72-126">N</span><span class="sxs-lookup"><span data-stu-id="73f72-126">N</span></span>   | <span data-ttu-id="73f72-127">S</span><span class="sxs-lookup"><span data-stu-id="73f72-127">Y</span></span>        |
| <span data-ttu-id="73f72-128">DestFolder</span><span class="sxs-lookup"><span data-stu-id="73f72-128">DestFolder</span></span>  | [<span data-ttu-id="73f72-129">Identificador</span><span class="sxs-lookup"><span data-stu-id="73f72-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="73f72-130">N</span><span class="sxs-lookup"><span data-stu-id="73f72-130">N</span></span>   | <span data-ttu-id="73f72-131">S</span><span class="sxs-lookup"><span data-stu-id="73f72-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="73f72-132">Colunas</span><span class="sxs-lookup"><span data-stu-id="73f72-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="73f72-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="73f72-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="73f72-134">Uma chave primária, um token não localizado, identificando um registro de Duplicatafiles exclusivo.</span><span class="sxs-lookup"><span data-stu-id="73f72-134">A primary key, a non-localized token, identifying a unique DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="73f72-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="73f72-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="73f72-136">Uma chave externa para a primeira coluna da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="73f72-136">An external key to the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="73f72-137">Se o componente identificado pela chave não estiver selecionado para instalação ou remoção, nenhuma ação será executada nesse registro duplicado.</span><span class="sxs-lookup"><span data-stu-id="73f72-137">If the component identified by the key is not selected for installation or removal, then no action is taken on this DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="73f72-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_</span><span class="sxs-lookup"><span data-stu-id="73f72-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="73f72-139">Chave estrangeira na [tabela de arquivos](file-table.md) que representa o arquivo original a ser duplicado.</span><span class="sxs-lookup"><span data-stu-id="73f72-139">Foreign key into the [File table](file-table.md) representing the original file that is to be duplicated.</span></span>

</dd> <dt>

<span data-ttu-id="73f72-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>Destname</span><span class="sxs-lookup"><span data-stu-id="73f72-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="73f72-141">Nome localizável a ser dado ao arquivo duplicado.</span><span class="sxs-lookup"><span data-stu-id="73f72-141">Localizable name to be given to the duplicate file.</span></span> <span data-ttu-id="73f72-142">Se esse campo estiver em branco, o arquivo de destino receberá o mesmo nome do arquivo original.</span><span class="sxs-lookup"><span data-stu-id="73f72-142">If this field is blank, then the destination file is given the same name as the original file.</span></span>

</dd> <dt>

<span data-ttu-id="73f72-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="73f72-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="73f72-144">Nome de uma propriedade que é o caminho completo para onde o arquivo duplicado deve ser copiado.</span><span class="sxs-lookup"><span data-stu-id="73f72-144">Name of a property that is the full path to where the duplicate file is to be copied.</span></span> <span data-ttu-id="73f72-145">Se esse diretório for o mesmo que o diretório que contém o arquivo original e o nome do arquivo duplicado proposto for o mesmo que o original, nenhuma ação ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="73f72-145">If this directory is the same as the directory containing the original file and the name for the proposed duplicate file is the same as the original, then no action takes place.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73f72-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="73f72-146">Remarks</span></span>

<span data-ttu-id="73f72-147">A tabela é processada pela [ação DuplicateFiles](duplicatefiles-action.md) e a [ação RemoveDuplicateFiles](removeduplicatefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="73f72-147">The table is processed by the [DuplicateFiles action](duplicatefiles-action.md) and the [RemoveDuplicateFiles action](removeduplicatefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="73f72-148">Validação</span><span class="sxs-lookup"><span data-stu-id="73f72-148">Validation</span></span>

<dl>

[<span data-ttu-id="73f72-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="73f72-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="73f72-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="73f72-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="73f72-151">ICE18</span><span class="sxs-lookup"><span data-stu-id="73f72-151">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="73f72-152">ICE32</span><span class="sxs-lookup"><span data-stu-id="73f72-152">ICE32</span></span>](ice32.md)  
</dl>

 

 



