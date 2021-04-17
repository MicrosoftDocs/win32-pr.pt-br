---
description: O arquivo VBScript WiLstXfm.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo de script pode ser usado para exibir um arquivo de transformação.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Exibir uma transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749566"
---
# <a name="view-a-transform"></a><span data-ttu-id="a8c38-104">Exibir uma transformação</span><span class="sxs-lookup"><span data-stu-id="a8c38-104">View a Transform</span></span>

<span data-ttu-id="a8c38-105">O arquivo VBScript WiLstXfm.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="a8c38-105">The VBScript file WiLstXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="a8c38-106">Este exemplo de script pode ser usado para exibir um arquivo de transformação.</span><span class="sxs-lookup"><span data-stu-id="a8c38-106">This script sample can be used to view a transform file.</span></span>

<span data-ttu-id="a8c38-107">O exemplo demonstra o uso de:</span><span class="sxs-lookup"><span data-stu-id="a8c38-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="a8c38-108">\_Tabela de transformview</span><span class="sxs-lookup"><span data-stu-id="a8c38-108">\_TransformView table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="a8c38-109">**Método OpenDatabase (objeto instalador)**</span><span class="sxs-lookup"><span data-stu-id="a8c38-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="a8c38-110">[**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="a8c38-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="a8c38-111">**Método ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="a8c38-111">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="a8c38-112">**Método OpenView**</span><span class="sxs-lookup"><span data-stu-id="a8c38-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="a8c38-113">[**Método Commit**](database-commit.md) do [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="a8c38-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="a8c38-114">**Propriedade IsNull**</span><span class="sxs-lookup"><span data-stu-id="a8c38-114">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="a8c38-115">[**Propriedade StringData**](record-stringdata.md) do [ **objeto Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="a8c38-115">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="a8c38-116">O uso deste exemplo requer a versão CScript.exe do Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="a8c38-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="a8c38-117">Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8c38-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="a8c38-118">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="a8c38-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="a8c38-119">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="a8c38-119">or if too few arguments are specified.</span></span> <span data-ttu-id="a8c38-120">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="a8c38-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="a8c38-121">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="a8c38-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="a8c38-122">**cscript WiLstXfm.vbs** *\[ caminho para o caminho de opção de banco de dados de referência \] \[ \] \[ a ser exibido \] para transformação*</span><span class="sxs-lookup"><span data-stu-id="a8c38-122">**cscript WiLstXfm.vbs** *\[path to reference database\]\[option\]\[path to transform to be viewed\]*</span></span>

<span data-ttu-id="a8c38-123">Especifique o caminho para a referência Windows Installer banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a8c38-123">Specify the path to the reference Windows Installer database.</span></span> <span data-ttu-id="a8c38-124">Especifique uma lista de caminhos para transformar os arquivos que estão sendo exibidos.</span><span class="sxs-lookup"><span data-stu-id="a8c38-124">Specify a list of paths to transform files that are being viewed.</span></span> <span data-ttu-id="a8c38-125">Cada caminho na lista pode ser precedido por um valor numérico opcional.</span><span class="sxs-lookup"><span data-stu-id="a8c38-125">Each path in the list may by preceded by an optional numeric value.</span></span> <span data-ttu-id="a8c38-126">Esse valor especifica um conjunto de condições de erro que devem ser suprimidas.</span><span class="sxs-lookup"><span data-stu-id="a8c38-126">This value specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="a8c38-127">Você pode adicionar esses valores juntos para suprimir várias condições.</span><span class="sxs-lookup"><span data-stu-id="a8c38-127">You may add these values together to suppress multiple conditions.</span></span> <span data-ttu-id="a8c38-128">Se nenhuma opção numérica for especificada, todas as condições de erro serão suprimidas.</span><span class="sxs-lookup"><span data-stu-id="a8c38-128">If no numeric option is specified, all the error conditions are suppressed.</span></span> <span data-ttu-id="a8c38-129">Os argumentos nessa lista são executados na ordem da esquerda para a direita na qual aparecem na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a8c38-129">The arguments in this list are executed in the left-to-right order in which they appear on the command line.</span></span>



| <span data-ttu-id="a8c38-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a8c38-130">Value</span></span> | <span data-ttu-id="a8c38-131">Condição de erro para suprimir</span><span class="sxs-lookup"><span data-stu-id="a8c38-131">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="a8c38-132">1</span><span class="sxs-lookup"><span data-stu-id="a8c38-132">1</span></span>     | <span data-ttu-id="a8c38-133">Adicionando uma linha que já existe.</span><span class="sxs-lookup"><span data-stu-id="a8c38-133">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="a8c38-134">2</span><span class="sxs-lookup"><span data-stu-id="a8c38-134">2</span></span>     | <span data-ttu-id="a8c38-135">Excluindo uma linha que não existe.</span><span class="sxs-lookup"><span data-stu-id="a8c38-135">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="a8c38-136">4</span><span class="sxs-lookup"><span data-stu-id="a8c38-136">4</span></span>     | <span data-ttu-id="a8c38-137">Adicionando uma tabela que já existe.</span><span class="sxs-lookup"><span data-stu-id="a8c38-137">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="a8c38-138">8</span><span class="sxs-lookup"><span data-stu-id="a8c38-138">8</span></span>     | <span data-ttu-id="a8c38-139">Excluindo uma tabela que não existe.</span><span class="sxs-lookup"><span data-stu-id="a8c38-139">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="a8c38-140">16</span><span class="sxs-lookup"><span data-stu-id="a8c38-140">16</span></span>    | <span data-ttu-id="a8c38-141">Atualizando uma linha que não existe.</span><span class="sxs-lookup"><span data-stu-id="a8c38-141">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="a8c38-142">256</span><span class="sxs-lookup"><span data-stu-id="a8c38-142">256</span></span>   | <span data-ttu-id="a8c38-143">Incompatibilidade de páginas de código de banco de dados e transformação.</span><span class="sxs-lookup"><span data-stu-id="a8c38-143">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="a8c38-144">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="a8c38-144">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="a8c38-145">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a8c38-145">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



