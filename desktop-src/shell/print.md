---
description: A API do Shell fornece funções que você pode usar para gerenciar impressoras em rede. Se um arquivo tiver o verbo de impressão associado a ele, você poderá usar o comando ShellExecuteEx para imprimi-lo.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Gerenciando impressoras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968001"
---
# <a name="managing-printers"></a><span data-ttu-id="81bda-104">Gerenciando impressoras</span><span class="sxs-lookup"><span data-stu-id="81bda-104">Managing Printers</span></span>

<span data-ttu-id="81bda-105">A API do Shell fornece funções que você pode usar para gerenciar impressoras em rede.</span><span class="sxs-lookup"><span data-stu-id="81bda-105">The Shell API provides functions that you can use to manage networked printers.</span></span> <span data-ttu-id="81bda-106">Se um arquivo tiver o verbo de **impressão** associado a ele, você poderá usar o comando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para imprimi-lo.</span><span class="sxs-lookup"><span data-stu-id="81bda-106">If a file has the **print** verb associated with it, you can use the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) command to print it.</span></span>

-   [<span data-ttu-id="81bda-107">Gerenciamento de impressora</span><span class="sxs-lookup"><span data-stu-id="81bda-107">Printer Management</span></span>](#printer-management)
-   [<span data-ttu-id="81bda-108">Imprimindo arquivos com ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="81bda-108">Printing Files with ShellExecuteEx</span></span>](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a><span data-ttu-id="81bda-109">Gerenciamento de impressora</span><span class="sxs-lookup"><span data-stu-id="81bda-109">Printer Management</span></span>

<span data-ttu-id="81bda-110">Você pode gerenciar impressoras em um sistema com a função [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) .</span><span class="sxs-lookup"><span data-stu-id="81bda-110">You can manage printers on a system with the [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) function.</span></span> <span data-ttu-id="81bda-111">Essa função permite que você:</span><span class="sxs-lookup"><span data-stu-id="81bda-111">This function allows you to:</span></span>

-   <span data-ttu-id="81bda-112">Instalar impressoras.</span><span class="sxs-lookup"><span data-stu-id="81bda-112">Install printers.</span></span>
-   <span data-ttu-id="81bda-113">Abra Impressoras.</span><span class="sxs-lookup"><span data-stu-id="81bda-113">Open printers.</span></span>
-   <span data-ttu-id="81bda-114">Obter propriedades da impressora.</span><span class="sxs-lookup"><span data-stu-id="81bda-114">Get printer properties.</span></span>
-   <span data-ttu-id="81bda-115">Crie links de impressora.</span><span class="sxs-lookup"><span data-stu-id="81bda-115">Create printer links.</span></span>
-   <span data-ttu-id="81bda-116">Imprima uma página de teste.</span><span class="sxs-lookup"><span data-stu-id="81bda-116">Print a test page.</span></span>

## <a name="printing-files-with-shellexecuteex"></a><span data-ttu-id="81bda-117">Imprimindo arquivos com ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="81bda-117">Printing Files with ShellExecuteEx</span></span>

<span data-ttu-id="81bda-118">Se um tipo de arquivo tiver um comando de impressão associado a ele, você poderá imprimir o arquivo chamando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) com **Print** como o verbo.</span><span class="sxs-lookup"><span data-stu-id="81bda-118">If a file type has a print command associated with it, you can print the file by calling [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) with **print** as the verb.</span></span> <span data-ttu-id="81bda-119">Esse comando é geralmente o mesmo usado para o verbo **Open** , com a adição de um sinalizador para dizer ao aplicativo para imprimir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="81bda-119">This command is often the same as that used for the **open** verb, with the addition of a flag to tell the application to print the file.</span></span> <span data-ttu-id="81bda-120">Por exemplo, os arquivos. txt podem ser impressos pelo Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="81bda-120">For instance, .txt files can be printed by Microsoft WordPad.</span></span> <span data-ttu-id="81bda-121">O verbo **Open** para um arquivo. txt, portanto, corresponderia a algo como o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="81bda-121">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



<span data-ttu-id="81bda-122">Quando você usa [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para imprimir um arquivo. txt, o WordPad abre o arquivo, o imprime e, em seguida, fecha, retornando o controle para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81bda-122">When you use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to print a .txt file, WordPad opens the file, prints it, and then closes, returning control to the application.</span></span> <span data-ttu-id="81bda-123">A função de exemplo a seguir usa um caminho totalmente qualificado e usa **ShellExecuteEx** para imprimi-lo, usando o comando Print associado à sua extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="81bda-123">The following sample function takes a fully qualified path, and uses **ShellExecuteEx** to print it, using the print command associated with its file name extension.</span></span>


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



