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
# <a name="writing-a-control-handler-function"></a><span data-ttu-id="7dff3-103">Escrevendo uma função de manipulador de controle</span><span class="sxs-lookup"><span data-stu-id="7dff3-103">Writing a Control Handler Function</span></span>

<span data-ttu-id="7dff3-104">Quando uma função de [**manipulador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) é chamada pelo thread Dispatcher, ela manipula o código de controle passado no parâmetro *opcode* e, em seguida, chama a função ReportSvcStatus para atualizar o status do serviço.</span><span class="sxs-lookup"><span data-stu-id="7dff3-104">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function is called by the dispatcher thread, it handles the control code passed in the *Opcode* parameter and then calls the ReportSvcStatus function to update the service status.</span></span> <span data-ttu-id="7dff3-105">Quando uma função de [**manipulador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) recebe um código de controle, ela deve relatar o status do serviço somente se manipular o código de controle faz com que o status do serviço seja alterado.</span><span class="sxs-lookup"><span data-stu-id="7dff3-105">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function receives a control code, it should report the service status only if handling the control code causes the service status to change.</span></span> <span data-ttu-id="7dff3-106">Se o serviço não agir no controle, ele não deverá relatar o status para o Gerenciador de controle de serviços.</span><span class="sxs-lookup"><span data-stu-id="7dff3-106">If the service does not act on the control, it should not report status to the service control manager.</span></span> <span data-ttu-id="7dff3-107">Para obter o código-fonte para ReportSvcStatus, consulte [escrevendo uma função de immain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="7dff3-107">For the source code for ReportSvcStatus, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span>

<span data-ttu-id="7dff3-108">No exemplo a seguir, a função SvcCtrlHandler é um exemplo de uma função de [**manipulador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) .</span><span class="sxs-lookup"><span data-stu-id="7dff3-108">In the following example, the SvcCtrlHandler function is an example of a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function.</span></span> <span data-ttu-id="7dff3-109">Observe que a variável ghSvcStopEvent é uma variável global que deve ser inicializada e usada conforme demonstrado na [gravação de uma função de um usermain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="7dff3-109">Note that the ghSvcStopEvent variable is a global variable that should be initialized and used as demonstrated in [Writing a ServiceMain function](writing-a-servicemain-function.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7dff3-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7dff3-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dff3-111">Função do manipulador do controle de serviço</span><span class="sxs-lookup"><span data-stu-id="7dff3-111">Service Control Handler Function</span></span>](service-control-handler-function.md)
</dt> <dt>

[<span data-ttu-id="7dff3-112">O exemplo de serviço completo</span><span class="sxs-lookup"><span data-stu-id="7dff3-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



