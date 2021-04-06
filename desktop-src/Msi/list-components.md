---
description: O arquivo VBScript WiCompon.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este script de exemplo pode ser usado para listar os componentes em um banco de dados Windows Installer.
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: Listar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b79fa34f62374632ec7fdf52a13c6da8ddbfd82a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647200"
---
# <a name="list-components"></a><span data-ttu-id="60fd3-104">Listar componentes</span><span class="sxs-lookup"><span data-stu-id="60fd3-104">List Components</span></span>

<span data-ttu-id="60fd3-105">O arquivo VBScript WiCompon.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="60fd3-105">The VBScript file WiCompon.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="60fd3-106">Este script de exemplo pode ser usado para listar os componentes em um banco de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="60fd3-106">This sample script can be used to list the components in a Windows Installer database.</span></span>

<span data-ttu-id="60fd3-107">Este exemplo demonstra o uso de várias chaves primárias na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="60fd3-107">This sample demonstrates using the various primary key in the [Component table](component-table.md).</span></span>

<span data-ttu-id="60fd3-108">O exemplo também demonstra:</span><span class="sxs-lookup"><span data-stu-id="60fd3-108">The sample also demonstrates:</span></span>

-   <span data-ttu-id="60fd3-109">[**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md), o [**método CreateRecord**](installer-createrecord.md)e o [**método LastErrorRecord**](installer-lasterrorrecord.md) do [**objeto instalador**](installer-object.md).</span><span class="sxs-lookup"><span data-stu-id="60fd3-109">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md), the [**CreateRecord method**](installer-createrecord.md), and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md).</span></span>
-   <span data-ttu-id="60fd3-110">[**Método OpenView**](database-openview.md), a [**Propriedade TablePersistent**](database-tablepersistent.md)e a [**Propriedade primarykeys**](database-primarykeys.md) do [**objeto Database**](database-object.md).</span><span class="sxs-lookup"><span data-stu-id="60fd3-110">[**OpenView method**](database-openview.md), the [**TablePersistent property**](database-tablepersistent.md), and the [**PrimaryKeys property**](database-primarykeys.md) of the [**Database Object**](database-object.md).</span></span>
-   <span data-ttu-id="60fd3-111">[**Método execute**](view-execute.md) e o [**método FETCH**](view-fetch.md) do [**objeto View**](view-object.md).</span><span class="sxs-lookup"><span data-stu-id="60fd3-111">[**Execute method**](view-execute.md) and the [**Fetch method**](view-fetch.md) of the [**View Object**](view-object.md).</span></span>
-   <span data-ttu-id="60fd3-112">Propriedade da [**Propriedade StringData**](record-stringdata.md) do [**objeto Record**](record-object.md).</span><span class="sxs-lookup"><span data-stu-id="60fd3-112">[**StringData property**](record-stringdata.md) property of the [**Record Object**](record-object.md).</span></span>

<span data-ttu-id="60fd3-113">O uso deste exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="60fd3-113">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="60fd3-114">Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="60fd3-114">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="60fd3-115">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="60fd3-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="60fd3-116">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="60fd3-116">or if too few arguments are specified.</span></span> <span data-ttu-id="60fd3-117">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="60fd3-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="60fd3-118">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="60fd3-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="60fd3-119">**cscript WiCompon.vbs \[ caminho para o \] nome do componente de banco de dados \[\]**</span><span class="sxs-lookup"><span data-stu-id="60fd3-119">**cscript WiCompon.vbs \[path to database\]\[component name\]**</span></span>

<span data-ttu-id="60fd3-120">Especifique o caminho para o banco de dados de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="60fd3-120">Specify path to the Windows Installer database.</span></span> <span data-ttu-id="60fd3-121">Especifique o nome do componente.</span><span class="sxs-lookup"><span data-stu-id="60fd3-121">Specify the name of the component.</span></span> <span data-ttu-id="60fd3-122">O nome deve ser listado na coluna componente da tabela de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="60fd3-122">The name must be listed in the Component column of the [Component table](component-table.md).</span></span> <span data-ttu-id="60fd3-123">Se o nome do componente for omitido, todos os componentes serão listados.</span><span class="sxs-lookup"><span data-stu-id="60fd3-123">If the name of the component is omitted all the components are listed.</span></span> <span data-ttu-id="60fd3-124">Se um asterisco ( \* ) for usado como o nome do componente, WiCompon.vbs listará a composição de todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="60fd3-124">If an asterisk (\*) is used as the component name, WiCompon.vbs lists the composition of all components.</span></span> <span data-ttu-id="60fd3-125">Observe que bancos de dados grandes são mais bem exibidos usando CScript em vez de WScript.</span><span class="sxs-lookup"><span data-stu-id="60fd3-125">Note that large databases are better displayed using CScript rather than WScript.</span></span>

<span data-ttu-id="60fd3-126">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="60fd3-126">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="60fd3-127">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="60fd3-127">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



