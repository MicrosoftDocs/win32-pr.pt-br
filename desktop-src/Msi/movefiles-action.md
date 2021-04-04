---
description: A ação MoveFiles localiza arquivos existentes no computador do usuário e move ou copia esses arquivos para um novo local.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Ação MoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837312"
---
# <a name="movefiles-action"></a><span data-ttu-id="0fe93-103">Ação MoveFiles</span><span class="sxs-lookup"><span data-stu-id="0fe93-103">MoveFiles Action</span></span>

<span data-ttu-id="0fe93-104">A ação MoveFiles localiza arquivos existentes no computador do usuário e move ou copia esses arquivos para um novo local.</span><span class="sxs-lookup"><span data-stu-id="0fe93-104">The MoveFiles action locates existing files on the user's computer and moves or copies those files to a new location.</span></span> <span data-ttu-id="0fe93-105">A ação MoveFiles consulta a [tabela MoveFile](movefile-table.md) e move os arquivos especificados ali se o componente vinculado às entradas for especificado para ser instalado localmente ou estiver sendo executado a partir da origem.</span><span class="sxs-lookup"><span data-stu-id="0fe93-105">The MoveFiles action queries the [MoveFile table](movefile-table.md) and moves files specified there if the component linked to the entries is specified to be install locally or is being run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0fe93-106">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="0fe93-106">Sequence Restrictions</span></span>

