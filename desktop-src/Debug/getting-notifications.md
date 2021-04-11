---
description: O código a seguir mostra como obter e relatar informações de status detalhadas do manipulador de símbolos sobre a pesquisa e o carregamento de módulos e os arquivos de símbolo correspondentes.
ms.assetid: 1dd8af0e-280b-4fc4-bf75-45c5c7517365
title: Obtendo notificações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bebaed2683f329fa267bdc926063d0b763190400
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164165"
---
# <a name="getting-notifications"></a><span data-ttu-id="26d0e-103">Obtendo notificações</span><span class="sxs-lookup"><span data-stu-id="26d0e-103">Getting Notifications</span></span>

<span data-ttu-id="26d0e-104">O código a seguir mostra como obter e relatar informações de status detalhadas do manipulador de símbolos sobre a pesquisa e o carregamento de módulos e os arquivos de símbolo correspondentes.</span><span class="sxs-lookup"><span data-stu-id="26d0e-104">The following code shows how to obtain and report verbose status information from the symbol handler about searching for and loading of modules and the corresponding symbol files.</span></span>

<span data-ttu-id="26d0e-105">Muitos familiarizados com o depurador do WinDbg podem se lembrar de um comando chamado "! Sym ruidosa".</span><span class="sxs-lookup"><span data-stu-id="26d0e-105">Many familiar with the WinDbg debugger may remember a command called "!sym noisy".</span></span> <span data-ttu-id="26d0e-106">Esse comando é usado pelo usuário para determinar por que o WinDbg é ou não é capaz de carregar arquivos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="26d0e-106">This command is used by the user to determine why WinDbg is or is not able to load symbol files.</span></span> <span data-ttu-id="26d0e-107">Ele mostra uma listagem detalhada de tudo o que o manipulador de símbolo tenta.</span><span class="sxs-lookup"><span data-stu-id="26d0e-107">It shows a verbose listing of everything the symbol handler tries.</span></span>

<span data-ttu-id="26d0e-108">Essa mesma listagem também está disponível para qualquer pessoa que estiver desenvolvendo um cliente para o manipulador de símbolos DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="26d0e-108">This same listing is also available to anyone developing a client to the DbgHelp symbol handler.</span></span>

<span data-ttu-id="26d0e-109">Primeiro, chame [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) com **SYMOPT \_ debug**.</span><span class="sxs-lookup"><span data-stu-id="26d0e-109">First, call [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) with **SYMOPT\_DEBUG**.</span></span> <span data-ttu-id="26d0e-110">Isso faz com que o DbgHelp ative as notificações de depuração.</span><span class="sxs-lookup"><span data-stu-id="26d0e-110">This causes DbgHelp to turn on debug notifications.</span></span>

<span data-ttu-id="26d0e-111">Depois de chamar [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), use [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) para registrar uma função de retorno de chamada que dbghelp chamará sempre que ocorrer um evento interessante.</span><span class="sxs-lookup"><span data-stu-id="26d0e-111">After calling [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), use [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) to register a callback function that DbgHelp will call whenever an interesting event occurs.</span></span> <span data-ttu-id="26d0e-112">Neste exemplo, a função de retorno de chamada é chamada [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback).</span><span class="sxs-lookup"><span data-stu-id="26d0e-112">In this example, the callback function is called [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback).</span></span> <span data-ttu-id="26d0e-113">As funções de retorno de chamada de símbolo são passadas por uma variedade de códigos de ação que podem ser tratados de acordo com o tipo.</span><span class="sxs-lookup"><span data-stu-id="26d0e-113">Symbol callback functions are passed an assortment of action codes that they can handle according to type.</span></span> <span data-ttu-id="26d0e-114">Neste exemplo, estamos manipulando apenas o código de ação do **\_ evento CBA** .</span><span class="sxs-lookup"><span data-stu-id="26d0e-114">In this example, we are handling only the **CBA\_EVENT** action code.</span></span> <span data-ttu-id="26d0e-115">Essa função passa uma cadeia de caracteres contendo informações detalhadas sobre um evento que ocorreu no processo de carregamento de um símbolo.</span><span class="sxs-lookup"><span data-stu-id="26d0e-115">This function passes a string containing verbose information about an event that occurred in the process of loading a symbol.</span></span> <span data-ttu-id="26d0e-116">Esse evento pode ser qualquer coisa, desde uma tentativa de ler os dados em uma imagem executável até o local bem-sucedido de um arquivo de símbolo.</span><span class="sxs-lookup"><span data-stu-id="26d0e-116">This event could be anything from an attempt to read the data within an executable image to the successful location of a symbol file.</span></span> <span data-ttu-id="26d0e-117">**SymRegisterCallbackProc64** exibe essa cadeia de caracteres e retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="26d0e-117">**SymRegisterCallbackProc64** displays that string and returns **TRUE**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26d0e-118">Certifique-se de retornar **false** para todos os códigos de ação que você não tratar, caso contrário, você poderá experimentar um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="26d0e-118">Make sure you return **FALSE** to every action code that you do not handle, otherwise you may experience undefined behavior.</span></span> <span data-ttu-id="26d0e-119">Consulte [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) para obter uma lista de todos os códigos de ação e suas implicações.</span><span class="sxs-lookup"><span data-stu-id="26d0e-119">Refer to [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) for a list of all the action codes and their implications.</span></span>

 

<span data-ttu-id="26d0e-120">Agora que o retorno de chamada está registrado, é hora de carregar o módulo especificado na linha de comando chamando [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex).</span><span class="sxs-lookup"><span data-stu-id="26d0e-120">Now that the callback is registered, it is time to load the module specified on the command line by calling [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex).</span></span>

