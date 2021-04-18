---
description: O arquivo VBScript WiStream.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Gerenciar fluxos binários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785430"
---
# <a name="manage-binary-streams"></a><span data-ttu-id="a98bf-103">Gerenciar fluxos binários</span><span class="sxs-lookup"><span data-stu-id="a98bf-103">Manage Binary Streams</span></span>

<span data-ttu-id="a98bf-104">O arquivo VBScript WiStream.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="a98bf-104">The VBScript file WiStream.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="a98bf-105">Este exemplo mostra como o script pode ser usado para gerenciar fluxos binários em um banco de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a98bf-105">This sample shows how script can be used to manage binary streams in a Windows Installer database.</span></span> <span data-ttu-id="a98bf-106">O exemplo pode ser usado para inserir gabinetes de arquivo compactados em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a98bf-106">The sample may be used to enter compressed file cabinets into a database.</span></span> <span data-ttu-id="a98bf-107">Este exemplo demonstra a operação da [ \_ tabela de fluxos](-streams-table.md) no banco de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a98bf-107">This sample demonstrates the operation of the [\_Streams table](-streams-table.md) in the Windows Installer database.</span></span>

<span data-ttu-id="a98bf-108">O exemplo também demonstra o uso de:</span><span class="sxs-lookup"><span data-stu-id="a98bf-108">The sample also demonstrates the use of:</span></span>

-   [<span data-ttu-id="a98bf-109">**Método OpenDatabase (objeto instalador)**</span><span class="sxs-lookup"><span data-stu-id="a98bf-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="a98bf-110">**Método CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="a98bf-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="a98bf-111">[**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="a98bf-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="a98bf-112">**Método OpenView**</span><span class="sxs-lookup"><span data-stu-id="a98bf-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="a98bf-113">[**Método Commit**](database-commit.md) do [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="a98bf-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="a98bf-114">**Método Fetch**</span><span class="sxs-lookup"><span data-stu-id="a98bf-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="a98bf-115">**Modificar método**</span><span class="sxs-lookup"><span data-stu-id="a98bf-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="a98bf-116">[**Método execute**](view-execute.md) do [ **objeto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="a98bf-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="a98bf-117">**Propriedade StringData**</span><span class="sxs-lookup"><span data-stu-id="a98bf-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="a98bf-118">[**Método SetStream**](record-setstream.md) do [ **objeto Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="a98bf-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="a98bf-119">Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="a98bf-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="a98bf-120">Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="a98bf-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="a98bf-121">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="a98bf-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="a98bf-122">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="a98bf-122">or if too few arguments are specified.</span></span> <span data-ttu-id="a98bf-123">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="a98bf-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="a98bf-124">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="a98bf-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="a98bf-125">**cscript WiStream.vbs \[ caminho para o caminho do banco \] \[ de dados para opções de arquivo \] \[ \] \[ nome do fluxo\]**</span><span class="sxs-lookup"><span data-stu-id="a98bf-125">**cscript WiStream.vbs \[path to database\]\[path to file\]\[options\]\[stream name\]**</span></span>

<span data-ttu-id="a98bf-126">Especifique o caminho para o banco de dados de Windows Installer que deve receber o fluxo.</span><span class="sxs-lookup"><span data-stu-id="a98bf-126">Specify the path to the Windows Installer database that is to receive the stream.</span></span> <span data-ttu-id="a98bf-127">Especifique um caminho para o arquivo binário que contém os dados do fluxo.</span><span class="sxs-lookup"><span data-stu-id="a98bf-127">Specify a path to the binary file containing the stream data.</span></span> <span data-ttu-id="a98bf-128">Para listar os fluxos no banco de dados do instalador, omita este caminho.</span><span class="sxs-lookup"><span data-stu-id="a98bf-128">To list the streams in the installer database, omit this path.</span></span> <span data-ttu-id="a98bf-129">Você pode especificar um nome de fluxo opcional, se isso for omitido, o padrão será o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a98bf-129">You may specify an optional stream name, if this is omitted it defaults to the file name.</span></span>

<span data-ttu-id="a98bf-130">A opção a seguir pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="a98bf-130">The following option may be specified.</span></span>



| <span data-ttu-id="a98bf-131">Opção</span><span class="sxs-lookup"><span data-stu-id="a98bf-131">Option</span></span>              | <span data-ttu-id="a98bf-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="a98bf-132">Description</span></span>                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a98bf-133">nenhuma opção especificada</span><span class="sxs-lookup"><span data-stu-id="a98bf-133">no option specified</span></span> | <span data-ttu-id="a98bf-134">Adicione um fluxo ao banco de dados de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a98bf-134">Add a stream to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="a98bf-135">/d</span><span class="sxs-lookup"><span data-stu-id="a98bf-135">/d</span></span>                  | <span data-ttu-id="a98bf-136">Remover um fluxo.</span><span class="sxs-lookup"><span data-stu-id="a98bf-136">Remove a stream.</span></span> <span data-ttu-id="a98bf-137">Esse sinalizador de opção deve ser seguido pelo nome do subarmazenamento que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="a98bf-137">This option flag must be followed by the name of the substorage being removed.</span></span> |



 

<span data-ttu-id="a98bf-138">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="a98bf-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="a98bf-139">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a98bf-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



