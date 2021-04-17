---
description: O arquivo VBScript WiLangID.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Gerenciar idioma e página de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789773"
---
# <a name="manage-language-and-codepage"></a><span data-ttu-id="a978d-103">Gerenciar idioma e página de código</span><span class="sxs-lookup"><span data-stu-id="a978d-103">Manage Language and Codepage</span></span>

<span data-ttu-id="a978d-104">O arquivo VBScript WiLangID.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="a978d-104">The VBScript file WiLangID.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="a978d-105">Este exemplo mostra como o script é usado para acessar informações de idioma e página de código de um pacote.</span><span class="sxs-lookup"><span data-stu-id="a978d-105">This sample shows how script is used to access a package's language information and codepage.</span></span> <span data-ttu-id="a978d-106">Para obter mais informações, consulte [localizando um pacote de Windows Installer](localizing-a-windows-installer-package.md) e [tratamento de página de código (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="a978d-106">For more information, see [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md) and [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

<span data-ttu-id="a978d-107">O exemplo demonstra o uso de:</span><span class="sxs-lookup"><span data-stu-id="a978d-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="a978d-108">**Método OpenDatabase (objeto instalador)**</span><span class="sxs-lookup"><span data-stu-id="a978d-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="a978d-109">**Método CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="a978d-109">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="a978d-110">[**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="a978d-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="a978d-111">**Método OpenView**</span><span class="sxs-lookup"><span data-stu-id="a978d-111">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="a978d-112">[**Propriedade SummaryInformation (objeto Database)**](database-summaryinformation.md) do [ **objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="a978d-112">[**SummaryInformation property (Database Object)**](database-summaryinformation.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="a978d-113">O uso deste exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="a978d-113">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="a978d-114">Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="a978d-114">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="a978d-115">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="a978d-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="a978d-116">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="a978d-116">or if too few arguments are specified.</span></span> <span data-ttu-id="a978d-117">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="a978d-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="a978d-118">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="a978d-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="a978d-119">**cscript WiLangID.vbs o \[ valor da \] \[ palavra-chave Path \] to database \[\]**</span><span class="sxs-lookup"><span data-stu-id="a978d-119">**cscript WiLangID.vbs \[path to database\]\[keyword\]\[value\]**</span></span>

<span data-ttu-id="a978d-120">Especifique o caminho para o banco de dados de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a978d-120">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="a978d-121">Para alterar um valor, especifique uma das seguintes palavras-chave seguidas pelo novo valor.</span><span class="sxs-lookup"><span data-stu-id="a978d-121">To change a value specify one of the following keywords followed by the new value.</span></span> <span data-ttu-id="a978d-122">Se nenhum valor for especificado, o exemplo retornará o valor atual.</span><span class="sxs-lookup"><span data-stu-id="a978d-122">If no value is specified the sample returns the current value.</span></span>



| <span data-ttu-id="a978d-123">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="a978d-123">Keyword</span></span>      | <span data-ttu-id="a978d-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="a978d-124">Description</span></span>                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a978d-125">**Pacote**</span><span class="sxs-lookup"><span data-stu-id="a978d-125">**Package**</span></span>  | <span data-ttu-id="a978d-126">As versões de idioma com suporte no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a978d-126">The language versions supported by the database.</span></span> <span data-ttu-id="a978d-127">Para obter informações, consulte Propriedade de [**Resumo do modelo**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="a978d-127">For information, see [**Template Summary**](template-summary.md) property.</span></span>                                                               |
| <span data-ttu-id="a978d-128">**Product**</span><span class="sxs-lookup"><span data-stu-id="a978d-128">**Product**</span></span>  | <span data-ttu-id="a978d-129">Idioma que o instalador deve usar para todas as cadeias de caracteres na interface do usuário que não são criadas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a978d-129">Language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="a978d-130">Para obter informações, consulte Propriedade [**ProductLanguage**](productlanguage.md) .</span><span class="sxs-lookup"><span data-stu-id="a978d-130">For information, see [**ProductLanguage**](productlanguage.md) property.</span></span> |
| <span data-ttu-id="a978d-131">**Codepage**</span><span class="sxs-lookup"><span data-stu-id="a978d-131">**Codepage**</span></span> | <span data-ttu-id="a978d-132">Página de código ANSI única para o pool de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a978d-132">Single ANSI code page for the string pool.</span></span> <span data-ttu-id="a978d-133">Para obter informações, consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="a978d-133">For information, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>                                       |



 

<span data-ttu-id="a978d-134">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="a978d-134">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="a978d-135">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a978d-135">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="a978d-136">Para obter mais informações, consulte [determinando a página de código](determining-an-installation-database-s-code-page.md) de um banco de dados de instalação e [definindo a página de código de um banco de dados](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="a978d-136">For more information, see [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

 

 



