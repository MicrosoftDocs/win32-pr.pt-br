---
description: Quando uma tabela que contém apenas caracteres ASCII é exportada para um arquivo morto de texto, o arquivo. IDT segue o formato de arquivo morto básico.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: Dados ASCII em arquivos mortos de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828062"
---
# <a name="ascii-data-in-text-archive-files"></a><span data-ttu-id="9a03a-103">Dados ASCII em arquivos mortos de texto</span><span class="sxs-lookup"><span data-stu-id="9a03a-103">ASCII Data in Text Archive Files</span></span>

<span data-ttu-id="9a03a-104">Quando uma tabela que contém apenas caracteres ASCII é exportada para um [arquivo morto de texto](text-archive-files.md), o arquivo. IDT segue o [formato de arquivo morto](archive-file-format.md)básico.</span><span class="sxs-lookup"><span data-stu-id="9a03a-104">When a table that contains only ASCII characters is exported to a [text archive file](text-archive-files.md), the .idt file adheres to the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="9a03a-105">Se a tabela contiver informações não ASCII, o formato do arquivo morto será estendido para incluir informações de página de código.</span><span class="sxs-lookup"><span data-stu-id="9a03a-105">If the table contains non-ASCII information, the format of the archive file is extended to include code page information.</span></span>

## <a name="text-archive-files-that-contain-only-ascii-characters"></a><span data-ttu-id="9a03a-106">Arquivos mortos de texto que contêm apenas caracteres ASCII</span><span class="sxs-lookup"><span data-stu-id="9a03a-106">Text archive files that contain only ASCII characters</span></span>

