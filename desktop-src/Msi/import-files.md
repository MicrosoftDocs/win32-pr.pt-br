---
description: O arquivo VBScript WiImport.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo mostra como gravar um script para importar tabelas para um banco de dados Windows Installer.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importar arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752254"
---
# <a name="import-files"></a><span data-ttu-id="71e31-104">Importar arquivos</span><span class="sxs-lookup"><span data-stu-id="71e31-104">Import Files</span></span>

<span data-ttu-id="71e31-105">O arquivo VBScript WiImport.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="71e31-105">The VBScript file WiImport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="71e31-106">Este exemplo mostra como gravar um script para importar tabelas para um banco de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="71e31-106">This sample shows how to write a script to import tables into a Windows Installer database.</span></span>

<span data-ttu-id="71e31-107">O script se conecta a um objeto do [**instalador**](installer-object.md) , abre um banco de dados, processa uma lista de arquivos e confirma as alterações antes de fechar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71e31-107">The script connects to an [**Installer**](installer-object.md) object, opens a database, processes a list of files, and commits the changes before closing the database.</span></span>

<span data-ttu-id="71e31-108">O exemplo demonstra o uso de:</span><span class="sxs-lookup"><span data-stu-id="71e31-108">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="71e31-109">**Método OpenDatabase (objeto instalador)**</span><span class="sxs-lookup"><span data-stu-id="71e31-109">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="71e31-110">[**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="71e31-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="71e31-111">**Método Import**</span><span class="sxs-lookup"><span data-stu-id="71e31-111">**Import method**</span></span>](database-import.md)
-   <span data-ttu-id="71e31-112">[**Método Commit**](database-commit.md) do [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="71e31-112">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="71e31-113">Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="71e31-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="71e31-114">Para usar CScript.exe para executar este exemplo, use a sintaxe a seguir no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="71e31-114">To use CScript.exe to run this sample, use the following syntax at the command prompt.</span></span>

<span data-ttu-id="71e31-115">**cscript WiImport.vbs \[ caminho para o caminho do banco \] \[ de dados para \] \[ as opções de pasta lista de \] \[ arquivos de arquivo**\]</span><span class="sxs-lookup"><span data-stu-id="71e31-115">**cscript WiImport.vbs \[path to database\]\[path to folder\]\[options\] \[archive file list**\]</span></span>

<span data-ttu-id="71e31-116">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="71e31-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="71e31-117">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="71e31-117">or if too few arguments are specified.</span></span> <span data-ttu-id="71e31-118">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ caminho para o arquivo \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="71e31-118">To redirect the output to a file, end the command line with VBS > \[path to file\].The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="71e31-119">Especifique o caminho para um banco de dados do Windows Installer que será criado ou que deve receber as tabelas importadas.</span><span class="sxs-lookup"><span data-stu-id="71e31-119">Specify the path to a Windows installer database that is to be created or that is to receive the imported tables.</span></span> <span data-ttu-id="71e31-120">Especifique o caminho para a pasta que contém os arquivos mortos das tabelas que estão sendo importadas.</span><span class="sxs-lookup"><span data-stu-id="71e31-120">Specify the path to the folder containing the archive files of the tables that are being imported.</span></span> <span data-ttu-id="71e31-121">Liste os nomes dos arquivos mortos que estão sendo importados.</span><span class="sxs-lookup"><span data-stu-id="71e31-121">List the names of the archive files that are being imported.</span></span> <span data-ttu-id="71e31-122">Nomes de arquivo curinga, como \* . IDT, podem ser usados para importar vários arquivos.</span><span class="sxs-lookup"><span data-stu-id="71e31-122">Wildcard file names, such as \*.idt, can be used to import multiple files.</span></span>

<span data-ttu-id="71e31-123">As opções a seguir podem ser especificadas em qualquer lugar na linha de comando antes da lista de arquivos.</span><span class="sxs-lookup"><span data-stu-id="71e31-123">The following options may be specified anywhere on the command line before the file list.</span></span>



| <span data-ttu-id="71e31-124">Opção</span><span class="sxs-lookup"><span data-stu-id="71e31-124">Option</span></span>              | <span data-ttu-id="71e31-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="71e31-125">Description</span></span>                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71e31-126">nenhuma opção especificada</span><span class="sxs-lookup"><span data-stu-id="71e31-126">no option specified</span></span> | <span data-ttu-id="71e31-127">Importe a lista de arquivos de tabela arquivados da pasta especificada para o banco de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="71e31-127">Import the list of table archive files from the specified folder into the Windows Installer database.</span></span>                                |
| <span data-ttu-id="71e31-128">/c</span><span class="sxs-lookup"><span data-stu-id="71e31-128">/c</span></span>                  | <span data-ttu-id="71e31-129">Crie um banco de dados Windows Installer e importe a lista de arquivos de tabela de arquivo da pasta especificada para o novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71e31-129">Create a Windows Installer database and then import the list of table archive files from the specified folder into the new database.</span></span> |



 

<span data-ttu-id="71e31-130">Para obter mais informações, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md) para obter exemplos de script adicionais.</span><span class="sxs-lookup"><span data-stu-id="71e31-130">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="71e31-131">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="71e31-131">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="71e31-132">Observe que [um exemplo de localização](a-localization-example.md) também demonstra a [importação de tabelas de erro e ActionText localizadas](importing-localized-error-and-actiontext-tables.md).</span><span class="sxs-lookup"><span data-stu-id="71e31-132">Note that [A Localization Example](a-localization-example.md) also demonstrates [Importing Localized Error and ActionText Tables](importing-localized-error-and-actiontext-tables.md).</span></span>

 

 



