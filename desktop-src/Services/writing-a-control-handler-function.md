---
description: Quando uma função de manipulador é chamada pelo thread Dispatcher, ela manipula o código de controle passado no parâmetro opcode e, em seguida, chama a função ReportSvcStatus para atualizar o status do serviço.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Escrevendo uma função de manipulador de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724a04aa20143d2c4a506da7ac17119388a8c82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753921"
---
# <a name="writing-a-control-handler-function"></a>Escrevendo uma função de manipulador de controle

Quando uma função de [**manipulador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) é chamada pelo thread Dispatcher, ela manipula o código de controle passado no parâmetro *opcode* e, em seguida, chama a função ReportSvcStatus para atualizar o status do serviço. Quando uma função de [**manipulador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) recebe um código de controle, ela deve relatar o status do serviço somente se manipular o código de controle faz com que o status do serviço seja alterado. Se o serviço não agir no controle, ele não deverá relatar o status para o Gerenciador de controle de serviços. Para obter o código-fonte para ReportSvcStatus, consulte [escrevendo uma função de immain](writing-a-servicemain-function.md).

No exemplo a seguir, a função SvcCtrlHandler é um exemplo de uma função de [**manipulador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) . Observe que a variável ghSvcStopEvent é uma variável global que deve ser inicializada e usada conforme demonstrado na [gravação de uma função de um usermain](writing-a-servicemain-function.md).


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

 

 