<span data-ttu-id="26d0e-121">Por fim, chame [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) antes de sair.</span><span class="sxs-lookup"><span data-stu-id="26d0e-121">Lastly, call [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) before exiting.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#ifdef UNICODE
 #define DBGHELP_TRANSLATE_TCHAR
#endif
#include <dbghelp.h>

// Here is an implementation of a Symbol Callback function.

BOOL 
CALLBACK 
SymRegisterCallbackProc64(
    __in HANDLE hProcess,
    __in ULONG ActionCode,
    __in_opt ULONG64 CallbackData,
    __in_opt ULONG64 UserContext
    )
{
    UNREFERENCED_PARAMETER(hProcess);
    UNREFERENCED_PARAMETER(UserContext);
    
    PIMAGEHLP_CBA_EVENT evt;

    // If SYMOPT_DEBUG is set, then the symbol handler will pass
    // verbose information on its attempt to load symbols.
    // This information be delivered as text strings.
    
    switch (ActionCode)
    {
    case CBA_EVENT:
        evt = (PIMAGEHLP_CBA_EVENT)CallbackData;
        _tprintf(_T("%s"), (PTSTR)evt->desc);
        break;

    // CBA_DEBUG_INFO is the old ActionCode for symbol spew.
    // It still works, but we use CBA_EVENT in this example.
#if 0
    case CBA_DEBUG_INFO:
        _tprintf(_T("%s"), (PTSTR)CallbackData);
        break;
#endif

    default:
        // Return false to any ActionCode we don't handle
        // or we could generate some undesirable behavior.
        return FALSE;
    }

    return TRUE;
}

// Main code.

int __cdecl
#ifdef UNICODE
_tmain(
#else
main(
#endif
    __in int argc,
    __in_ecount(argc) PCTSTR argv[]
    )
{
    BOOL status;
    int rc = -1;
    HANDLE hProcess;
    DWORD64 module;
    
    if (argc < 2)
    {
        _tprintf(_T("You must specify an executable image to load.\n"));
        return rc;
    }

    // If we want to se debug spew, we need to set this option.
        
    SymSetOptions(SYMOPT_DEBUG);
    
    // We are not debugging an actual process, so lets use a placeholder
    // value of 1 for hProcess just to ID these calls from any other
    // series we may want to load.  For this simple case, anything will do.
    
    hProcess = (HANDLE)1;
    
    // Initialize the symbol handler.  No symbol path.  
    // Just let dbghelp use _NT_SYMBOL_PATH
    
    status = SymInitialize(hProcess, NULL, false);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymInitialize.\n"), GetLastError());
        return rc;
    }
     
    // Now register our callback.
    
    status = SymRegisterCallback64(hProcess, SymRegisterCallbackProc64, NULL);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymRegisterCallback64.\n"), GetLastError());
        goto cleanup;
    }
    
    // Go ahead and load a module for testing.
    
    module = SymLoadModuleEx(hProcess,  // our unique id
                             NULL,      // no open file handle to image
                             argv[1],   // name of image to load
                             NULL,      // no module name - dbghelp will get it
                             0,         // no base address - dbghelp will get it
                             0,         // no module size - dbghelp will get it
                             NULL,      // no special MODLOAD_DATA structure
                             0);        // flags
    if (!module)
    {
        _tprintf(_T("Error 0x%x calling SymLoadModuleEx.\n"), GetLastError());
        goto cleanup;
    }
    rc = 0;
    
cleanup:
    SymCleanup(hProcess);
    
    return rc;    
}
```



<span data-ttu-id="26d0e-122">A especificação de **NULL** como o segundo parâmetro de [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indica que o manipulador de símbolo deve usar o caminho de pesquisa padrão para localizar arquivos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="26d0e-122">Specifying **NULL** as the second parameter of [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indicates that the symbol handler should use the default search path to locate symbol files.</span></span> <span data-ttu-id="26d0e-123">Para obter informações detalhadas sobre como o manipulador de símbolo localiza arquivos de símbolo ou como um aplicativo pode especificar um caminho de pesquisa de símbolo, consulte [caminhos de símbolo](symbol-paths.md).</span><span class="sxs-lookup"><span data-stu-id="26d0e-123">For detailed information on how the symbol handler locates symbol files or how an application can specify a symbol search path, see [Symbol Paths](symbol-paths.md).</span></span>

<span data-ttu-id="26d0e-124">A execução deste programa mostra como o caminho do símbolo é processado.</span><span class="sxs-lookup"><span data-stu-id="26d0e-124">Running this program shows how the symbol path is processed.</span></span> <span data-ttu-id="26d0e-125">Como DbgHelp examina o caminho do símbolo para localizar o arquivo de símbolo, ele chama repetidamente o [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) que, por sua vez, exibe as seguintes cadeias de caracteres que estão sendo passadas pelo dbghelp.</span><span class="sxs-lookup"><span data-stu-id="26d0e-125">As DbgHelp looks through the symbol path to find the symbol file, it repeatedly calls [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) which, in turn, displays the following strings being passed by DbgHelp.</span></span>

``` syntax
d:\load.exe c:\home\dbghelp.dll
DBGHELP: No header for c:\home\dbghelp.dll.  Searching for image on disk
DBGHELP: c:\home\dbghelp.dll - OK
DBGHELP: .\dbghelp.pdb - file not found
DBGHELP: .\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\symbols\dll\dbghelp.pdb - file not found
DBGHELP: d:\nt.binaries.amd64chk\symbols.pri\dbg\dbghelp.pdb - file not found
DBGHELP: dbghelp - private symbols & lines
         dbghelp.pdb
```

 

 



