---
description: O arquivo VBScript WiUseXfm.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo mostra como o script pode ser usado para aplicar uma transformação a um banco de dados Windows Installer.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Aplicar uma transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828073"
---
# <a name="apply-a-transform"></a><span data-ttu-id="da17d-104">Aplicar uma transformação</span><span class="sxs-lookup"><span data-stu-id="da17d-104">Apply a Transform</span></span>

<span data-ttu-id="da17d-105">O arquivo VBScript WiUseXfm.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="da17d-105">The VBScript file WiUseXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="da17d-106">Este exemplo mostra como o script pode ser usado para aplicar uma transformação a um banco de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="da17d-106">This sample shows how script can be used to apply a transform to a Windows Installer database.</span></span>

<span data-ttu-id="da17d-107">O exemplo demonstra o uso de</span><span class="sxs-lookup"><span data-stu-id="da17d-107">The sample demonstrates the use of</span></span>

-   [<span data-ttu-id="da17d-108">**Método OpenDatabase (objeto instalador)**</span><span class="sxs-lookup"><span data-stu-id="da17d-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="da17d-109">[**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="da17d-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="da17d-110">**Método ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="da17d-110">**ApplyTransform method**</span></span>](database-applytransform.md)
-   <span data-ttu-id="da17d-111">[**Método Commit**](database-commit.md) do [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="da17d-111">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="da17d-112">Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="da17d-112">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="da17d-113">Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="da17d-113">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="da17d-114">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="da17d-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="da17d-115">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="da17d-115">or if too few arguments are specified.</span></span> <span data-ttu-id="da17d-116">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="da17d-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="da17d-117">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="da17d-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="da17d-118">**cscript WiUseXfm.vbs \[ caminho para o caminho do banco de dados original \] \[ para \] \[ as opções de arquivo de transformação\]**</span><span class="sxs-lookup"><span data-stu-id="da17d-118">**cscript WiUseXfm.vbs \[path to original database\]\[path to transform file\]\[options\]**</span></span>

<span data-ttu-id="da17d-119">Especifique o caminho para o banco de dados de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="da17d-119">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="da17d-120">Especifique o caminho para o arquivo de transformação.</span><span class="sxs-lookup"><span data-stu-id="da17d-120">Specify the path to the transform file.</span></span> <span data-ttu-id="da17d-121">Se o caminho para o arquivo de transformação for omitido, os dois bancos de dados serão comparados apenas.</span><span class="sxs-lookup"><span data-stu-id="da17d-121">If the path to the transform file is omitted, the two databases are only compared.</span></span> <span data-ttu-id="da17d-122">O terceiro argumento é um valor numérico opcional que especifica um conjunto de condições de erro que devem ser suprimidas.</span><span class="sxs-lookup"><span data-stu-id="da17d-122">The third argument is an optional numeric value that specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="da17d-123">Adicione esses valores juntos para suprimir várias condições.</span><span class="sxs-lookup"><span data-stu-id="da17d-123">Add these values together to suppress multiple conditions.</span></span>



| <span data-ttu-id="da17d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="da17d-124">Value</span></span> | <span data-ttu-id="da17d-125">Condição de erro para suprimir</span><span class="sxs-lookup"><span data-stu-id="da17d-125">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="da17d-126">1</span><span class="sxs-lookup"><span data-stu-id="da17d-126">1</span></span>     | <span data-ttu-id="da17d-127">Adicionando uma linha que já existe.</span><span class="sxs-lookup"><span data-stu-id="da17d-127">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="da17d-128">2</span><span class="sxs-lookup"><span data-stu-id="da17d-128">2</span></span>     | <span data-ttu-id="da17d-129">Excluindo uma linha que não existe.</span><span class="sxs-lookup"><span data-stu-id="da17d-129">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="da17d-130">4</span><span class="sxs-lookup"><span data-stu-id="da17d-130">4</span></span>     | <span data-ttu-id="da17d-131">Adicionando uma tabela que já existe.</span><span class="sxs-lookup"><span data-stu-id="da17d-131">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="da17d-132">8</span><span class="sxs-lookup"><span data-stu-id="da17d-132">8</span></span>     | <span data-ttu-id="da17d-133">Excluindo uma tabela que não existe.</span><span class="sxs-lookup"><span data-stu-id="da17d-133">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="da17d-134">16</span><span class="sxs-lookup"><span data-stu-id="da17d-134">16</span></span>    | <span data-ttu-id="da17d-135">Atualizando uma linha que não existe.</span><span class="sxs-lookup"><span data-stu-id="da17d-135">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="da17d-136">256</span><span class="sxs-lookup"><span data-stu-id="da17d-136">256</span></span>   | <span data-ttu-id="da17d-137">Incompatibilidade de páginas de código de banco de dados e transformação.</span><span class="sxs-lookup"><span data-stu-id="da17d-137">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="da17d-138">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="da17d-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="da17d-139">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="da17d-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