<span data-ttu-id="9a03a-107">Quando uma tabela que contém apenas caracteres ASCII é exportada para um arquivo morto, o arquivo. IDT está no [formato básico de arquivo morto](archive-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="9a03a-107">When a table that contains only ASCII characters is exported to an archive file, the .idt file is in the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="9a03a-108">Cada fluxo na tabela é exportado como um arquivo com uma extensão de nome de arquivo. IBD.</span><span class="sxs-lookup"><span data-stu-id="9a03a-108">Each stream in the table is exported as a file with an .ibd file name extension.</span></span> <span data-ttu-id="9a03a-109">Os arquivos. IBD são armazenados em uma pasta com o mesmo nome que a tabela.</span><span class="sxs-lookup"><span data-stu-id="9a03a-109">The .ibd files are stored in a folder with the same name as the table.</span></span> <span data-ttu-id="9a03a-110">Por exemplo, considere a exportação da tabela [binária](binary-table.md) a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a03a-110">For example, consider the export of the following [Binary](binary-table.md) table.</span></span>



| <span data-ttu-id="9a03a-111">Nome</span><span class="sxs-lookup"><span data-stu-id="9a03a-111">Name</span></span>  | <span data-ttu-id="9a03a-112">Dados</span><span class="sxs-lookup"><span data-stu-id="9a03a-112">Data</span></span>      |
|-------|-----------|
| <span data-ttu-id="9a03a-113">Manuais</span><span class="sxs-lookup"><span data-stu-id="9a03a-113">Books</span></span> | <span data-ttu-id="9a03a-114">Books. IBD</span><span class="sxs-lookup"><span data-stu-id="9a03a-114">Books.ibd</span></span> |
| <span data-ttu-id="9a03a-115">Cars</span><span class="sxs-lookup"><span data-stu-id="9a03a-115">Cars</span></span>  | <span data-ttu-id="9a03a-116">Carros. IBD</span><span class="sxs-lookup"><span data-stu-id="9a03a-116">Cars.ibd</span></span>  |



 

<span data-ttu-id="9a03a-117">A estrutura de diretório depois de exportar essa tabela é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="9a03a-117">The directory structure after exporting this table is as follows.</span></span> <span data-ttu-id="9a03a-118">As informações na tabela de banco de dados são exportadas para Binary. IDT.</span><span class="sxs-lookup"><span data-stu-id="9a03a-118">The information in the database table is exported to Binary.idt.</span></span> <span data-ttu-id="9a03a-119">Os dois fluxos de dados binários são exportados para book. IBD e carros. IBD salvos na pasta denominada Binary.</span><span class="sxs-lookup"><span data-stu-id="9a03a-119">The two streams of binary data are exported to Book.ibd and Cars.ibd saved in the folder named Binary.</span></span>

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

<span data-ttu-id="9a03a-120">O arquivo morto Binary. IDT está no formato básico de [arquivo morto](archive-file-format.md) e teria a seguinte aparência.</span><span class="sxs-lookup"><span data-stu-id="9a03a-120">The Binary.idt archive file is in the basic [archive file format](archive-file-format.md) and would look as follows.</span></span>

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a><span data-ttu-id="9a03a-121">Arquivos mortos de texto que contêm caracteres não ASCII</span><span class="sxs-lookup"><span data-stu-id="9a03a-121">Text archive files that contain non- ASCII characters</span></span>

<span data-ttu-id="9a03a-122">Se o arquivo contiver dados não ASCII, o [formato de arquivo morto](archive-file-format.md) básico do arquivo. IDT será estendido para incluir informações de página de código.</span><span class="sxs-lookup"><span data-stu-id="9a03a-122">If the file contains non-ASCII data, the basic [archive file format](archive-file-format.md) of the .idt file is extended to include code page information.</span></span> <span data-ttu-id="9a03a-123">A terceira linha na tabela. IDT é a página de código numérica seguida pelo nome da tabela e nomes de coluna de chave primária separados por guias.</span><span class="sxs-lookup"><span data-stu-id="9a03a-123">The third row in the .idt table is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="9a03a-124">Um arquivo. IDT que contém informações não ASCII deve ser salvo no formato ASCII.</span><span class="sxs-lookup"><span data-stu-id="9a03a-124">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="9a03a-125">Por exemplo, um arquivo morto de texto pode conter os nomes de coluna e tabela codificados como UTF-8, mas o arquivo morto em si deve ser ASCII.</span><span class="sxs-lookup"><span data-stu-id="9a03a-125">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span>

 

<span data-ttu-id="9a03a-126">A seguinte tabela ActionText localizada em francês conterá informações não ASCII.</span><span class="sxs-lookup"><span data-stu-id="9a03a-126">The following ActionText table localized into French would contain non-ASCII information.</span></span> <span data-ttu-id="9a03a-127">A página de código numérico usada para cadeias de caracteres francesas é 1252.</span><span class="sxs-lookup"><span data-stu-id="9a03a-127">The numeric code page used for French strings is 1252.</span></span>



| <span data-ttu-id="9a03a-128">Ação</span><span class="sxs-lookup"><span data-stu-id="9a03a-128">Action</span></span>    | <span data-ttu-id="9a03a-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a03a-129">Description</span></span>                                  | <span data-ttu-id="9a03a-130">Modelo</span><span class="sxs-lookup"><span data-stu-id="9a03a-130">Template</span></span> |
|-----------|----------------------------------------------|----------|
| <span data-ttu-id="9a03a-131">ANUNCIAR</span><span class="sxs-lookup"><span data-stu-id="9a03a-131">ADVERTISE</span></span> | <span data-ttu-id="9a03a-132">Publicação d'informations sur l'application</span><span class="sxs-lookup"><span data-stu-id="9a03a-132">Publication d'informations sur l'application</span></span> |          |



 

<span data-ttu-id="9a03a-133">O arquivo morto exportado, ActionText. IDT, seria o seguinte.</span><span class="sxs-lookup"><span data-stu-id="9a03a-133">The exported archive file, ActionText.idt, would be as follows.</span></span>

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> <span data-ttu-id="9a03a-134">Se um arquivo morto de texto contiver dados não ASCII, o arquivo morto incluirá informações de página de código.</span><span class="sxs-lookup"><span data-stu-id="9a03a-134">If a text archive file contains non-ASCII data, the archive file includes code page information.</span></span> <span data-ttu-id="9a03a-135">Arquivos mortos com informações de página de código só podem ser importados de volta para um banco de dados dessa página de código exata ou para um banco de dados neutro de idioma.</span><span class="sxs-lookup"><span data-stu-id="9a03a-135">Archive files with code page information can only be imported back into a database of that exact code page or into a language neutral database.</span></span> <span data-ttu-id="9a03a-136">No caso de um banco de dados com neutralidade de idioma, a página de código é definida como a página de código do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="9a03a-136">In the case of a language neutral database, the code page is set to the code page of the archive file.</span></span> <span data-ttu-id="9a03a-137">Para obter mais informações sobre como Windows Installer manipula páginas de código, consulte a seção [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="9a03a-137">For more information about how Windows Installer handles code pages see the section [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

 

 

 



