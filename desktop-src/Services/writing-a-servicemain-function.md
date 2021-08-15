---
description: A função SvcMain no exemplo a seguir é a função ServiceMain para o serviço de exemplo.
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: Escrevendo uma função ServiceMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca28b09efdc228457ae85d8a3343f334a26f246b6e48e49208d7416551e7f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887969"
---
# <a name="writing-a-servicemain-function"></a>Escrevendo uma função ServiceMain

A função SvcMain no exemplo a seguir é a [**função ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) para o serviço de exemplo. O SvcMain tem acesso aos argumentos de linha de comando para o serviço da maneira que a **função** principal de um aplicativo de console faz. O primeiro parâmetro contém o número de argumentos que estão sendo passados para o serviço no segundo parâmetro. Sempre haverá pelo menos um argumento. O segundo parâmetro é um ponteiro para uma matriz de ponteiros de cadeia de caracteres. O primeiro item na matriz é sempre o nome do serviço.

A função SvcMain primeiro chama a função [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) para registrar a função SvcCtrlHandler como a função [**manipulador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) do serviço e iniciar a inicialização. **RegisterServiceCtrlHandler** deve ser a primeira função não funcional no [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) para que o serviço possa usar o alça de status retornado por essa função para chamar [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) com o estado SERVICE STOPPED se ocorrer um \_ erro.

Em seguida, a função SvcMain chama a função ReportSvcStatus para indicar que seu status inicial é SERVICE \_ START \_ PENDING. Enquanto o serviço estiver nesse estado, nenhum controle será aceito. Para simplificar a lógica do serviço, é recomendável que o serviço não aceite nenhum controle enquanto estiver executando sua inicialização.

Por fim, a função SvcMain chama a função SvcInit para executar a inicialização específica do serviço e iniciar o trabalho a ser executado pelo serviço.

A função de inicialização de exemplo, SvcInit, é um exemplo muito simples; ele não executa tarefas de inicialização mais complexas, como a criação de threads adicionais. Ele cria um evento que o manipulador de controle de serviço pode sinalizar para indicar que o serviço deve parar e, em seguida, chama ReportSvcStatus para indicar que o serviço entrou no estado SERVICE \_ RUNNING. Neste ponto, o serviço concluiu sua inicialização e está pronto para aceitar controles. Para melhor desempenho do sistema, seu aplicativo deve inserir o estado de execução dentro de 25 a 100 milissegundos.

Como esse serviço de exemplo não conclui nenhuma tarefa real, o SvcInit simplesmente aguarda que o evento de parada de serviço seja sinalizado chamando a função [**WaitForSingleObject,**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) chama ReportSvcStatus para indicar que o serviço entrou no estado SERVICE STOPPED e \_ retorna. (Observe que é importante que a função retorne, em vez de chamar a função [**ExitThread,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) porque retornar permite a limpeza da memória alocada para os argumentos.) Você pode executar tarefas de limpeza adicionais usando [**a função RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) em vez de **WaitForSingleObject**. O thread que está executando a [**função ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) é encerrado, mas o próprio serviço continua sendo executado. Quando o manipulador de controle de serviço sinaliza o evento, um thread do pool de threads executa o retorno de chamada para executar a limpeza adicional, incluindo a definição do status como SERVICE \_ STOPPED.

Observe que este exemplo usa SvcReportEvent para gravar eventos de erro no log de eventos. Para o código-fonte de SvcReportEvent, consulte [Svc.cpp](svc-cpp.md). Para uma função de manipulador de controle de exemplo, consulte [Escrevendo uma função de manipulador de controle](writing-a-control-handler-function.md).

As definições globais a seguir são usadas neste exemplo.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



O fragmento de exemplo a seguir é retirado do exemplo de serviço completo.


```C++
//
// Purpose: 
//   Entry point for the service
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None.
//
VOID WINAPI SvcMain( DWORD dwArgc, LPTSTR *lpszArgv )
{
    // Register the handler function for the service

    gSvcStatusHandle = RegisterServiceCtrlHandler( 
        SVCNAME, 
        SvcCtrlHandler);

    if( !gSvcStatusHandle )
    { 
        SvcReportEvent(TEXT("RegisterServiceCtrlHandler")); 
        return; 
    } 

    // These SERVICE_STATUS members remain as set here

    gSvcStatus.dwServiceType = SERVICE_WIN32_OWN_PROCESS; 
    gSvcStatus.dwServiceSpecificExitCode = 0;    

    // Report initial status to the SCM

    ReportSvcStatus( SERVICE_START_PENDING, NO_ERROR, 3000 );

    // Perform service-specific initialization and work.

    SvcInit( dwArgc, lpszArgv );
}

//
// Purpose: 
//   The service code
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None
//
VOID SvcInit( DWORD dwArgc, LPTSTR *lpszArgv)
{
    // TO_DO: Declare and set any required variables.
    //   Be sure to periodically call ReportSvcStatus() with 
    //   SERVICE_START_PENDING. If initialization fails, call
    //   ReportSvcStatus with SERVICE_STOPPED.

    // Create an event. The control handler function, SvcCtrlHandler,
    // signals this event when it receives the stop control code.

    ghSvcStopEvent = CreateEvent(
                         NULL,    // default security attributes
                         TRUE,    // manual reset event
                         FALSE,   // not signaled
                         NULL);   // no name

    if ( ghSvcStopEvent == NULL)
    {
        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }

    // Report running status when initialization is complete.

    ReportSvcStatus( SERVICE_RUNNING, NO_ERROR, 0 );

    // TO_DO: Perform work until service stops.

    while(1)
    {
        // Check whether to stop the service.

        WaitForSingleObject(ghSvcStopEvent, INFINITE);

        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }
}

//
// Purpose: 
//   Sets the current service status and reports it to the SCM.
//
// Parameters:
//   dwCurrentState - The current state (see SERVICE_STATUS)
//   dwWin32ExitCode - The system error code
//   dwWaitHint - Estimated time for pending operation, 
//     in milliseconds
// 
// Return value:
//   None
//
VOID ReportSvcStatus( DWORD dwCurrentState,
                      DWORD dwWin32ExitCode,
                      DWORD dwWaitHint)
{
    static DWORD dwCheckPoint = 1;

    // Fill in the SERVICE_STATUS structure.

    gSvcStatus.dwCurrentState = dwCurrentState;
    gSvcStatus.dwWin32ExitCode = dwWin32ExitCode;
    gSvcStatus.dwWaitHint = dwWaitHint;

    if (dwCurrentState == SERVICE_START_PENDING)
        gSvcStatus.dwControlsAccepted = 0;
    else gSvcStatus.dwControlsAccepted = SERVICE_ACCEPT_STOP;

    if ( (dwCurrentState == SERVICE_RUNNING) ||
           (dwCurrentState == SERVICE_STOPPED) )
        gSvcStatus.dwCheckPoint = 0;
    else gSvcStatus.dwCheckPoint = dwCheckPoint++;

    // Report the status of the service to the SCM.
    SetServiceStatus( gSvcStatusHandle, &gSvcStatus );
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Função ServiceMain](service-servicemain-function.md)
</dt> <dt>

[O exemplo de serviço completo](the-complete-service-sample.md)
</dt> </dl>

 

 
