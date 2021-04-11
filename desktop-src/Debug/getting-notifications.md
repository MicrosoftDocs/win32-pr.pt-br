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
# <a name="getting-notifications"></a>Obtendo notificações

O código a seguir mostra como obter e relatar informações de status detalhadas do manipulador de símbolos sobre a pesquisa e o carregamento de módulos e os arquivos de símbolo correspondentes.

Muitos familiarizados com o depurador do WinDbg podem se lembrar de um comando chamado "! Sym ruidosa". Esse comando é usado pelo usuário para determinar por que o WinDbg é ou não é capaz de carregar arquivos de símbolo. Ele mostra uma listagem detalhada de tudo o que o manipulador de símbolo tenta.

Essa mesma listagem também está disponível para qualquer pessoa que estiver desenvolvendo um cliente para o manipulador de símbolos DbgHelp.

Primeiro, chame [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) com **SYMOPT \_ debug**. Isso faz com que o DbgHelp ative as notificações de depuração.

Depois de chamar [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), use [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) para registrar uma função de retorno de chamada que dbghelp chamará sempre que ocorrer um evento interessante. Neste exemplo, a função de retorno de chamada é chamada [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback). As funções de retorno de chamada de símbolo são passadas por uma variedade de códigos de ação que podem ser tratados de acordo com o tipo. Neste exemplo, estamos manipulando apenas o código de ação do **\_ evento CBA** . Essa função passa uma cadeia de caracteres contendo informações detalhadas sobre um evento que ocorreu no processo de carregamento de um símbolo. Esse evento pode ser qualquer coisa, desde uma tentativa de ler os dados em uma imagem executável até o local bem-sucedido de um arquivo de símbolo. **SymRegisterCallbackProc64** exibe essa cadeia de caracteres e retorna **true**.

> [!IMPORTANT]
> Certifique-se de retornar **false** para todos os códigos de ação que você não tratar, caso contrário, você poderá experimentar um comportamento indefinido. Consulte [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) para obter uma lista de todos os códigos de ação e suas implicações.

 

Agora que o retorno de chamada está registrado, é hora de carregar o módulo especificado na linha de comando chamando [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex).

Por fim, chame [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) antes de sair.


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



A especificação de **NULL** como o segundo parâmetro de [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indica que o manipulador de símbolo deve usar o caminho de pesquisa padrão para localizar arquivos de símbolo. Para obter informações detalhadas sobre como o manipulador de símbolo localiza arquivos de símbolo ou como um aplicativo pode especificar um caminho de pesquisa de símbolo, consulte [caminhos de símbolo](symbol-paths.md).

A execução deste programa mostra como o caminho do símbolo é processado. Como DbgHelp examina o caminho do símbolo para localizar o arquivo de símbolo, ele chama repetidamente o [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) que, por sua vez, exibe as seguintes cadeias de caracteres que estão sendo passadas pelo dbghelp.

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

 

 



