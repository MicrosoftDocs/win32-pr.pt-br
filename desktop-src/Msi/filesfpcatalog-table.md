---
description: A tabela FileSFPCatalog associa os arquivos especificados aos arquivos de catálogo usados pela proteção de arquivo do sistema.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Tabela FileSFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770377"
---
# <a name="filesfpcatalog-table"></a><span data-ttu-id="b6e1e-103">Tabela FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="b6e1e-103">FileSFPCatalog Table</span></span>

<span data-ttu-id="b6e1e-104">A tabela FileSFPCatalog associa os arquivos especificados aos arquivos de catálogo usados pela proteção de arquivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="b6e1e-104">The FileSFPCatalog table associates specified files with the catalog files used by system file protection.</span></span>

<span data-ttu-id="b6e1e-105">**Windows Vista, Windows Server 2003 e Windows XP:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="b6e1e-105">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

<span data-ttu-id="b6e1e-106">A tabela FileSFPCatalog tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6e1e-106">The FileSFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="b6e1e-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="b6e1e-107">Column</span></span>       | <span data-ttu-id="b6e1e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6e1e-108">Type</span></span>                         | <span data-ttu-id="b6e1e-109">Chave</span><span class="sxs-lookup"><span data-stu-id="b6e1e-109">Key</span></span> | <span data-ttu-id="b6e1e-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="b6e1e-110">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="b6e1e-111">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="b6e1e-111">File\_</span></span>       | [<span data-ttu-id="b6e1e-112">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6e1e-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="b6e1e-113">S</span><span class="sxs-lookup"><span data-stu-id="b6e1e-113">Y</span></span>   | <span data-ttu-id="b6e1e-114">N</span><span class="sxs-lookup"><span data-stu-id="b6e1e-114">N</span></span>        |
| <span data-ttu-id="b6e1e-115">SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="b6e1e-115">SFPCatalog\_</span></span> | [<span data-ttu-id="b6e1e-116">Filename</span><span class="sxs-lookup"><span data-stu-id="b6e1e-116">Filename</span></span>](filename.md)     | <span data-ttu-id="b6e1e-117">S</span><span class="sxs-lookup"><span data-stu-id="b6e1e-117">Y</span></span>   | <span data-ttu-id="b6e1e-118">N</span><span class="sxs-lookup"><span data-stu-id="b6e1e-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b6e1e-119">Colunas</span><span class="sxs-lookup"><span data-stu-id="b6e1e-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b6e1e-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_</span><span class="sxs-lookup"><span data-stu-id="b6e1e-120"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="b6e1e-121">Chave estrangeira para a [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="b6e1e-121">Foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6e1e-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="b6e1e-122"><span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_</span></span>
</dt> <dd>

<span data-ttu-id="b6e1e-123">Chave estrangeira para a [tabela SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="b6e1e-123">Foreign key to the [SFPCatalog table](sfpcatalog-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6e1e-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6e1e-124">Remarks</span></span>

<span data-ttu-id="b6e1e-125">A [ação InstallSFPCatalogFile](installsfpcatalogfile-action.md) consulta a [tabela de componentes](component-table.md), a [tabela de arquivos](file-table.md), a tabela FileSFPCatalog e a [tabela SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="b6e1e-125">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), FileSFPCatalog table and [SFPCatalog table](sfpcatalog-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="b6e1e-126">Validação</span><span class="sxs-lookup"><span data-stu-id="b6e1e-126">Validation</span></span>

<dl>

[<span data-ttu-id="b6e1e-127">ICE03</span><span class="sxs-lookup"><span data-stu-id="b6e1e-127">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b6e1e-128">ICE06</span><span class="sxs-lookup"><span data-stu-id="b6e1e-128">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b6e1e-129">ICE32</span><span class="sxs-lookup"><span data-stu-id="b6e1e-129">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b6e1e-130">ICE66</span><span class="sxs-lookup"><span data-stu-id="b6e1e-130">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="b6e1e-131">ICE76</span><span class="sxs-lookup"><span data-stu-id="b6e1e-131">ICE76</span></span>](ice76.md)  
</dl>

 

 



