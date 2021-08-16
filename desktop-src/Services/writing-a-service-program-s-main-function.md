---
description: O exemplo a seguir pode ser usado como o ponto de entrada para um programa de serviço que dá suporte a um único serviço.
ms.assetid: 7fdfc20a-9148-4ae1-8101-7a387c0d0edc
title: Gravar uma função main de Programas de Serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82e3c519650957f4f27b00ff54864f558cafba3db960f30c0dd20517328f1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117966607"
---
# <a name="writing-a-service-programs-main-function"></a>Escrevendo a função principal de um programa de serviço

A **função** principal de um programa de [serviço](service-programs.md) chama a função [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) para se conectar ao SCM [(gerenciador](service-control-manager.md) de controle de serviço) e iniciar o thread do dispatcher de controle. O thread do dispatcher faz loops, aguardando solicitações de controle de entrada para os serviços especificados na tabela de expedição. Esse thread retorna quando há um erro ou quando todos os serviços no processo são encerrados. Quando todos os serviços no processo são encerrados, o SCM envia uma solicitação de controle para o thread do dispatcher dizendo para sair. Esse thread retorna da chamada **StartServiceCtrlDispatcher** e o processo pode ser encerrado.

As definições globais a seguir são usadas neste exemplo.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



O exemplo a seguir pode ser usado como o ponto de entrada para um programa de serviço que dá suporte a um único serviço. Se o programa de serviço dá suporte a vários serviços, adicione os nomes dos serviços adicionais à tabela de expedição para que eles possam ser monitorados pelo thread do dispatcher.

A \_ função tmain é o ponto de entrada. A função SvcReportEvent grava mensagens informativas e erros no log de eventos. Para obter informações sobre como escrever a função SvcMain, consulte [Escrevendo uma função ServiceMain](writing-a-servicemain-function.md). Para obter mais informações sobre a função SvcInstall, consulte [Instalando um serviço](installing-a-service.md). Para obter informações sobre como escrever a função SvcCtrlHandler, consulte [Escrevendo uma função de manipulador de controle](writing-a-control-handler-function.md). Para o serviço de exemplo completo, incluindo a origem da função SvcReportEvent, consulte [Svc.cpp](svc-cpp.md).


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



A seguir está um exemplo de Sample.h conforme gerado pelo compilador de mensagem. Para obter mais informações, [consulte Sample.mc](sample-mc.md).

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

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de entrada de serviço](service-entry-point.md)
</dt> <dt>

[O exemplo de serviço completo](the-complete-service-sample.md)
</dt> </dl>

 

 



