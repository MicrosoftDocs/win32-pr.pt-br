---
description: Esta tabela contém uma lista de arquivos a serem movidos ou copiados de um diretório de origem especificado para um diretório de destino especificado.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: Tabela MoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2340626e745627c3c6146998c851a076d21ab81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663377"
---
# <a name="movefile-table"></a><span data-ttu-id="ca6ed-103">Tabela MoveFile</span><span class="sxs-lookup"><span data-stu-id="ca6ed-103">MoveFile Table</span></span>

<span data-ttu-id="ca6ed-104">Esta tabela contém uma lista de arquivos a serem movidos ou copiados de um diretório de origem especificado para um diretório de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-104">This table contains a list of files to be moved or copied from a specified source directory to a specified destination directory.</span></span>

<span data-ttu-id="ca6ed-105">A tabela MoveFile tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-105">The MoveFile table has the following columns.</span></span>



| <span data-ttu-id="ca6ed-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="ca6ed-106">Column</span></span>       | <span data-ttu-id="ca6ed-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca6ed-107">Type</span></span>                         | <span data-ttu-id="ca6ed-108">Chave</span><span class="sxs-lookup"><span data-stu-id="ca6ed-108">Key</span></span> | <span data-ttu-id="ca6ed-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="ca6ed-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="ca6ed-110">FileKey</span><span class="sxs-lookup"><span data-stu-id="ca6ed-110">FileKey</span></span>      | [<span data-ttu-id="ca6ed-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="ca6ed-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="ca6ed-112">S</span><span class="sxs-lookup"><span data-stu-id="ca6ed-112">Y</span></span>   | <span data-ttu-id="ca6ed-113">N</span><span class="sxs-lookup"><span data-stu-id="ca6ed-113">N</span></span>        |
| <span data-ttu-id="ca6ed-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="ca6ed-114">Component\_</span></span>  | [<span data-ttu-id="ca6ed-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="ca6ed-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="ca6ed-116">N</span><span class="sxs-lookup"><span data-stu-id="ca6ed-116">N</span></span>   | <span data-ttu-id="ca6ed-117">N</span><span class="sxs-lookup"><span data-stu-id="ca6ed-117">N</span></span>        |
| <span data-ttu-id="ca6ed-118">SourceName</span><span class="sxs-lookup"><span data-stu-id="ca6ed-118">SourceName</span></span>   | [<span data-ttu-id="ca6ed-119">Text</span><span class="sxs-lookup"><span data-stu-id="ca6ed-119">Text</span></span>](text.md)             | <span data-ttu-id="ca6ed-120">N</span><span class="sxs-lookup"><span data-stu-id="ca6ed-120">N</span></span>   | <span data-ttu-id="ca6ed-121">S</span><span class="sxs-lookup"><span data-stu-id="ca6ed-121">Y</span></span>        |
| <span data-ttu-id="ca6ed-122">Destname</span><span class="sxs-lookup"><span data-stu-id="ca6ed-122">DestName</span></span>     | [<span data-ttu-id="ca6ed-123">Filename</span><span class="sxs-lookup"><span data-stu-id="ca6ed-123">Filename</span></span>](filename.md)     | <span data-ttu-id="ca6ed-124">N</span><span class="sxs-lookup"><span data-stu-id="ca6ed-124">N</span></span>   | <span data-ttu-id="ca6ed-125">S</span><span class="sxs-lookup"><span data-stu-id="ca6ed-125">Y</span></span>        |
| <span data-ttu-id="ca6ed-126">SourceFolder</span><span class="sxs-lookup"><span data-stu-id="ca6ed-126">SourceFolder</span></span> | [<span data-ttu-id="ca6ed-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="ca6ed-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="ca6ed-128">N</span><span class="sxs-lookup"><span data-stu-id="ca6ed-128">N</span></span>   | <span data-ttu-id="ca6ed-129">S</span><span class="sxs-lookup"><span data-stu-id="ca6ed-129">Y</span></span>        |
| <span data-ttu-id="ca6ed-130">DestFolder</span><span class="sxs-lookup"><span data-stu-id="ca6ed-130">DestFolder</span></span>   | [<span data-ttu-id="ca6ed-131">Identificador</span><span class="sxs-lookup"><span data-stu-id="ca6ed-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="ca6ed-132">N</span><span class="sxs-lookup"><span data-stu-id="ca6ed-132">N</span></span>   | <span data-ttu-id="ca6ed-133">N</span><span class="sxs-lookup"><span data-stu-id="ca6ed-133">N</span></span>        |
| <span data-ttu-id="ca6ed-134">Opções</span><span class="sxs-lookup"><span data-stu-id="ca6ed-134">Options</span></span>      | [<span data-ttu-id="ca6ed-135">Inteiro</span><span class="sxs-lookup"><span data-stu-id="ca6ed-135">Integer</span></span>](integer.md)       | <span data-ttu-id="ca6ed-136">N</span><span class="sxs-lookup"><span data-stu-id="ca6ed-136">N</span></span>   | <span data-ttu-id="ca6ed-137">N</span><span class="sxs-lookup"><span data-stu-id="ca6ed-137">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ca6ed-138">Colunas</span><span class="sxs-lookup"><span data-stu-id="ca6ed-138">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ca6ed-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="ca6ed-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="ca6ed-140">Chave primária que identifica exclusivamente um registro MoveFile específico.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-140">Primary key that uniquely identifies a particular MoveFile record.</span></span>

</dd> <dt>

<span data-ttu-id="ca6ed-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="ca6ed-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="ca6ed-142">Chave externa na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ca6ed-142">External key into the [Component table](component-table.md).</span></span> <span data-ttu-id="ca6ed-143">Se o componente referenciado por essa chave não estiver selecionado para instalação ou remoção, nenhuma ação será executada nessa entrada MoveFile.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-143">If the component referenced by this key is not selected for installation or removal, then no action is taken on this MoveFile entry.</span></span>

</dd> <dt>

<span data-ttu-id="ca6ed-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span><span class="sxs-lookup"><span data-stu-id="ca6ed-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span></span>
</dt> <dd>

<span data-ttu-id="ca6ed-145">Esta coluna contém o nome localizável dos arquivos de origem a serem movidos ou copiados.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-145">This column contains the localizable name of the source files to be moved or copied.</span></span> <span data-ttu-id="ca6ed-146">Esta coluna pode ser deixada em branco.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-146">This column may be left blank.</span></span> <span data-ttu-id="ca6ed-147">Consulte a descrição da coluna SourceFolder.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-147">See the description of the SourceFolder column.</span></span> <span data-ttu-id="ca6ed-148">Este campo deve conter um nome de arquivo longo e pode conter caracteres curinga ( \* e?).</span><span class="sxs-lookup"><span data-stu-id="ca6ed-148">This field must contain a long file name and may contain wildcard characters (\* and ?).</span></span>

</dd> <dt>

<span data-ttu-id="ca6ed-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>Destname</span><span class="sxs-lookup"><span data-stu-id="ca6ed-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="ca6ed-150">Esta coluna contém o nome localizável a ser dado ao arquivo original após ser movido ou copiado.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-150">This column contains the localizable name to be given to the original file after it is moved or copied.</span></span> <span data-ttu-id="ca6ed-151">Se esse campo estiver em branco, o arquivo de destino receberá o mesmo nome que o arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-151">If this field is blank, then the destination file is given the same name as the source file.</span></span>

</dd> <dt>

<span data-ttu-id="ca6ed-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span><span class="sxs-lookup"><span data-stu-id="ca6ed-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span></span>
</dt> <dd>

<span data-ttu-id="ca6ed-153">Esta coluna contém o nome de uma propriedade que tem um valor que resolve para o caminho completo para o diretório de origem.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-153">This column contains the name of a property having a value that resolves to the full path to the source directory.</span></span> <span data-ttu-id="ca6ed-154">Se a coluna SourceName for deixada em branco, a propriedade chamada na coluna SourceFolder será considerada para conter o caminho completo para o próprio arquivo de origem (incluindo o nome do arquivo).</span><span class="sxs-lookup"><span data-stu-id="ca6ed-154">If the SourceName column is left blank, then the property named in the SourceFolder column is assumed to contain the full path to the source file itself (including the file name).</span></span>

</dd> <dt>

<span data-ttu-id="ca6ed-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="ca6ed-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="ca6ed-156">O nome de uma propriedade cujo valor é resolvido para o caminho completo do diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-156">The name of a property whose value resolves to the full path to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="ca6ed-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opções</span><span class="sxs-lookup"><span data-stu-id="ca6ed-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="ca6ed-158">Valor inteiro que especifica o modo de operação.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-158">Integer value specifying the operating mode.</span></span>



| <span data-ttu-id="ca6ed-159">Constante</span><span class="sxs-lookup"><span data-stu-id="ca6ed-159">Constant</span></span>                     | <span data-ttu-id="ca6ed-160">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="ca6ed-160">Hexadecimal</span></span> | <span data-ttu-id="ca6ed-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="ca6ed-161">Decimal</span></span> | <span data-ttu-id="ca6ed-162">Significado</span><span class="sxs-lookup"><span data-stu-id="ca6ed-162">Meaning</span></span>               |
|------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="ca6ed-163">(nenhum)</span><span class="sxs-lookup"><span data-stu-id="ca6ed-163">(none)</span></span>                       | <span data-ttu-id="ca6ed-164">0x000</span><span class="sxs-lookup"><span data-stu-id="ca6ed-164">0x000</span></span>       | <span data-ttu-id="ca6ed-165">0</span><span class="sxs-lookup"><span data-stu-id="ca6ed-165">0</span></span>       | <span data-ttu-id="ca6ed-166">Copie o arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-166">Copy the source file.</span></span> |
| <span data-ttu-id="ca6ed-167">**msidbMoveFileOptionsMove**</span><span class="sxs-lookup"><span data-stu-id="ca6ed-167">**msidbMoveFileOptionsMove**</span></span> | <span data-ttu-id="ca6ed-168">0x001</span><span class="sxs-lookup"><span data-stu-id="ca6ed-168">0x001</span></span>       | <span data-ttu-id="ca6ed-169">1</span><span class="sxs-lookup"><span data-stu-id="ca6ed-169">1</span></span>       | <span data-ttu-id="ca6ed-170">Mova o arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-170">Move the source file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca6ed-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca6ed-171">Remarks</span></span>

<span data-ttu-id="ca6ed-172">Se um \* caractere curinga "" for inserido na coluna SourceName da tabela MoveFile e um nome de arquivo de destino for especificado na coluna destname, todos os arquivos movidos ou copiados manterão os nomes nas fontes.</span><span class="sxs-lookup"><span data-stu-id="ca6ed-172">If a "\*" wildcard is entered in the SourceName column of the MoveFile table and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="ca6ed-173">Essa tabela é processada pela [ação MoveFiles](movefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="ca6ed-173">This table is processed by the [MoveFiles action](movefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="ca6ed-174">Validação</span><span class="sxs-lookup"><span data-stu-id="ca6ed-174">Validation</span></span>

<dl>

[<span data-ttu-id="ca6ed-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="ca6ed-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ca6ed-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="ca6ed-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ca6ed-177">ICE18</span><span class="sxs-lookup"><span data-stu-id="ca6ed-177">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="ca6ed-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="ca6ed-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ca6ed-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="ca6ed-179">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="ca6ed-180">ICE85</span><span class="sxs-lookup"><span data-stu-id="ca6ed-180">ICE85</span></span>](ice85.md)  
</dl>

 

 



