---
description: O arquivo VBScript WiToAnsi.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo mostra como o script é usado para reescrever um arquivo de texto Unicode como um arquivo de texto ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Copiar um arquivo Unicode para um arquivo ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828876"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a><span data-ttu-id="71e1c-104">Copiar um arquivo Unicode para um arquivo ANSI</span><span class="sxs-lookup"><span data-stu-id="71e1c-104">Copy a Unicode File to an ANSI File</span></span>

<span data-ttu-id="71e1c-105">O arquivo VBScript WiToAnsi.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="71e1c-105">The VBScript file WiToAnsi.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="71e1c-106">Este exemplo mostra como o script é usado para reescrever um arquivo de texto Unicode como um arquivo de texto ANSI.</span><span class="sxs-lookup"><span data-stu-id="71e1c-106">This sample shows how script is used to rewrite a Unicode text file as an ANSI text file.</span></span>

<span data-ttu-id="71e1c-107">O uso deste exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="71e1c-107">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="71e1c-108">Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="71e1c-108">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="71e1c-109">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="71e1c-109">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="71e1c-110">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="71e1c-110">or if too few arguments are specified.</span></span> <span data-ttu-id="71e1c-111">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="71e1c-111">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="71e1c-112">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="71e1c-112">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="71e1c-113">**cscript WiToAnsi.vbs \[ caminho para o caminho do arquivo Unicode \] \[ para o arquivo ANSI\]**</span><span class="sxs-lookup"><span data-stu-id="71e1c-113">**cscript WiToAnsi.vbs \[path to Unicode file\]\[path to ANSI file\]**</span></span>

<span data-ttu-id="71e1c-114">Especifique o arquivo de texto Unicode que está sendo convertido.</span><span class="sxs-lookup"><span data-stu-id="71e1c-114">Specify the Unicode text file that is being converted.</span></span> <span data-ttu-id="71e1c-115">Especifique o arquivo de texto ANSI que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="71e1c-115">Specify the ANSI text file that is being created.</span></span> <span data-ttu-id="71e1c-116">Se nenhum arquivo ANSI for especificado, o arquivo Unicode será substituído.</span><span class="sxs-lookup"><span data-stu-id="71e1c-116">If no ANSI file is specified, the Unicode file is replaced.</span></span>

<span data-ttu-id="71e1c-117">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="71e1c-117">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="71e1c-118">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="71e1c-118">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



