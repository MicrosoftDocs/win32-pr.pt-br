---
description: O arquivo VBScript WiFilVer.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. O exemplo mostra como você pode usar um script para relatar ou atualizar a versão do arquivo, o tamanho e as informações de idioma.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Gerenciar tamanhos e versões de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647468"
---
# <a name="manage-file-sizes-and-versions"></a><span data-ttu-id="73081-104">Gerenciar tamanhos e versões de arquivo</span><span class="sxs-lookup"><span data-stu-id="73081-104">Manage File Sizes and Versions</span></span>

<span data-ttu-id="73081-105">O arquivo VBScript WiFilVer.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="73081-105">The VBScript file WiFilVer.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="73081-106">O exemplo mostra como você pode usar um script para relatar ou atualizar a versão do arquivo, o tamanho e as informações de idioma.</span><span class="sxs-lookup"><span data-stu-id="73081-106">The sample shows you how you can use a script to report or update the file version, size, and language information.</span></span>

<span data-ttu-id="73081-107">O exemplo também mostra Windows Installer ações, como acessar um banco de dados do Windows Installer e o uso do seguinte:</span><span class="sxs-lookup"><span data-stu-id="73081-107">The sample also shows you Windows Installer actions, how to access a Windows Installer database, and the use of the following:</span></span>

-   <span data-ttu-id="73081-108">Método [**Installer. OpenDatabase**](installer-opendatabase.md) do [ **objeto instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="73081-108">[**Installer.OpenDatabase**](installer-opendatabase.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="73081-109">Propriedade [**Installer. FileAttributes**](installer-fileattributes.md)</span><span class="sxs-lookup"><span data-stu-id="73081-109">[**Installer.FileAttributes**](installer-fileattributes.md) property</span></span>
-   <span data-ttu-id="73081-110">Método [**Installer. FileHash**](installer-filehash.md)</span><span class="sxs-lookup"><span data-stu-id="73081-110">[**Installer.FileHash**](installer-filehash.md) method</span></span>
-   <span data-ttu-id="73081-111">Método [**Installer. FileVersion**](installer-fileversion.md)</span><span class="sxs-lookup"><span data-stu-id="73081-111">[**Installer.FileVersion**](installer-fileversion.md) method</span></span>
-   <span data-ttu-id="73081-112">Método [**Installer. LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="73081-112">[**Installer.LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="73081-113">Método [**Database. OpenView**](database-openview.md)</span><span class="sxs-lookup"><span data-stu-id="73081-113">[**Database.OpenView**](database-openview.md) method</span></span>
-   <span data-ttu-id="73081-114">Propriedade [**Database. SummaryInformation**](database-summaryinformation.md) do [ **objeto de banco de dados**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="73081-114">[**Database.SummaryInformation**](database-summaryinformation.md) property of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="73081-115">Método [**Session. DoAction**](session-doaction.md)</span><span class="sxs-lookup"><span data-stu-id="73081-115">[**Session.DoAction**](session-doaction.md) method</span></span>
-   [<span data-ttu-id="73081-116">**Sessão. Propriedade**</span><span class="sxs-lookup"><span data-stu-id="73081-116">**Session.Property**</span></span>](session-session.md)
-   <span data-ttu-id="73081-117">Propriedade [**Session. SourcePath**](session-sourcepath.md)</span><span class="sxs-lookup"><span data-stu-id="73081-117">[**Session.SourcePath**](session-sourcepath.md) property</span></span>
-   <span data-ttu-id="73081-118">Propriedade [**Session. Mode**](session-mode.md) do [ **objeto Session**](session-object.md)</span><span class="sxs-lookup"><span data-stu-id="73081-118">[**Session.Mode**](session-mode.md) property of the [**Session Object**](session-object.md)</span></span>
-   <span data-ttu-id="73081-119">Propriedade [**Record. StringData**](record-stringdata.md)</span><span class="sxs-lookup"><span data-stu-id="73081-119">[**Record.StringData**](record-stringdata.md) property</span></span>
-   <span data-ttu-id="73081-120">Propriedade [**Record. IntegerData**](record-integerdata.md) do [ **objeto Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="73081-120">[**Record.IntegerData**](record-integerdata.md) property of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="73081-121">O uso deste exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="73081-121">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="73081-122">Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="73081-122">To use CScript.exe to run this sample, type a command at the command prompt by using the following syntax:</span></span>

<span data-ttu-id="73081-123">**cscript WiFilVer.vbs \[ caminho para os \] \[ locais de origem opcionais do banco de dados\]**</span><span class="sxs-lookup"><span data-stu-id="73081-123">**cscript WiFilVer.vbs \[path to database\]\[optional source locations\]**</span></span>

<span data-ttu-id="73081-124">Lembre-se também do seguinte:</span><span class="sxs-lookup"><span data-stu-id="73081-124">Also be aware of the following:</span></span>

-   <span data-ttu-id="73081-125">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="73081-125">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="73081-126">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="73081-126">or if too few arguments are specified.</span></span>
-   <span data-ttu-id="73081-127">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="73081-127">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span>
-   <span data-ttu-id="73081-128">O exemplo retorna um valor de 0 (zero) para êxito, 1 (um) se a ajuda for invocada e 2 (dois) se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="73081-128">The sample returns a value of 0 (zero) for success, 1 (one) if help is invoked, and 2 (two) if the script fails.</span></span>

<span data-ttu-id="73081-129">Especifique o banco de dados Windows Installer que você deseja atualizar, que deve estar localizado na raiz do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="73081-129">Specify the Windows Installer database that you want to be updated, which must be located at the source file root.</span></span> <span data-ttu-id="73081-130">No entanto, você pode especificar fontes para o banco de dados em locais separados.</span><span class="sxs-lookup"><span data-stu-id="73081-130">However, you can specify sources for the database at separate locations.</span></span> <span data-ttu-id="73081-131">Se a origem for compactada, todos os arquivos serão abertos na raiz.</span><span class="sxs-lookup"><span data-stu-id="73081-131">If the source is compressed, all the files are opened at the root.</span></span>

<span data-ttu-id="73081-132">As opções a seguir podem ser especificadas em qualquer local na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="73081-132">The following options can be specified at any location on the command line.</span></span>



| <span data-ttu-id="73081-133">Opção</span><span class="sxs-lookup"><span data-stu-id="73081-133">Option</span></span>                | <span data-ttu-id="73081-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="73081-134">Description</span></span>                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73081-135">*nenhuma opção especificada*</span><span class="sxs-lookup"><span data-stu-id="73081-135">*no option specified*</span></span> | <span data-ttu-id="73081-136">Exibir as informações de arquivo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="73081-136">Display the file information of the database.</span></span>                                            |
| <span data-ttu-id="73081-137">/u</span><span class="sxs-lookup"><span data-stu-id="73081-137">/u</span></span>                    | <span data-ttu-id="73081-138">Atualize o tamanho do arquivo, a versão e as informações de idioma no banco de dados da origem.</span><span class="sxs-lookup"><span data-stu-id="73081-138">Update the file size, version, and language information in the database from the source.</span></span> |



 

<span data-ttu-id="73081-139">Para obter mais informações, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md) e [ferramentas de desenvolvimento de Windows Installer](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="73081-139">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) and [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



