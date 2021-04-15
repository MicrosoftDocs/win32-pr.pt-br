---
description: O arquivo VBScript WiDiffDb.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Esse script de exemplo gera um arquivo de transformação temporário entre dois bancos de dados do Windows Installer e exibe a transformação.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Exibir diferenças entre dois bancos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501596"
---
# <a name="view-differences-between-two-databases"></a><span data-ttu-id="8e8b7-104">Exibir diferenças entre dois bancos de dados</span><span class="sxs-lookup"><span data-stu-id="8e8b7-104">View Differences Between Two Databases</span></span>

<span data-ttu-id="8e8b7-105">O arquivo VBScript WiDiffDb.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="8e8b7-105">The VBScript file WiDiffDb.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="8e8b7-106">Esse script de exemplo gera um arquivo de transformação temporário entre dois bancos de dados do Windows Installer e exibe a transformação.</span><span class="sxs-lookup"><span data-stu-id="8e8b7-106">This sample script generates a temporary transform file between two Windows Installer databases and displays the transform.</span></span>

<span data-ttu-id="8e8b7-107">O exemplo demonstra o uso de:</span><span class="sxs-lookup"><span data-stu-id="8e8b7-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="8e8b7-108">**Método OpenDatabase (objeto instalador)**</span><span class="sxs-lookup"><span data-stu-id="8e8b7-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="8e8b7-109">[**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="8e8b7-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="8e8b7-110">**Método OpenView**</span><span class="sxs-lookup"><span data-stu-id="8e8b7-110">**OpenView method**</span></span>](database-openview.md)
-   [<span data-ttu-id="8e8b7-111">**Propriedade SummaryInformation (objeto Database)**</span><span class="sxs-lookup"><span data-stu-id="8e8b7-111">**SummaryInformation property (Database Object)**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="8e8b7-112">**Método GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="8e8b7-112">**GenerateTransform method**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="8e8b7-113">**Método ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="8e8b7-113">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="8e8b7-114">**Objeto de banco de dados**</span><span class="sxs-lookup"><span data-stu-id="8e8b7-114">**Database object**</span></span>](database-object.md)
-   <span data-ttu-id="8e8b7-115">[**Método FETCH**](view-fetch.md) do [ **objeto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="8e8b7-115">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="8e8b7-116">**Propriedade IsNull**</span><span class="sxs-lookup"><span data-stu-id="8e8b7-116">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="8e8b7-117">[**Propriedade StringData**](record-stringdata.md) do [ **objeto Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="8e8b7-117">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>
-   [<span data-ttu-id="8e8b7-118">\_Tabela de transformview</span><span class="sxs-lookup"><span data-stu-id="8e8b7-118">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="8e8b7-119">O uso deste exemplo requer a versão CScript.exe do Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="8e8b7-119">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="8e8b7-120">Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e8b7-120">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="8e8b7-121">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="8e8b7-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="8e8b7-122">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="8e8b7-122">or if too few arguments are specified.</span></span> <span data-ttu-id="8e8b7-123">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="8e8b7-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="8e8b7-124">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="8e8b7-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="8e8b7-125">**cscript WiDiffDb.vbs** *\[ caminho do caminho do banco de dados original \] \[ para o banco de dados \] revisado*</span><span class="sxs-lookup"><span data-stu-id="8e8b7-125">**cscript WiDiffDb.vbs** *\[path to original database\]\[path to revised database\]*</span></span>

<span data-ttu-id="8e8b7-126">Especifique o caminho para o banco de dados de Windows Installer original.</span><span class="sxs-lookup"><span data-stu-id="8e8b7-126">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="8e8b7-127">Especifique o caminho para o banco de dados revisado.</span><span class="sxs-lookup"><span data-stu-id="8e8b7-127">Specify the path to the revised database.</span></span> <span data-ttu-id="8e8b7-128">O script de exemplo exibirá a transformação.</span><span class="sxs-lookup"><span data-stu-id="8e8b7-128">The sample script will display the transform.</span></span>

<span data-ttu-id="8e8b7-129">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="8e8b7-129">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="8e8b7-130">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8e8b7-130">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



