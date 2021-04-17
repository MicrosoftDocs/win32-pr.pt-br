---
description: A função SvcMain no exemplo a seguir é a função usermain para o serviço de exemplo.
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: Escrevendo uma função de immain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3e947c356bad6c6d54395a671aa192c93de1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756140"
---
# <a name="writing-a-servicemain-function"></a><span data-ttu-id="015fb-103">Escrevendo uma função de immain</span><span class="sxs-lookup"><span data-stu-id="015fb-103">Writing a ServiceMain Function</span></span>

<span data-ttu-id="015fb-104">A função SvcMain no exemplo a seguir é a função [**usermain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) para o serviço de exemplo.</span><span class="sxs-lookup"><span data-stu-id="015fb-104">The SvcMain function in the following example is the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function for the example service.</span></span> <span data-ttu-id="015fb-105">SvcMain tem acesso aos argumentos de linha de comando para o serviço da forma que a função **principal** de um aplicativo de console.</span><span class="sxs-lookup"><span data-stu-id="015fb-105">SvcMain has access to the command-line arguments for the service in the way that the **main** function of a console application does.</span></span> <span data-ttu-id="015fb-106">O primeiro parâmetro contém o número de argumentos que estão sendo passados para o serviço no segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="015fb-106">The first parameter contains the number of arguments being passed to the service in the second parameter.</span></span> <span data-ttu-id="015fb-107">Sempre haverá pelo menos um argumento.</span><span class="sxs-lookup"><span data-stu-id="015fb-107">There will always be at least one argument.</span></span> <span data-ttu-id="015fb-108">O segundo parâmetro é um ponteiro para uma matriz de ponteiros de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="015fb-108">The second parameter is a pointer to an array of string pointers.</span></span> <span data-ttu-id="015fb-109">O primeiro item na matriz é sempre o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="015fb-109">The first item in the array is always the service name.</span></span>

<span data-ttu-id="015fb-110">A função SvcMain primeiro chama a função [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) para registrar a função SvcCtrlHandler como a função de [**manipulador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) do serviço e iniciar a inicialização.</span><span class="sxs-lookup"><span data-stu-id="015fb-110">The SvcMain function first calls the [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) function to register the SvcCtrlHandler function as the service's [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function and begin initialization.</span></span> <span data-ttu-id="015fb-111">**RegisterServiceCtrlHandler** deve ser a primeira função que não é de falha no [**usermain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) para que o serviço possa usar o identificador de status retornado por essa função para chamar [**falha em SETSERVICESTATUS**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) com o estado do serviço \_ parado se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="015fb-111">**RegisterServiceCtrlHandler** should be the first nonfailing function in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) so the service can use the status handle returned by this function to call [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) with the SERVICE\_STOPPED state if an error occurs.</span></span>

<span data-ttu-id="015fb-112">Em seguida, a função SvcMain chama a função ReportSvcStatus para indicar que seu status inicial é \_ início do serviço \_ pendente.</span><span class="sxs-lookup"><span data-stu-id="015fb-112">Next, the SvcMain function calls the ReportSvcStatus function to indicate that its initial status is SERVICE\_START\_PENDING.</span></span> <span data-ttu-id="015fb-113">Enquanto o serviço está nesse estado, nenhum controle é aceito.</span><span class="sxs-lookup"><span data-stu-id="015fb-113">While the service is in this state, no controls are accepted.</span></span> <span data-ttu-id="015fb-114">Para simplificar a lógica do serviço, é recomendável que o serviço não aceite nenhum controle enquanto estiver executando sua inicialização.</span><span class="sxs-lookup"><span data-stu-id="015fb-114">To simplify the logic of the service, it is recommended that the service not accept any controls while it is performing its initialization.</span></span>

<span data-ttu-id="015fb-115">Por fim, a função SvcMain chama a função SvcInit para executar a inicialização específica do serviço e iniciar o trabalho a ser executado pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="015fb-115">Finally, the SvcMain function calls the SvcInit function to perform the service-specific initialization and begin the work to be performed by the service.</span></span>

