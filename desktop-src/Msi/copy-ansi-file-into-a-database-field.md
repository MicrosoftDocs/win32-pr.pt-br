---
description: O arquivo de exemplo de código VBScript WiTextIn.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: Copiar arquivo ANSI em um campo de banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811854"
---
# <a name="copy-ansi-file-into-a-database-field"></a><span data-ttu-id="1bba8-103">Copiar arquivo ANSI em um campo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="1bba8-103">Copy ANSI File Into a Database Field</span></span>

<span data-ttu-id="1bba8-104">O arquivo de exemplo de código VBScript WiTextIn.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="1bba8-104">The VBScript code sample file WiTextIn.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="1bba8-105">O exemplo mostra como um script pode ser usado para copiar um arquivo em um campo de texto de um banco de dados de Windows Installer e demonstra o processamento de seus principais.</span><span class="sxs-lookup"><span data-stu-id="1bba8-105">The sample shows how a script can be used to copy a file into a text field of a Windows Installer database, and demonstrates the processing of primary key data.</span></span>

<span data-ttu-id="1bba8-106">O exemplo de código também mostra o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1bba8-106">The code sample also shows you the following:</span></span>

-   <span data-ttu-id="1bba8-107">[**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md) e o [**método LastErrorRecord**](installer-lasterrorrecord.md) do [**objeto instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="1bba8-107">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md) and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="1bba8-108">[**Método OpenView**](database-openview.md), o [**método Commit**](database-commit.md)e a [**Propriedade primarykeys**](database-primarykeys.md) do [**objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="1bba8-108">[**OpenView method**](database-openview.md), the [**Commit method**](database-commit.md), and the [**PrimaryKeys property**](database-primarykeys.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="1bba8-109">[**Método FETCH**](view-fetch.md) e o [**método Modify**](view-modify.md) do [**objeto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="1bba8-109">[**Fetch method**](view-fetch.md) and the [**Modify method**](view-modify.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="1bba8-110">[**Propriedade StringData**](record-stringdata.md) e [**método ReadStream**](record-readstream.md) do [**objeto Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="1bba8-110">[**StringData property**](record-stringdata.md) and [**ReadStream method**](record-readstream.md) of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="1bba8-111">Para usar o exemplo de código, você precisa da versão CScript.exe ou WScript.exe do Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="1bba8-111">To use the code sample you need the CScript.exe or WScript.exe version of Windows Script Host.</span></span>

<span data-ttu-id="1bba8-112">**Para usar CScript.exe para executar este exemplo**</span><span class="sxs-lookup"><span data-stu-id="1bba8-112">**To use CScript.exe to run this sample**</span></span>

-   <span data-ttu-id="1bba8-113">No prompt de comando, digite a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="1bba8-113">At the command prompt, type the following syntax:</span></span>

    <span data-ttu-id="1bba8-114">**cscript WiTextIn.vbs \[ caminho para a tabela do banco de dados \] \[ nome da \] \[ coluna valores de chave primária \] \[ nome do \] \[ caminho para arquivo\]**</span><span class="sxs-lookup"><span data-stu-id="1bba8-114">**cscript WiTextIn.vbs \[path to database\]\[table name\]\[primary key values\]\[column name\]\[path to file\]**</span></span>

> [!Note]  
> <span data-ttu-id="1bba8-115">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="1bba8-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="1bba8-116">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="1bba8-116">or if too few arguments are specified.</span></span>

 

<span data-ttu-id="1bba8-117">**Para redirecionar a saída para um arquivo**</span><span class="sxs-lookup"><span data-stu-id="1bba8-117">**To redirect the output to a file**</span></span>

-   <span data-ttu-id="1bba8-118">Termine a linha de comando com o seguinte: **VBS > \[ caminho para o arquivo \] . T**</span><span class="sxs-lookup"><span data-stu-id="1bba8-118">End the command line with the following: **VBS > \[path to file\]. T**</span></span>

> [!Note]  
> <span data-ttu-id="1bba8-119">O exemplo retorna um valor de 0 (zero) para êxito, 1 (um) se a ajuda for invocada e 2 (dois) se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="1bba8-119">The sample returns a value of 0 (zero) for success, 1 (one) if Help is invoked, and 2 (two) if the script fails.</span></span>

 

<span data-ttu-id="1bba8-120">A lista a seguir identifica os itens que você deve especificar:</span><span class="sxs-lookup"><span data-stu-id="1bba8-120">The following list identifies the items that you must specify:</span></span>

-   <span data-ttu-id="1bba8-121">Especifique o caminho para o banco de dados de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1bba8-121">Specify the path to the Windows Installer database.</span></span>
-   <span data-ttu-id="1bba8-122">Especifique o nome da tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1bba8-122">Specify the name of the database table.</span></span>
-   <span data-ttu-id="1bba8-123">Especifique todos os valores de chave primária para a linha, em ordem, e concatenados com dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="1bba8-123">Specify all the primary key values for the row, in order, and concatenated with colons.</span></span>
-   <span data-ttu-id="1bba8-124">Especifique um nome de coluna que não seja uma coluna de chave.</span><span class="sxs-lookup"><span data-stu-id="1bba8-124">Specify a column name that is not a key column.</span></span> <span data-ttu-id="1bba8-125">Essa é a coluna na qual você deseja receber os dados.</span><span class="sxs-lookup"><span data-stu-id="1bba8-125">This is the column that you want to receive the data.</span></span>
-   <span data-ttu-id="1bba8-126">Especifique o caminho para o arquivo de texto que está sendo copiado.</span><span class="sxs-lookup"><span data-stu-id="1bba8-126">Specify the path to the text file that is being copied.</span></span>

> [!Note]  
> <span data-ttu-id="1bba8-127">Se o último argumento for omitido, o valor atual no campo será exibido.</span><span class="sxs-lookup"><span data-stu-id="1bba8-127">If the last argument is omitted, the current value in the field is displayed.</span></span>

 

<span data-ttu-id="1bba8-128">Para obter mais exemplos de script, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="1bba8-128">For more scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="1bba8-129">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="1bba8-129">For sample utilities that do not require the Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