<span data-ttu-id="0fe93-107">A ação Moves removes deve vir após a ação [InstallValidate](installvalidate-action.md) e antes da ação [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0fe93-107">The MoveFiles action must come after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0fe93-108">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="0fe93-108">ActionData Messages</span></span>



| <span data-ttu-id="0fe93-109">Campo</span><span class="sxs-lookup"><span data-stu-id="0fe93-109">Field</span></span> | <span data-ttu-id="0fe93-110">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="0fe93-110">Description of action data</span></span>                  |
|-------|---------------------------------------------|
| <span data-ttu-id="0fe93-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="0fe93-111">\[1\]</span></span> | <span data-ttu-id="0fe93-112">Identificador do arquivo movido.</span><span class="sxs-lookup"><span data-stu-id="0fe93-112">Identifier of moved file.</span></span>                   |
| <span data-ttu-id="0fe93-113">\[6\]</span><span class="sxs-lookup"><span data-stu-id="0fe93-113">\[6\]</span></span> | <span data-ttu-id="0fe93-114">Tamanho do arquivo instalado em bytes.</span><span class="sxs-lookup"><span data-stu-id="0fe93-114">Size of installed file in bytes.</span></span>            |
| <span data-ttu-id="0fe93-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="0fe93-115">\[9\]</span></span> | <span data-ttu-id="0fe93-116">Identificador do diretório que contém o arquivo movido.</span><span class="sxs-lookup"><span data-stu-id="0fe93-116">Identifier of directory holding moved file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0fe93-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fe93-117">Remarks</span></span>

<span data-ttu-id="0fe93-118">A tabela MoveFiles contém uma coluna chamada "Options", que especifica os arquivos de origem a serem movidos ou copiados.</span><span class="sxs-lookup"><span data-stu-id="0fe93-118">The MoveFiles table contain a column named "options" which specifies the source files to be moved or copied.</span></span> <span data-ttu-id="0fe93-119">Um arquivo de origem movido é excluído depois de ser copiado para um novo local.</span><span class="sxs-lookup"><span data-stu-id="0fe93-119">A moved source file is deleted after it has been copied to a new location.</span></span> <span data-ttu-id="0fe93-120">Para obter a sintaxe exata, consulte a [tabela MoveFile](movefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="0fe93-120">For the exact syntax, see the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="0fe93-121">As colunas SourceFolder e DestFolder da tabela MoveFile são nomes de propriedade cujos valores devem ser resolvidos para caminhos totalmente qualificados.</span><span class="sxs-lookup"><span data-stu-id="0fe93-121">The SourceFolder and DestFolder columns of the MoveFile table are property names whose values are expected to resolve to fully qualified paths.</span></span> <span data-ttu-id="0fe93-122">Essas propriedades podem ser qualquer uma das entradas de diretório na tabela de [diretório](directory-table.md) , qualquer propriedade de pasta predefinida ([**FavoritesFolder**](favoritesfolder.md), por exemplo) ou uma propriedade definida por qualquer entrada na tabela [AppSearch](appsearch-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0fe93-122">These properties can be any of the directory entries in the [Directory](directory-table.md) table, any predefined folder property ([**FavoritesFolder**](favoritesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="0fe93-123">Essas propriedades podem conter um caminho completo que contém o nome do arquivo para um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="0fe93-123">These properties may contain a full path containing the file name to a specific file.</span></span> <span data-ttu-id="0fe93-124">Por exemplo, a tabela AppSearch pode ser criada para pesquisar um arquivo específico e definir uma propriedade para o caminho completo para esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="0fe93-124">For example, the AppSearch table can be authored to search for a particular file and set a property to the full path to that file.</span></span> <span data-ttu-id="0fe93-125">Neste exemplo, a coluna SourceName na tabela MoveFile pode ser deixada em branco para indicar que o valor na propriedade SourceFolder contém um caminho de arquivo completo.</span><span class="sxs-lookup"><span data-stu-id="0fe93-125">In this example, the SourceName column in the MoveFile table can be left blank to indicate that the value in the SourceFolder property contains a full file path.</span></span> <span data-ttu-id="0fe93-126">O ponto-e-vírgula é o delimitador de lista para transformações, fontes e patches e não deve ser usado em nomes de arquivo ou caminhos.</span><span class="sxs-lookup"><span data-stu-id="0fe93-126">The semicolon is the list delimiter for transforms, sources, and patches and should not be used in file names or paths.</span></span>

<span data-ttu-id="0fe93-127">A ação MoveFiles não atua em entradas na tabela MoveFile em que a propriedade SourceFolder ou DestFolder não é avaliada como um caminho completo.</span><span class="sxs-lookup"><span data-stu-id="0fe93-127">The MoveFiles action does not act on entries in the MoveFile table in which either the SourceFolder or DestFolder property does not evaluate to a full path.</span></span>

<span data-ttu-id="0fe93-128">A ação MoveFiles tenta mover ou copiar todos os arquivos no diretório de origem que correspondem ao nome fornecido na coluna SourceName da tabela MoveFiles.</span><span class="sxs-lookup"><span data-stu-id="0fe93-128">The MoveFiles action attempts to move or copy all files in the source directory that match the name given in the SourceName column of the MoveFiles table.</span></span> <span data-ttu-id="0fe93-129">O nome na coluna SourceName pode incluir \* ou?</span><span class="sxs-lookup"><span data-stu-id="0fe93-129">The name in the SourceName column can include either the \* or ?</span></span> <span data-ttu-id="0fe93-130">curingas que permitem que um grupo de arquivos seja movido ou copiado.</span><span class="sxs-lookup"><span data-stu-id="0fe93-130">wildcards which allow a group of files to be moved or copied.</span></span> <span data-ttu-id="0fe93-131">Por exemplo, a coluna SourceName pode conter uma entrada de " \* . xls" e a ação MoveFiles move ou copia Todas as pastas de trabalho do Microsoft Excel do diretório de origem para o destino.</span><span class="sxs-lookup"><span data-stu-id="0fe93-131">For example, the SourceName column may contain an entry of "\*.xls" and the MoveFiles action moves or copies every Microsoft Excel workbook from the source directory to the destination.</span></span>

<span data-ttu-id="0fe93-132">O nome a ser fornecido para o arquivo de destino pode ser especificado na coluna Destname da tabela MoveFile.</span><span class="sxs-lookup"><span data-stu-id="0fe93-132">The name to be given to the destination file can be specified in the DestName column of the MoveFile table.</span></span> <span data-ttu-id="0fe93-133">O nome do arquivo de destino manterá o nome do arquivo de origem se essa coluna for deixada em branco.</span><span class="sxs-lookup"><span data-stu-id="0fe93-133">The destination file name retains the source file name if this column is left blank.</span></span>

<span data-ttu-id="0fe93-134">Se um \* caractere curinga "" for inserido na coluna SourceName da [tabela MoveFile](movefile-table.md) e um nome de arquivo de destino for especificado na coluna destname, todos os arquivos movidos ou copiados manterão os nomes nas fontes.</span><span class="sxs-lookup"><span data-stu-id="0fe93-134">If a "\*" wildcard is entered in the SourceName column of the [MoveFile table](movefile-table.md) and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="0fe93-135">Os arquivos movidos ou copiados pela ação MoveFiles não são excluídos quando o produto é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="0fe93-135">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

 

 



