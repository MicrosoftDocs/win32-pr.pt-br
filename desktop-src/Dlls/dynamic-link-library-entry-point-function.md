---
description: Uma DLL pode, opcionalmente, especificar uma função de ponto de entrada.
ms.assetid: ec035fc6-0a6f-4e52-a4cc-8d7a25a94366
title: Dynamic-Link Entry-Point função de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62bff557bfa2aa792b420e8fe1856bbe0726921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647718"
---
# <a name="dynamic-link-library-entry-point-function"></a>Dynamic-Link Entry-Point função de biblioteca

Uma DLL pode, opcionalmente, especificar uma função de ponto de entrada. Se estiver presente, o sistema chamará a função de ponto de entrada sempre que um processo ou thread carregar ou descarregar a DLL. Ele pode ser usado para executar tarefas simples de inicialização e limpeza. Por exemplo, ele pode configurar o armazenamento local do thread quando um novo thread é criado e limpá-lo quando o thread for encerrado.

Se você estiver vinculando sua DLL com a biblioteca de tempo de execução C, ela poderá fornecer uma função de ponto de entrada para você e permitir que você forneça uma função de inicialização separada. Verifique a documentação da biblioteca de tempo de execução para obter mais informações.

Se você estiver fornecendo seu próprio ponto de entrada, consulte a função [**DllMain**](dllmain.md) . O nome **DllMain** é um espaço reservado para uma função definida pelo usuário. Você deve especificar o nome real que você usa ao compilar sua DLL. Para obter mais informações, consulte a documentação incluída com suas ferramentas de desenvolvimento.

## <a name="calling-the-entry-point-function"></a>Chamando a função Entry-Point

O sistema chama a função de ponto de entrada sempre que um dos seguintes eventos ocorre:

-   Um processo carrega a DLL. Para processos que usam vinculação dinâmica em tempo de carregamento, a DLL é carregada durante a inicialização do processo. Para processos que usam vinculação em tempo de execução, a DLL é carregada antes de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) retornar.
-   Um processo descarrega a DLL. A DLL é descarregada quando o processo termina ou chama a função [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) e a contagem de referência se torna zero. Se o processo for encerrado como resultado da função [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) ou [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) , o sistema não chamará a função de ponto de entrada de dll.
-   Um novo thread é criado em um processo que carregou a DLL. Você pode usar a função [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) para desabilitar a notificação quando os threads são criados.
-   Um thread de um processo que carregou a DLL é encerrado normalmente, não usando [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) ou [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Quando um processo descarrega a DLL, a função de ponto de entrada é chamada apenas uma vez para todo o processo, em vez de uma vez para cada thread existente do processo. Você pode usar o [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) para desabilitar a notificação quando os threads forem encerrados.

Somente um thread por vez pode chamar a função de ponto de entrada.

O sistema chama a função de ponto de entrada no contexto do processo ou thread que fez com que a função fosse chamada. Isso permite que uma DLL Use sua função de ponto de entrada para alocar memória no espaço de endereço virtual do processo de chamada ou para abrir identificadores acessíveis para o processo. A função de ponto de entrada também pode alocar memória privada para um novo thread usando o armazenamento local de threads (TLS). Para obter mais informações sobre o armazenamento local de thread, consulte [armazenamento local de thread](/windows/desktop/ProcThread/thread-local-storage).

## <a name="entry-point-function-definition"></a>Definição de função Entry-Point

A função de ponto de entrada de DLL deve ser declarada com a Convenção de chamada de chamada padrão. Se o ponto de entrada da DLL não for declarado corretamente, a DLL não será carregada e o sistema exibirá uma mensagem indicando que o ponto de entrada da DLL deve ser declarado com Winapi tenha.

No corpo da função, você pode lidar com qualquer combinação dos seguintes cenários em que o ponto de entrada de DLL foi chamado:

-   Um processo carrega a DLL (**\_ \_ anexar processo de dll**).
-   O processo atual cria um novo thread (**\_ \_ anexação de thread de dll**).
-   Um thread é encerrado normalmente **( \_ \_ desanexar thread de dll**).
-   Um processo descarrega a DLL (**\_ \_ desanexar processo de dll**).

A função de ponto de entrada deve executar apenas tarefas de inicialização simples. Ele não deve chamar a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (ou uma função que chama essas funções), pois isso pode criar loops de dependência na ordem de carregamento da dll. Isso pode resultar na utilização de uma DLL antes que o sistema tenha executado seu código de inicialização. Da mesma forma, a função de ponto de entrada não deve chamar a função [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (ou uma função que chama **FreeLibrary**) durante o encerramento do processo, porque isso pode resultar em uma DLL sendo usada depois que o sistema tiver executado seu código de encerramento.

Como Kernel32.dll é garantido que seja carregado no espaço de endereço do processo quando a função de ponto de entrada é chamada, a chamada de funções no Kernel32.dll não resulta na DLL que está sendo usada antes de seu código de inicialização ser executado. Portanto, a função de ponto de entrada pode criar [objetos de sincronização](/windows/desktop/Sync/synchronization-objects) , como seções críticas e mutexes, e usar TLS, pois essas funções estão localizadas em Kernel32.dll. Não é seguro chamar as funções de registro, por exemplo, porque elas estão localizadas em Advapi32.dll.

Chamar outras funções pode resultar em problemas que são difíceis de diagnosticar. Por exemplo, chamar o usuário, o Shell e as funções COM pode causar erros de violação de acesso, porque algumas funções em suas DLLs chamam [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar outros componentes do sistema. Por outro lado, chamar essas funções durante o encerramento pode causar erros de violação de acesso porque o componente correspondente pode já ter sido descarregado ou não inicializado.

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

## <a name="entry-point-function-return-value"></a>Entry-Point valor de retorno da função

Quando uma função de ponto de entrada de DLL é chamada porque um processo está sendo carregado, a função retorna **true** para indicar êxito. Para processos que usam vinculação de tempo de carga, um valor de retorno **false** faz com que a inicialização do processo falhe e o processo seja encerrado. Para processos que usam vinculação em tempo de execução, um valor de retorno FALSE faz com que a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) retorne **NULL**, indicando falha. (O sistema chama imediatamente sua função de ponto de entrada com o **processo de dll \_ \_ desanexar** e descarrega a dll.) O valor de retorno da função de ponto de entrada é desconsiderado quando a função é chamada por qualquer outro motivo.

 

 
