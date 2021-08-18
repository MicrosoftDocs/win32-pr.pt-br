---
description: Quando uma função Handler é chamada pelo thread do dispatcher, ela trata o código de controle passado no parâmetro Opcode e, em seguida, chama a função ReportSvcStatus para atualizar o status do serviço.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Escrevendo uma função de manipulador de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bf8ab32edb73fdf11f3f0370a512b17b143b8af219a2bd539e59bdf062a00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888057"
---
# <a name="writing-a-control-handler-function"></a>Escrevendo uma função de manipulador de controle

Quando uma [**função Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) é chamada pelo thread do dispatcher, ela trata o código de controle passado no parâmetro *Opcode* e, em seguida, chama a função ReportSvcStatus para atualizar o status do serviço. Quando uma [**função handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) recebe um código de controle, ela deve relatar o status do serviço somente se o tratamento do código de controle faz com que o status do serviço seja alterado. Se o serviço não agir no controle, ele não deverá relatar o status ao gerenciador de controle de serviço. Para o código-fonte de ReportSvcStatus, consulte [Escrevendo uma função ServiceMain](writing-a-servicemain-function.md).

No exemplo a seguir, a função SvcCtrlHandler é um exemplo de uma [**função handler.**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) Observe que a variável ghSvcStopEvent é uma variável global que deve ser inicializada e usada conforme demonstrado em Escrevendo uma [função ServiceMain](writing-a-servicemain-function.md).


```C++
//
// Purpose: 
//   Called by SCM whenever a control code is sent to the service
//   using the ControlService function.
//
// Parameters:
//   dwCtrl - control code
// 
// Return value:
//   None
//
VOID WINAPI SvcCtrlHandler( DWORD dwCtrl )
{
   // Handle the requested control code. 

   switch(dwCtrl) 
   {  
      case SERVICE_CONTROL_STOP: 
         ReportSvcStatus(SERVICE_STOP_PENDING, NO_ERROR, 0);

         // Signal the service to stop.

         SetEvent(ghSvcStopEvent);
         ReportSvcStatus(gSvcStatus.dwCurrentState, NO_ERROR, 0);
         
         return;
 
      case SERVICE_CONTROL_INTERROGATE: 
         break; 
 
      default: 
         break;
   } 
   
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Função do manipulador do controle de serviço](service-control-handler-function.md)
</dt> <dt>

[O exemplo de serviço completo](the-complete-service-sample.md)
</dt> </dl>

 

 



