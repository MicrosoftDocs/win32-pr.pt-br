---
description: Você pode adicionar informações de localização a um banco de dados de instalação importando e exportando arquivos mortos de texto ASCII usando MsiDatabaseExport e MsiDatabaseImport.
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: Manipulação de página de código de tabelas importadas e exportadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b090bead1fa35b451ed12e0e0da0143b98b8918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769326"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a><span data-ttu-id="b5cec-103">Manipulação de página de código de tabelas importadas e exportadas</span><span class="sxs-lookup"><span data-stu-id="b5cec-103">Code Page Handling of Imported and Exported Tables</span></span>

<span data-ttu-id="b5cec-104">Você pode adicionar informações de localização a um banco de dados de instalação importando e exportando arquivos mortos de texto ASCII usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) e [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="b5cec-104">You can add localization information to an installation database by importing and exporting ASCII text archive files using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) and [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="b5cec-105">Como o pool de cadeias de caracteres de banco de dados usa uma página de código ANSI, o banco de dados e os [arquivos mortos de texto](text-archive-files.md) exportados têm páginas</span><span class="sxs-lookup"><span data-stu-id="b5cec-105">Because the database string pool uses an ANSI code page, both the database and exported [Text Archive Files](text-archive-files.md) have code pages.</span></span>

<span data-ttu-id="b5cec-106">Quando um [arquivo morto de texto](text-archive-files.md) é exportado de um banco de dados, a página de código do arquivo morto é igual ao banco de dados pai.</span><span class="sxs-lookup"><span data-stu-id="b5cec-106">When a [Text Archive File](text-archive-files.md) is exported from a database, the code page of the archive file is the same as the parent database.</span></span> <span data-ttu-id="b5cec-107">Para obter uma lista de páginas de código numérico, consulte [localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b5cec-107">For a list of numeric code pages, see [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md).</span></span>

> [!Note]  
> <span data-ttu-id="b5cec-108">Exportar uma tabela para um arquivo morto de texto traduz os caracteres de controle para evitar conflitos com delimitadores de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b5cec-108">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span>

 

## <a name="ascii-text-archive-files"></a><span data-ttu-id="b5cec-109">Arquivos mortos de texto ASCII</span><span class="sxs-lookup"><span data-stu-id="b5cec-109">ASCII Text Archive Files</span></span>

<span data-ttu-id="b5cec-110">Os [arquivos mortos de texto](text-archive-files.md) ASCII exportados por [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) são explicados no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="b5cec-110">The ASCII [Text Archive Files](text-archive-files.md) exported by [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) are explained in the following format:</span></span>

-   <span data-ttu-id="b5cec-111">Os nomes das colunas da tabela são gravados na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="b5cec-111">The names of the table columns are written on the first line.</span></span>
-   <span data-ttu-id="b5cec-112">Os formatos de coluna são gravados na segunda linha.</span><span class="sxs-lookup"><span data-stu-id="b5cec-112">The column formats are written on the second line.</span></span>
-   <span data-ttu-id="b5cec-113">Se a tabela contiver apenas dados ASCII, a terceira linha do arquivo de texto será o nome da tabela seguido de uma lista das chaves primárias.</span><span class="sxs-lookup"><span data-stu-id="b5cec-113">If the table contains only ASCII data, the third line of the text file is the table name followed by a list of the primary keys.</span></span>
-   <span data-ttu-id="b5cec-114">Se a tabela contiver dados não ASCII e o banco de dado for carimbado com uma página de código numérica, o número da página de código aparecerá no início da terceira linha.</span><span class="sxs-lookup"><span data-stu-id="b5cec-114">If the table contains non-ASCII data and the database is stamped with a numeric code page, the code page number appears at the beginning of the third line.</span></span>
-   <span data-ttu-id="b5cec-115">Se o banco de dados contiver um dado não-ASCII, mas não estiver carimbado com a página de código numérico, o número da página de código do sistema atual será gravado no início da terceira linha.</span><span class="sxs-lookup"><span data-stu-id="b5cec-115">If the database contains non-ASCII data, but the database is not stamped with the numeric code page, the current system code page number is written at the beginning of the third line.</span></span>
-   <span data-ttu-id="b5cec-116">As linhas restantes do arquivo de texto são os dados na página de código especificada.</span><span class="sxs-lookup"><span data-stu-id="b5cec-116">The remaining lines of the text file are the data in the specified code page.</span></span>
-   <span data-ttu-id="b5cec-117">Se uma tabela contiver fluxos, o [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exporta cada fluxo na tabela para um arquivo separado.</span><span class="sxs-lookup"><span data-stu-id="b5cec-117">If a table contains streams, [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exports each stream in the table to a separate file.</span></span>

### <a name="neutral-and-non-neutral-code-pages"></a><span data-ttu-id="b5cec-118">Páginas de código neutras e não neutras</span><span class="sxs-lookup"><span data-stu-id="b5cec-118">Neutral and Non-Neutral Code Pages</span></span>

<span data-ttu-id="b5cec-119">Você pode facilitar a localização iniciando com um banco de dados que tem uma página de código neutra:</span><span class="sxs-lookup"><span data-stu-id="b5cec-119">You can facilitate localization by starting with a database that has a neutral code page:</span></span>

-   <span data-ttu-id="b5cec-120">Um banco de dados em branco tem uma página de código neutra.</span><span class="sxs-lookup"><span data-stu-id="b5cec-120">A blank database has a neutral code page.</span></span>
-   <span data-ttu-id="b5cec-121">Um banco de dados que não contém caracteres estendidos que exigem uma página de código para ser representado em ASCII tem uma página de código neutra.</span><span class="sxs-lookup"><span data-stu-id="b5cec-121">A database that does not contain extended characters that require a code page to be represented in ASCII has a neutral code page.</span></span>

<span data-ttu-id="b5cec-122">Para obter mais informações, consulte [criando um banco de dados com uma página de código neutra](creating-a-database-with-a-neutral-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="b5cec-122">For more information, see [Creating a Database with a Neutral Code Page](creating-a-database-with-a-neutral-code-page.md).</span></span>

<span data-ttu-id="b5cec-123">As páginas de código neutras e não neutras têm as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="b5cec-123">Neutral and non-neutral code pages have the following characteristics:</span></span>

-   <span data-ttu-id="b5cec-124">Se um [arquivo morto de texto](text-archive-files.md) com uma página de código não neutra for importado para um banco de dados que tenha uma página de código diferente de neutro, o instalador retornará um erro quando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) for chamado.</span><span class="sxs-lookup"><span data-stu-id="b5cec-124">If a [Text Archive File](text-archive-files.md) with a non-neutral code page is imported into a database that has a different non-neutral code page, the Installer returns an error when [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) is called.</span></span>
-   <span data-ttu-id="b5cec-125">Um [arquivo morto de texto](text-archive-files.md) que tem uma página de código neutra pode ser importado para um banco de dados que tenha qualquer página de código.</span><span class="sxs-lookup"><span data-stu-id="b5cec-125">A [Text Archive File](text-archive-files.md) that has a neutral code page can be imported into a database that has any code page.</span></span>
-   <span data-ttu-id="b5cec-126">Um [arquivo morto de texto](text-archive-files.md) que tem qualquer página de código pode ser importado para um banco de dados que tem uma página de código neutra.</span><span class="sxs-lookup"><span data-stu-id="b5cec-126">A [Text Archive File](text-archive-files.md) that has any code page can be imported into a database that has a neutral code page.</span></span>
-   <span data-ttu-id="b5cec-127">A importação de um [arquivo morto de texto](text-archive-files.md) em um banco de dados com uma página de código neutra define a página de código do banco de dados para a página de código do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="b5cec-127">Importing a [Text Archive File](text-archive-files.md) into a database with a neutral code page sets the code page of the database to the archive file code page.</span></span> <span data-ttu-id="b5cec-128">Todos os arquivos mortos subsequentemente importados para o banco de dados devem ter a mesma página de código que o primeiro arquivo.</span><span class="sxs-lookup"><span data-stu-id="b5cec-128">All archive files subsequently imported into the database must have the same code page as the first file.</span></span>

<span data-ttu-id="b5cec-129">Para obter mais informações, consulte [determinando uma página de código do banco de dados de instalação](determining-an-installation-database-s-code-page.md) e [definindo a página de código de um banco de dados](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="b5cec-129">For more information, see [Determining an Installation Database Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

<span data-ttu-id="b5cec-130">Os [arquivos mortos de texto](text-archive-files.md) exportados pelo [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) podem ser usados com sistemas de controle de versão.</span><span class="sxs-lookup"><span data-stu-id="b5cec-130">The [Text Archive Files](text-archive-files.md) that are exported by [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) can be used with version control systems.</span></span> <span data-ttu-id="b5cec-131">Use as [funções de banco](database-functions.md) de dados ou um editor de tabela de banco de dados para editar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b5cec-131">Use the [Database Functions](database-functions.md) or a database table editor to edit the database.</span></span>

<span data-ttu-id="b5cec-132">Você pode adicionar informações de localização a um banco de dados de instalação usando um editor de tabela de banco de dados ou a API Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b5cec-132">You can add localization information to an installation database by using a database table editor or the Windows Installer API.</span></span> <span data-ttu-id="b5cec-133">Para obter mais informações, consulte [manipulação de página de código de cadeias de caracteres de parâmetro](code-page-handling-of-parameter-strings.md).</span><span class="sxs-lookup"><span data-stu-id="b5cec-133">For more information, see [Code Page Handling of Parameter Strings](code-page-handling-of-parameter-strings.md).</span></span>

 

 