<span data-ttu-id="015fb-116">A função de inicialização de exemplo, SvcInit, é um exemplo muito simples; Ele não executa tarefas de inicialização mais complexas, como a criação de threads adicionais.</span><span class="sxs-lookup"><span data-stu-id="015fb-116">The sample initialization function, SvcInit, is a very simple example; it does not perform more complex initialization tasks such as creating additional threads.</span></span> <span data-ttu-id="015fb-117">Ele cria um evento que o manipulador de controle de serviço pode sinalizar para indicar que o serviço deve parar e, em seguida, chama ReportSvcStatus para indicar que o serviço entrou no estado de execução do serviço \_ .</span><span class="sxs-lookup"><span data-stu-id="015fb-117">It creates an event that the service control handler can signal to indicate that the service should stop, then calls ReportSvcStatus to indicate that the service has entered the SERVICE\_RUNNING state.</span></span> <span data-ttu-id="015fb-118">Neste ponto, o serviço concluiu sua inicialização e está pronto para aceitar controles.</span><span class="sxs-lookup"><span data-stu-id="015fb-118">At this point, the service has completed its initialization and is ready to accept controls.</span></span> <span data-ttu-id="015fb-119">Para melhor desempenho do sistema, seu aplicativo deve entrar no estado de execução dentro de 25-100 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="015fb-119">For best system performance, your application should enter the running state within 25-100 milliseconds.</span></span>

<span data-ttu-id="015fb-120">Como esse serviço de exemplo não completa nenhuma tarefa real, SvcInit simplesmente aguarda que o evento de parada do serviço seja sinalizado chamando a função [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) , chama ReportSvcStatus para indicar que o serviço entrou no estado de serviço \_ parado e retorna.</span><span class="sxs-lookup"><span data-stu-id="015fb-120">Because this sample service does not complete any real tasks, SvcInit simply waits for the service stop event to be signaled by calling the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function, calls ReportSvcStatus to indicate that the service has entered the SERVICE\_STOPPED state, and returns.</span></span> <span data-ttu-id="015fb-121">(Observe que é importante que a função seja retornada, em vez de chamar a função [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) , porque o retorno permite a limpeza da memória alocada para os argumentos.) Você pode executar tarefas de limpeza adicionais usando a função [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) em vez de **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="015fb-121">(Note that it is important for the function to return, rather than call the [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) function, because returning allows for cleanup of the memory allocated for the arguments.) You can perform additional cleanup tasks by using the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) function instead of **WaitForSingleObject**.</span></span> <span data-ttu-id="015fb-122">O thread que está executando a função de [**immain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) é encerrado, mas o próprio serviço continua a ser executado.</span><span class="sxs-lookup"><span data-stu-id="015fb-122">The thread that is running the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function terminates, but the service itself continues to run.</span></span> <span data-ttu-id="015fb-123">Quando o manipulador de controle de serviço sinaliza o evento, um thread do pool de threads executa o retorno de chamada para executar a limpeza adicional, incluindo a definição do status como serviço \_ parado.</span><span class="sxs-lookup"><span data-stu-id="015fb-123">When the service control handler signals the event, a thread from the thread pool executes your callback to perform the additional cleanup, including setting the status to SERVICE\_STOPPED.</span></span>

<span data-ttu-id="015fb-124">Observe que este exemplo usa SvcReportEvent para gravar eventos de erro no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="015fb-124">Note that this example uses SvcReportEvent to write error events to the event log.</span></span> <span data-ttu-id="015fb-125">Para o código-fonte para SvcReportEvent, consulte [svc. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="015fb-125">For the source code for SvcReportEvent, see [Svc.cpp](svc-cpp.md).</span></span> <span data-ttu-id="015fb-126">Para obter uma função de manipulador de controle de exemplo, consulte [escrevendo uma função de manipulador de controle](writing-a-control-handler-function.md).</span><span class="sxs-lookup"><span data-stu-id="015fb-126">For an example control handler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span>

<span data-ttu-id="015fb-127">As definições globais a seguir são usadas neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="015fb-127">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="015fb-128">O fragmento de exemplo a seguir é obtido do exemplo de serviço completo.</span><span class="sxs-lookup"><span data-stu-id="015fb-128">The following sample fragment is taken from the complete service sample.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="015fb-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="015fb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="015fb-130">Função Service-Main</span><span class="sxs-lookup"><span data-stu-id="015fb-130">Service ServiceMain Function</span></span>](service-servicemain-function.md)
</dt> <dt>

[<span data-ttu-id="015fb-131">O exemplo de serviço completo</span><span class="sxs-lookup"><span data-stu-id="015fb-131">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
