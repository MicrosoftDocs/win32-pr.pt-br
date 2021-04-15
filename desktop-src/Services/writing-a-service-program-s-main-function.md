---
description: O exemplo a seguir pode ser usado como o ponto de entrada para um programa de serviço que dá suporte a um único serviço.
ms.assetid: 7fdfc20a-9148-4ae1-8101-7a387c0d0edc
title: Gravar uma função main de Programas de Serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83aa743bfabbeafa2e05818c5bb068a949dce807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501574"
---
# <a name="writing-a-service-programs-main-function"></a><span data-ttu-id="c6995-103">Escrevendo a função main de um programa de serviço</span><span class="sxs-lookup"><span data-stu-id="c6995-103">Writing a Service Program's main Function</span></span>

<span data-ttu-id="c6995-104">A função **principal** de um [programa de serviço](service-programs.md) chama a função [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) para se conectar ao SCM (Gerenciador de [controle de serviço](service-control-manager.md) ) e iniciar o thread do Dispatcher de controle.</span><span class="sxs-lookup"><span data-stu-id="c6995-104">The **main** function of a [service program](service-programs.md) calls the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function to connect to the [service control manager](service-control-manager.md) (SCM) and start the control dispatcher thread.</span></span> <span data-ttu-id="c6995-105">Os loops de thread do Dispatcher, aguardando solicitações de controle de entrada para os serviços especificados na tabela de expedição.</span><span class="sxs-lookup"><span data-stu-id="c6995-105">The dispatcher thread loops, waiting for incoming control requests for the services specified in the dispatch table.</span></span> <span data-ttu-id="c6995-106">Esse thread retorna quando há um erro ou quando todos os serviços no processo foram encerrados.</span><span class="sxs-lookup"><span data-stu-id="c6995-106">This thread returns when there is an error or when all of the services in the process have terminated.</span></span> <span data-ttu-id="c6995-107">Quando todos os serviços no processo forem encerrados, o SCM enviará uma solicitação de controle ao thread do Dispatcher solicitando que ele saia.</span><span class="sxs-lookup"><span data-stu-id="c6995-107">When all services in the process have terminated, the SCM sends a control request to the dispatcher thread telling it to exit.</span></span> <span data-ttu-id="c6995-108">Em seguida, esse thread retorna da chamada **StartServiceCtrlDispatcher** e o processo pode ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="c6995-108">This thread then returns from the **StartServiceCtrlDispatcher** call and the process can terminate.</span></span>

<span data-ttu-id="c6995-109">As definições globais a seguir são usadas neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="c6995-109">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="c6995-110">O exemplo a seguir pode ser usado como o ponto de entrada para um programa de serviço que dá suporte a um único serviço.</span><span class="sxs-lookup"><span data-stu-id="c6995-110">The following example can be used as the entry point for a service program that supports a single service.</span></span> <span data-ttu-id="c6995-111">Se o programa de serviço oferecer suporte a vários serviços, adicione os nomes dos serviços adicionais à tabela de expedição para que eles possam ser monitorados pelo thread Dispatcher.</span><span class="sxs-lookup"><span data-stu-id="c6995-111">If your service program supports multiple services, add the names of the additional services to the dispatch table so they can be monitored by the dispatcher thread.</span></span>

<span data-ttu-id="c6995-112">A \_ função tmain é o ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="c6995-112">The \_tmain function is the entry point.</span></span> <span data-ttu-id="c6995-113">A função SvcReportEvent grava mensagens informativas e erros no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="c6995-113">The SvcReportEvent function writes informational messages and errors to the event log.</span></span> <span data-ttu-id="c6995-114">Para obter informações sobre como escrever a função SvcMain, consulte [escrevendo uma função de immain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="c6995-114">For information about writing the SvcMain function, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span> <span data-ttu-id="c6995-115">Para obter mais informações sobre a função SvcInstall, consulte [instalando um serviço](installing-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="c6995-115">For more information about the SvcInstall function, see [Installing a Service](installing-a-service.md).</span></span> <span data-ttu-id="c6995-116">Para obter informações sobre como escrever a função SvcCtrlHandler, consulte [escrevendo uma função de manipulador de controle](writing-a-control-handler-function.md).</span><span class="sxs-lookup"><span data-stu-id="c6995-116">For information about writing the SvcCtrlHandler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span> <span data-ttu-id="c6995-117">Para o serviço de exemplo completo, incluindo a origem da função SvcReportEvent, consulte [svc. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="c6995-117">For the complete example service, including the source for the SvcReportEvent function, see [Svc.cpp](svc-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Entry point for the process
//
// Parameters:
//   None
// 
// Return value:
//   None, defaults to 0 (zero)
//
int __cdecl _tmain(int argc, TCHAR *argv[])
{ 
    // If command-line parameter is "install", install the service. 
    // Otherwise, the service is probably being started by the SCM.

    if( lstrcmpi( argv[1], TEXT("install")) == 0 )
    {
        SvcInstall();
        return;
    }

    // TO_DO: Add any additional services for the process to this table.
    SERVICE_TABLE_ENTRY DispatchTable[] = 
    { 
        { SVCNAME, (LPSERVICE_MAIN_FUNCTION) SvcMain }, 
        { NULL, NULL } 
    }; 
 
    // This call returns when the service has stopped. 
    // The process should simply terminate when the call returns.

    if (!StartServiceCtrlDispatcher( DispatchTable )) 
    { 
        SvcReportEvent(TEXT("StartServiceCtrlDispatcher")); 
    } 
} 

```



<span data-ttu-id="c6995-118">Veja a seguir um exemplo de Sample. h, conforme gerado pelo compilador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c6995-118">The following is an example Sample.h as generated by the message compiler.</span></span> <span data-ttu-id="c6995-119">Para obter mais informações, consulte [Sample.MC](sample-mc.md).</span><span class="sxs-lookup"><span data-stu-id="c6995-119">For more information, see [Sample.mc](sample-mc.md).</span></span>

``` syntax
 // The following are message definitions.
//
//  Values are 32 bit values layed out as follows:
//
//   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
//   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
//  +---+-+-+-----------------------+-------------------------------+
//  |Sev|C|R|     Facility          |               Code            |
//  +---+-+-+-----------------------+-------------------------------+
//
//  where
//
//      Sev - is the severity code
//
//          00 - Success
//          01 - Informational
//          10 - Warning
//          11 - Error
//
//      C - is the Customer code flag
//
//      R - is a reserved bit
//
//      Facility - is the facility code
//
//      Code - is the facility's status code
//
//
// Define the facility codes
//
#define FACILITY_SYSTEM                  0x0
#define FACILITY_STUBS                   0x3
#define FACILITY_RUNTIME                 0x2
#define FACILITY_IO_ERROR_CODE           0x4


//
// Define the severity codes
//
#define STATUS_SEVERITY_WARNING          0x2
#define STATUS_SEVERITY_SUCCESS          0x0
#define STATUS_SEVERITY_INFORMATIONAL    0x1
#define STATUS_SEVERITY_ERROR            0x3


//
// MessageId: SVC_ERROR
//
// MessageText:
//
//  An error has occurred (%2).
//  
//
#define SVC_ERROR                        ((DWORD)0xC0020001L)
```

## <a name="related-topics"></a><span data-ttu-id="c6995-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6995-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6995-121">Ponto de entrada de serviço</span><span class="sxs-lookup"><span data-stu-id="c6995-121">Service Entry Point</span></span>](service-entry-point.md)
</dt> <dt>

[<span data-ttu-id="c6995-122">O exemplo de serviço completo</span><span class="sxs-lookup"><span data-stu-id="c6995-122">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



