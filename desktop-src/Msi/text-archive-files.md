---
description: As tabelas de banco de dados Windows Installer podem ser exportadas para arquivos de texto ASCII usando MsiDatabaseExport ou o método de exportação do objeto de banco de dados.
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: Arquivos mortos de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baba814fd182a7da5e13fbb26eec257be96ab1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828702"
---
# <a name="text-archive-files"></a><span data-ttu-id="eafc6-103">Arquivos mortos de texto</span><span class="sxs-lookup"><span data-stu-id="eafc6-103">Text Archive Files</span></span>

<span data-ttu-id="eafc6-104">As tabelas de banco de dados Windows Installer podem ser exportadas para arquivos de texto ASCII usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) ou o método de [**exportação**](database-export.md) do objeto de [**banco de dados**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="eafc6-104">The Windows Installer database tables can be exported to ASCII text files by using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) or the [**Export**](database-export.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="eafc6-105">As informações contidas nesses arquivos de texto podem ser importadas de volta para um Windows Installer banco de dados usando o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) ou o método de [importação](database-import.md) do objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="eafc6-105">The information in these text archive files can then be imported back into a Windows Installer database using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the **Database** object.</span></span>

<span data-ttu-id="eafc6-106">Ferramentas como [msidb.exe](msidb-exe.md) são capazes de exportar e importar arquivos mortos de texto.</span><span class="sxs-lookup"><span data-stu-id="eafc6-106">Tools such as [msidb.exe](msidb-exe.md) are capable of exporting and importing text archive files.</span></span> <span data-ttu-id="eafc6-107">Consulte [exportar arquivos](export-files.md) e [importar arquivos](import-files.md) para obter [Windows Installer exemplos de script](windows-installer-scripting-examples.md) que podem exportar e importar arquivos de texto arquivados de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="eafc6-107">See [Export Files](export-files.md) and [Import Files](import-files.md) for [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) that can export and import text archive files from a database.</span></span>

> [!Note]  
> <span data-ttu-id="eafc6-108">Arquivos de texto arquivados não são destinados a um meio de editar o banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="eafc6-108">Text archive files are not intended as a means to edit the installation database.</span></span> <span data-ttu-id="eafc6-109">Você deve usar uma ferramenta de edição de tabela Windows Installer, como [Orca](orca-exe.md) ou uma ferramenta de terceiros, para criar e modificar um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="eafc6-109">You should use a Windows Installer table editing tool, such as [Orca](orca-exe.md) or a third-party tool, to create and modify an installation package.</span></span>

 

<span data-ttu-id="eafc6-110">Os arquivos mortos de texto podem ser usados para as seguintes finalidades.</span><span class="sxs-lookup"><span data-stu-id="eafc6-110">Text archive files can be used for the following purposes.</span></span>

-   <span data-ttu-id="eafc6-111">Arquivos de texto arquivados podem ser usados com sistemas de controle de versão.</span><span class="sxs-lookup"><span data-stu-id="eafc6-111">Text archive files can be used with version control systems.</span></span>
-   <span data-ttu-id="eafc6-112">Para remover o espaço de armazenamento desperdiçado e reduzir o tamanho final dos arquivos. msi.</span><span class="sxs-lookup"><span data-stu-id="eafc6-112">To remove wasted storage space and reduce the final size of .msi files.</span></span> <span data-ttu-id="eafc6-113">Consulte [reduzindo o tamanho de um arquivo. msi](reducing-the-size-of-an--msi-file.md).</span><span class="sxs-lookup"><span data-stu-id="eafc6-113">See [Reducing the Size of an .msi File](reducing-the-size-of-an--msi-file.md).</span></span>
-   <span data-ttu-id="eafc6-114">Para adicionar informações de localização a um banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="eafc6-114">To add localization information to an installation database.</span></span> <span data-ttu-id="eafc6-115">Para obter mais informações, consulte [manipulação de página de código de tabelas importadas e](code-page-handling-of-imported-and-exported-tables.md)exportadas.</span><span class="sxs-lookup"><span data-stu-id="eafc6-115">For more information, see [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

-   <span data-ttu-id="eafc6-116">Para determinar a página de código de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="eafc6-116">To determine the code page of a database.</span></span> <span data-ttu-id="eafc6-117">Consulte [determinando a página de código de um banco de dados de instalação](determining-an-installation-database-s-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="eafc6-117">See [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md).</span></span>
-   <span data-ttu-id="eafc6-118">Para definir a página de código de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="eafc6-118">To set the code page of a database.</span></span> <span data-ttu-id="eafc6-119">Consulte [Configurando a página de código de um banco de dados](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="eafc6-119">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="eafc6-120">Para aumentar o limite de uma coluna de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="eafc6-120">To increase the limit of a database column.</span></span> <span data-ttu-id="eafc6-121">Exporte a tabela usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), edite o arquivo. IDT exportado e importe a tabela usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="eafc6-121">Export the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), edit the exported .idt file, and then import the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="eafc6-122">Os autores não podem alterar os tipos de dados de coluna, a nulidade ou os atributos de localização de colunas em tabelas padrão.</span><span class="sxs-lookup"><span data-stu-id="eafc6-122">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="eafc6-123">Consulte também [criando um pacote grande](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="eafc6-123">See also [Authoring a Large Package](authoring-a-large-package.md).</span></span>

<span data-ttu-id="eafc6-124">As páginas a seguir descrevem as páginas de arquivamento de texto e seus formatos.</span><span class="sxs-lookup"><span data-stu-id="eafc6-124">The following pages describe text archive pages and their formats.</span></span>

-   [<span data-ttu-id="eafc6-125">Formato de arquivo morto</span><span class="sxs-lookup"><span data-stu-id="eafc6-125">Archive File Format</span></span>](archive-file-format.md)
-   [<span data-ttu-id="eafc6-126">Dados ASCII em arquivos mortos de texto</span><span class="sxs-lookup"><span data-stu-id="eafc6-126">ASCII Data in Text Archive Files</span></span>](ascii-data-in-text-archive-files.md)
-   [<span data-ttu-id="eafc6-127">\_ForceCodepage</span><span class="sxs-lookup"><span data-stu-id="eafc6-127">\_ForceCodepage</span></span>](-forcecodepage.md)
-   [<span data-ttu-id="eafc6-128">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="eafc6-128">\_SummaryInformation</span></span>](-summaryinformation.md)

 

 



