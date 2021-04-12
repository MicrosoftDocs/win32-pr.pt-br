---
description: O arquivo VBScript WiSubStg.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Gerenciar subarmazenamentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297444"
---
# <a name="manage-substorages"></a><span data-ttu-id="e5218-103">Gerenciar subarmazenamentos</span><span class="sxs-lookup"><span data-stu-id="e5218-103">Manage Substorages</span></span>

<span data-ttu-id="e5218-104">O arquivo VBScript WiSubStg.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="e5218-104">The VBScript file WiSubStg.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="e5218-105">Este exemplo mostra como o script pode ser usado para gerenciar subarmazenamentos em um banco de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e5218-105">This sample shows how script can be used to manage substorages in a Windows Installer database.</span></span> <span data-ttu-id="e5218-106">Uma transformação pode ser adicionada a um banco de dados Windows Installer existente como um subarmazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5218-106">A transform can be added to an existing Windows Installer database as a substorage.</span></span>

<span data-ttu-id="e5218-107">O exemplo demonstra o uso de:</span><span class="sxs-lookup"><span data-stu-id="e5218-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="e5218-108">\_Tabela de armazenamentos</span><span class="sxs-lookup"><span data-stu-id="e5218-108">\_Storages table</span></span>](-storages-table.md)
-   [<span data-ttu-id="e5218-109">**Método OpenDatabase (objeto instalador)**</span><span class="sxs-lookup"><span data-stu-id="e5218-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="e5218-110">**Método CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="e5218-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="e5218-111">[**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="e5218-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="e5218-112">**Método OpenView**</span><span class="sxs-lookup"><span data-stu-id="e5218-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="e5218-113">[**Método Commit**](database-commit.md) do [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="e5218-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="e5218-114">**Método Fetch**</span><span class="sxs-lookup"><span data-stu-id="e5218-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="e5218-115">**Modificar método**</span><span class="sxs-lookup"><span data-stu-id="e5218-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="e5218-116">[**Método execute**](view-execute.md) do [ **objeto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="e5218-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="e5218-117">**Propriedade StringData**</span><span class="sxs-lookup"><span data-stu-id="e5218-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="e5218-118">[**Método SetStream**](record-setstream.md) do [ **objeto Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="e5218-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="e5218-119">Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="e5218-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="e5218-120">Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="e5218-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="e5218-121">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="e5218-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="e5218-122">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="e5218-122">or if too few arguments are specified.</span></span> <span data-ttu-id="e5218-123">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="e5218-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="e5218-124">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="e5218-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="e5218-125">**cscript WiSubStg.vbs \[ caminho para o caminho do banco \] \[ de dados para opções de arquivo \] \[ \] \[ nome do subarmazenamento\]**</span><span class="sxs-lookup"><span data-stu-id="e5218-125">**cscript WiSubStg.vbs \[path to database\]\[path to file\]\[options\]\[substorage name\]**</span></span>

<span data-ttu-id="e5218-126">Especifique o caminho para o banco de dados de Windows Installer para adicionar ou remover o subarmazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5218-126">Specify the path to the Windows Installer database to add or remove substorage.</span></span> <span data-ttu-id="e5218-127">Especifique um caminho para a transformação ou o arquivo de banco de dados que está sendo adicionado como subarmazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5218-127">Specify a path to the transform or database file that is being added as substorage.</span></span> <span data-ttu-id="e5218-128">Para listar os subarmazenamentos no banco de dados Windows Installer, omita o caminho para esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="e5218-128">To list the substorages in the Windows Installer database, omit the path to this file.</span></span> <span data-ttu-id="e5218-129">Você pode especificar um nome de subarmazenamento opcional, se for omitido, o nome do subarmazenamento padrão será o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e5218-129">You may specify an optional substorage name, if this is omitted the substorage name defaults to the file name.</span></span>

<span data-ttu-id="e5218-130">A opção a seguir pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="e5218-130">The following option may be specified.</span></span>



| <span data-ttu-id="e5218-131">Opção</span><span class="sxs-lookup"><span data-stu-id="e5218-131">Option</span></span>              | <span data-ttu-id="e5218-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5218-132">Description</span></span>                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5218-133">nenhuma opção especificada</span><span class="sxs-lookup"><span data-stu-id="e5218-133">no option specified</span></span> | <span data-ttu-id="e5218-134">Adicione um subarmazenamento ao banco de dados de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e5218-134">Add a substorage to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="e5218-135">/d</span><span class="sxs-lookup"><span data-stu-id="e5218-135">/d</span></span>                  | <span data-ttu-id="e5218-136">Remova um subarmazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5218-136">Remove a substorage.</span></span> <span data-ttu-id="e5218-137">Esse sinalizador de opção deve ser seguido pelo nome do subarmazenamento a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e5218-137">This option flag must be followed by the name of the substorage to be removed.</span></span> |



 

<span data-ttu-id="e5218-138">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="e5218-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="e5218-139">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e5218-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="e5218-140">Observe que [um exemplo de localização demonstra a](a-localization-example.md) [inserção de transformações de personalização como um subarmazenamento](embedding-customization-transforms-as-substorage.md).</span><span class="sxs-lookup"><span data-stu-id="e5218-140">Note that [A Localization Example](a-localization-example.md) demonstrates [Embedding Customization Transforms as Substorage](embedding-customization-transforms-as-substorage.md).</span></span>

 

 



