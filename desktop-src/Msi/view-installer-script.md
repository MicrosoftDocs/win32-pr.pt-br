---
description: O arquivo VBScript WiLstScr.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo de script demonstra o Windows Installer Visualizador de script.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Exibir o script do instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778551"
---
# <a name="view-installer-script"></a><span data-ttu-id="b62ff-104">Exibir o script do instalador</span><span class="sxs-lookup"><span data-stu-id="b62ff-104">View Installer Script</span></span>

<span data-ttu-id="b62ff-105">O arquivo VBScript WiLstScr.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="b62ff-105">The VBScript file WiLstScr.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="b62ff-106">Este exemplo de script demonstra o Windows Installer Visualizador de script.</span><span class="sxs-lookup"><span data-stu-id="b62ff-106">This sample script demonstrates the Windows Installer script viewer.</span></span>

<span data-ttu-id="b62ff-107">O exemplo demonstra o uso de:</span><span class="sxs-lookup"><span data-stu-id="b62ff-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="b62ff-108">**Método OpenDatabase (objeto instalador)**</span><span class="sxs-lookup"><span data-stu-id="b62ff-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="b62ff-109">Método [**LastErrorRecord**](installer-lasterrorrecord.md) do objeto do [**instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="b62ff-109">[**LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer**](installer-object.md) object</span></span>
-   <span data-ttu-id="b62ff-110">Método [**OpenView**](database-openview.md) do objeto [**Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="b62ff-110">[**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object</span></span>
-   <span data-ttu-id="b62ff-111">Método [**Fetch**](view-fetch.md) do objeto [**View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="b62ff-111">[**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object</span></span>
-   <span data-ttu-id="b62ff-112">Método [**FormatText**](record-formattext.md)</span><span class="sxs-lookup"><span data-stu-id="b62ff-112">[**FormatText**](record-formattext.md) method</span></span>
-   <span data-ttu-id="b62ff-113">Propriedade [**FieldCount**](record-fieldcount.md)</span><span class="sxs-lookup"><span data-stu-id="b62ff-113">[**FieldCount**](record-fieldcount.md) property</span></span>
-   <span data-ttu-id="b62ff-114">Propriedade [**StringData**](record-stringdata.md) do objeto [**Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="b62ff-114">[**StringData**](record-stringdata.md) property of the [**Record**](record-object.md) object</span></span>
-   [<span data-ttu-id="b62ff-115">\_Tabela de transformview</span><span class="sxs-lookup"><span data-stu-id="b62ff-115">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="b62ff-116">O uso deste exemplo requer a versão CScript.exe do Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="b62ff-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="b62ff-117">Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="b62ff-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="b62ff-118">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="b62ff-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="b62ff-119">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="b62ff-119">or if too few arguments are specified.</span></span> <span data-ttu-id="b62ff-120">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="b62ff-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="b62ff-121">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="b62ff-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="b62ff-122">**cscript WiLstScr.vbs** *\[ caminho para Windows Installer \] script de execução*</span><span class="sxs-lookup"><span data-stu-id="b62ff-122">**cscript WiLstScr.vbs** *\[path to Windows Installer execution script\]*</span></span>

<span data-ttu-id="b62ff-123">Especifique o caminho para o script de execução do instalador.</span><span class="sxs-lookup"><span data-stu-id="b62ff-123">Specify the path to the installer execution script.</span></span>

<span data-ttu-id="b62ff-124">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="b62ff-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="b62ff-125">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b62ff-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



