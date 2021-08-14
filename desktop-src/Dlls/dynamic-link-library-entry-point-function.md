---
description: Uma DLL pode, opcionalmente, especificar uma função de ponto de entrada.
ms.assetid: ec035fc6-0a6f-4e52-a4cc-8d7a25a94366
title: Dynamic-Link biblioteca Entry-Point função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6289f705a11dad58eca8b047ba469ee07320dedef762024cbfa04046a0677f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815834"
---
# <a name="dynamic-link-library-entry-point-function"></a>Dynamic-Link biblioteca Entry-Point função

Uma DLL pode, opcionalmente, especificar uma função de ponto de entrada. Se estiver presente, o sistema chamará a função de ponto de entrada sempre que um processo ou thread carregar ou descarregar a DLL. Ele pode ser usado para executar tarefas simples de inicialização e limpeza. Por exemplo, ele pode configurar o armazenamento local do thread quando um novo thread é criado e limpá-lo quando o thread é encerrado.

Se você estiver vinculando sua DLL à biblioteca em tempo de executar C, ela poderá fornecer uma função de ponto de entrada para você e permitir que você forneça uma função de inicialização separada. Verifique a documentação da biblioteca em tempo de executar para obter mais informações.

Se você estiver fornecendo seu próprio ponto de entrada, consulte a [**função DllMain.**](dllmain.md) O nome **DllMain** é um espaço reservado para uma função definida pelo usuário. Você deve especificar o nome real usado ao criar sua DLL. Para obter mais informações, consulte a documentação incluída com suas ferramentas de desenvolvimento.

## <a name="calling-the-entry-point-function"></a>Chamando a função Entry-Point

O sistema chama a função de ponto de entrada sempre que ocorre um dos seguintes eventos:

-   Um processo carrega a DLL. Para processos que usam vinculação dinâmica de tempo de carregamento, a DLL é carregada durante a inicialização do processo. Para processos que usam a vinculação em tempo de executar, a DLL é carregada antes que [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**ou LoadLibraryEx retorne.**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   Um processo descarrega a DLL. A DLL é descarregada quando o processo é encerrado ou chama a [**função FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) e a contagem de referência se torna zero. Se o processo for encerrado como resultado da função [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) ou [**TerminateThread,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) o sistema não chamará a função de ponto de entrada DLL.
-   Um novo thread é criado em um processo que carregou a DLL. Você pode usar a [**função DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) para desabilitar a notificação quando os threads são criados.
-   Um thread de um processo que carregou a DLL é encerrado normalmente, não usando [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) ou [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Quando um processo descarrega a DLL, a função de ponto de entrada é chamada apenas uma vez para todo o processo, em vez de uma vez para cada thread existente do processo. Você pode usar [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) para desabilitar a notificação quando os threads são encerrados.

Somente um thread por vez pode chamar a função de ponto de entrada.

O sistema chama a função de ponto de entrada no contexto do processo ou thread que fez com que a função fosse chamada. Isso permite que uma DLL use sua função de ponto de entrada para alocar memória no espaço de endereço virtual do processo de chamada ou para abrir os alças acessíveis ao processo. A função de ponto de entrada também pode alocar memória privada para um novo thread usando o armazenamento local do thread (TLS). Para obter mais informações sobre o armazenamento local do thread, consulte [Thread Local Armazenamento](/windows/desktop/ProcThread/thread-local-storage).

## <a name="entry-point-function-definition"></a>Entry-Point de função

A função de ponto de entrada da DLL deve ser declarada com a convenção de chamada padrão. Se o ponto de entrada da DLL não for declarado corretamente, a DLL não será carregada e o sistema exibirá uma mensagem indicando que o ponto de entrada da DLL deve ser declarado com WINAPI.

No corpo da função, você pode lidar com qualquer combinação dos seguintes cenários em que o ponto de entrada de DLL foi chamado:

-   Um processo carrega a DLL (**DLL \_ PROCESS \_ ATTACH).**
-   O processo atual cria um novo thread (**DLL \_ THREAD \_ ATTACH**).
-   Um thread sai normalmente (**DLL \_ THREAD \_ DETACH**).
-   Um processo descarrega a DLL (**DLL \_ PROCESS \_ DETACH).**

A função de ponto de entrada deve executar apenas tarefas de inicialização simples. Ele não deve chamar a [**função LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (ou uma função que chama essas funções), pois isso pode criar loops de dependência na ordem de carregamento da DLL. Isso pode fazer com que uma DLL seja usada antes que o sistema execute seu código de inicialização. Da mesma forma, a função de ponto de entrada não deve chamar a função [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (ou uma função que chama **FreeLibrary**) durante o encerramento do processo, pois isso pode resultar em uma DLL sendo usada depois que o sistema tiver executado seu código de encerramento.

Como Kernel32.dll é garantido que o Kernel32.dll seja carregado no espaço de endereço do processo quando a função de ponto de entrada for chamada, chamar funções no Kernel32.dll não resultará no uso da DLL antes de seu código de inicialização ter sido executado. Portanto, a função de [](/windows/desktop/Sync/synchronization-objects) ponto de entrada pode criar objetos de sincronização, como seções críticas e mutexes, e usar TLS, pois essas funções estão localizadas em Kernel32.dll. Não é seguro chamar as funções do Registro, por exemplo, porque elas estão localizadas em Advapi32.dll.

Chamar outras funções pode resultar em problemas difíceis de diagnosticar. Por exemplo, chamar funções User, Shell e COM pode causar erros de violação de acesso, porque algumas funções em suas DLLs chamam [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar outros componentes do sistema. Por outro lado, chamar essas funções durante o encerramento pode causar erros de violação de acesso porque o componente correspondente pode já ter sido descarregado ou não reinicializado.

O exemplo a seguir demonstra como estruturar a função de ponto de entrada de DLL.

``` syntax
BOOL WINAPI DllMain(
    HINSTANCE hinstDLL,  // handle to DLL module
    DWORD fdwReason,     // reason for calling function
    LPVOID lpReserved )  // reserved
{
    // Perform actions based on the reason for calling.
    switch( fdwReason ) 
    { 
        case DLL_PROCESS_ATTACH:
         // Initialize once for each new process.
         // Return FALSE to fail DLL load.
            break;

        case DLL_THREAD_ATTACH:
         // Do thread-specific initialization.
            break;

        case DLL_THREAD_DETACH:
         // Do thread-specific cleanup.
            break;

        case DLL_PROCESS_DETACH:
         // Perform any necessary cleanup.
            break;
    }
    return TRUE;  // Successful DLL_PROCESS_ATTACH.
}
```

## <a name="entry-point-function-return-value"></a>Entry-Point valor de retorno da função de Entry-Point

Quando uma função de ponto de entrada de DLL é chamada porque um processo está sendo carregado, a função retorna **TRUE** para indicar êxito. Para processos que usam vinculação de tempo de carregamento, um valor de retorno **FALSE** faz com que a inicialização do processo falhe e o processo seja encerrado. Para processos que usam vinculação em tempo de executar, um valor de retorno FALSE faz com que a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) retorne **NULL,** indicando falha. (O sistema chama imediatamente sua função de ponto de entrada com **DLL \_ PROCESS \_ DETACH** e descarrega a DLL.) O valor de retorno da função de ponto de entrada é desconsiderado quando a função é chamada por qualquer outro motivo.

 

 
