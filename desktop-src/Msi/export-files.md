---
description: O arquivo VBScript WiExport.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Exportar arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760840"
---
# <a name="export-files"></a><span data-ttu-id="a5641-103">Exportar arquivos</span><span class="sxs-lookup"><span data-stu-id="a5641-103">Export Files</span></span>

<span data-ttu-id="a5641-104">O arquivo VBScript WiExport.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="a5641-104">The VBScript file WiExport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="a5641-105">Este exemplo mostra como gravar script para exportar tabelas para um banco de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a5641-105">This sample shows how to write script to export tables into a Windows Installer database.</span></span> <span data-ttu-id="a5641-106">O script de exemplo se conecta a um objeto do [**instalador**](installer-object.md) , abre um banco de dados e exporta tabelas para arquivos mortos.</span><span class="sxs-lookup"><span data-stu-id="a5641-106">The script sample connects to an [**Installer**](installer-object.md) object, opens a database and exports tables to archive files.</span></span>

<span data-ttu-id="a5641-107">O exemplo demonstra o uso de:</span><span class="sxs-lookup"><span data-stu-id="a5641-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="a5641-108">**Método OpenDatabase (objeto instalador)**</span><span class="sxs-lookup"><span data-stu-id="a5641-108">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="a5641-109">[**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="a5641-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="a5641-110">**Método de exportação**</span><span class="sxs-lookup"><span data-stu-id="a5641-110">**Export method**</span></span>](database-export.md)
-   <span data-ttu-id="a5641-111">[**Método OpenView**](database-openview.md) do [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="a5641-111">[**OpenView method**](database-openview.md) of the [**Database object**](database-object.md)</span></span>
-   <span data-ttu-id="a5641-112">[**Método FETCH**](view-fetch.md) do [ **objeto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="a5641-112">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   <span data-ttu-id="a5641-113">[**Propriedade StringData**](record-stringdata.md) do [ **objeto Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="a5641-113">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="a5641-114">Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="a5641-114">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="a5641-115">Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5641-115">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="a5641-116">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="a5641-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="a5641-117">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="a5641-117">or if too few arguments are specified.</span></span> <span data-ttu-id="a5641-118">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="a5641-118">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="a5641-119">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="a5641-119">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="a5641-120">**cscript WiExport.vbs \[ caminho para o caminho do banco \] \[ de dados para \] \[ as opções de pasta lista de \] \[ nomes de tabela\]**</span><span class="sxs-lookup"><span data-stu-id="a5641-120">**cscript WiExport.vbs \[path to database\]\[path to folder\]\[options\]\[table name list\]**</span></span>

<span data-ttu-id="a5641-121">Especifique o caminho para o banco de dados do instalador do qual as tabelas estão sendo exportadas.</span><span class="sxs-lookup"><span data-stu-id="a5641-121">Specify the path to the installer database from which the tables are being exported.</span></span> <span data-ttu-id="a5641-122">Especifique o caminho para a pasta na qual os arquivos mortos exportados devem ser copiados.</span><span class="sxs-lookup"><span data-stu-id="a5641-122">Specify the path to the folder into which the exported archive files are to be copied.</span></span> <span data-ttu-id="a5641-123">Listar os nomes que diferenciam maiúsculas de minúsculas das [tabelas de banco de dados](database-tables.md) que estão sendo</span><span class="sxs-lookup"><span data-stu-id="a5641-123">List the case-sensitive names of the [database tables](database-tables.md) being exported.</span></span> <span data-ttu-id="a5641-124">Especifique ' \* ' para exportar todas as tabelas, incluindo \_ SummaryInformation.</span><span class="sxs-lookup"><span data-stu-id="a5641-124">Specify '\*' to export all the tables including \_SummaryInformation.</span></span>

<span data-ttu-id="a5641-125">As opções a seguir podem ser especificadas em qualquer lugar na linha de comando antes da lista nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="a5641-125">The following options may be specified anywhere on the command line before the table name list.</span></span>



| <span data-ttu-id="a5641-126">Opção</span><span class="sxs-lookup"><span data-stu-id="a5641-126">Option</span></span>              | <span data-ttu-id="a5641-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5641-127">Description</span></span>                                            |
|---------------------|--------------------------------------------------------|
| <span data-ttu-id="a5641-128">nenhuma opção especificada</span><span class="sxs-lookup"><span data-stu-id="a5641-128">no option specified</span></span> | <span data-ttu-id="a5641-129">Arquivos mortos exportados podem ter um nome de arquivo longo.</span><span class="sxs-lookup"><span data-stu-id="a5641-129">Exported archive files may have a long file name.</span></span>      |
| <span data-ttu-id="a5641-130">/s</span><span class="sxs-lookup"><span data-stu-id="a5641-130">/s</span></span>                  | <span data-ttu-id="a5641-131">Force os arquivos exportados para terem nomes de arquivo curtos.</span><span class="sxs-lookup"><span data-stu-id="a5641-131">Force exported archive files to have short file names.</span></span> |



 

<span data-ttu-id="a5641-132">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="a5641-132">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="a5641-133">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a5641-133">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



