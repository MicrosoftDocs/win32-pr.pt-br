---
description: Normalmente, os serviços são escritos como aplicativos de console.
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: Ponto de entrada de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9e2683c4a69949b6f51c7d000c0ee3571fe118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920845"
---
# <a name="service-entry-point"></a><span data-ttu-id="2b3a7-103">Ponto de entrada de serviço</span><span class="sxs-lookup"><span data-stu-id="2b3a7-103">Service Entry Point</span></span>

<span data-ttu-id="2b3a7-104">Normalmente, os serviços são escritos como aplicativos de console.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-104">Services are generally written as console applications.</span></span> <span data-ttu-id="2b3a7-105">O ponto de entrada de um aplicativo de console é sua função **principal** .</span><span class="sxs-lookup"><span data-stu-id="2b3a7-105">The entry point of a console application is its **main** function.</span></span> <span data-ttu-id="2b3a7-106">A função **Main** recebe argumentos do valor **ImagePath** da chave do registro para o serviço.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-106">The **main** function receives arguments from the **ImagePath** value from the registry key for the service.</span></span> <span data-ttu-id="2b3a7-107">Para obter mais informações, consulte a seção comentários da função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) .</span><span class="sxs-lookup"><span data-stu-id="2b3a7-107">For more information, see the Remarks section of the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function.</span></span>

<span data-ttu-id="2b3a7-108">Quando o SCM inicia um programa de serviço, ele aguarda que ele chame a função [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) .</span><span class="sxs-lookup"><span data-stu-id="2b3a7-108">When the SCM starts a service program, it waits for it to call the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function.</span></span> <span data-ttu-id="2b3a7-109">Use as diretrizes a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-109">Use the following guidelines.</span></span>

-   <span data-ttu-id="2b3a7-110">Um serviço do tipo \_ \_ próprio processo do Win32 \_ deve chamar [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) imediatamente, de seu thread principal.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-110">A service of type SERVICE\_WIN32\_OWN\_PROCESS should call [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) immediately, from its main thread.</span></span> <span data-ttu-id="2b3a7-111">Você pode executar qualquer inicialização depois que o serviço for iniciado, conforme descrito em [função Service-Main](service-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="2b3a7-111">You can perform any initialization after the service starts, as described in [Service ServiceMain Function](service-servicemain-function.md).</span></span>
-   <span data-ttu-id="2b3a7-112">Se o tipo de serviço for o \_ processo de compartilhamento Win32 do serviço \_ \_ e houver inicialização comum para todos os serviços no programa, você poderá executar a inicialização no thread principal antes de chamar [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera), desde que demore menos de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-112">If the service type is SERVICE\_WIN32\_SHARE\_PROCESS and there is common initialization for all services in the program, you can perform the initialization in the main thread before calling [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera), as long as it takes less than 30 seconds.</span></span> <span data-ttu-id="2b3a7-113">Caso contrário, você deve criar outro thread para fazer a inicialização comum, enquanto o thread principal chama **StartServiceCtrlDispatcher**.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-113">Otherwise, you must create another thread to do the common initialization, while the main thread calls **StartServiceCtrlDispatcher**.</span></span> <span data-ttu-id="2b3a7-114">Você ainda deve executar qualquer inicialização específica do serviço depois que o serviço for iniciado.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-114">You should still perform any service-specific initialization after the service starts.</span></span>

<span data-ttu-id="2b3a7-115">A função [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) usa uma estrutura de [**\_ \_ entrada de tabela de serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) para cada serviço contido no processo.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-115">The [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function takes a [**SERVICE\_TABLE\_ENTRY**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) structure for each service contained in the process.</span></span> <span data-ttu-id="2b3a7-116">Cada estrutura especifica o nome do serviço e o ponto de entrada para o serviço.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-116">Each structure specifies the service name and the entry point for the service.</span></span> <span data-ttu-id="2b3a7-117">Para obter um exemplo, consulte [escrevendo a função principal de um programa de serviço](writing-a-service-program-s-main-function.md).</span><span class="sxs-lookup"><span data-stu-id="2b3a7-117">For an example, see [Writing a Service Program's main Function](writing-a-service-program-s-main-function.md).</span></span>

<span data-ttu-id="2b3a7-118">Se [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) tiver sucesso, o thread de chamada não retornará até que todos os serviços em execução no processo tenham inserido o \_ estado serviço parado.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-118">If [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) succeeds, the calling thread does not return until all running services in the process have entered the SERVICE\_STOPPED state.</span></span> <span data-ttu-id="2b3a7-119">O SCM envia solicitações de controle para esse thread por meio de um pipe nomeado.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-119">The SCM sends control requests to this thread through a named pipe.</span></span> <span data-ttu-id="2b3a7-120">O thread atua como um Dispatcher de controle, executando as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="2b3a7-120">The thread acts as a control dispatcher, performing the following tasks:</span></span>

-   <span data-ttu-id="2b3a7-121">Crie um novo thread para chamar o ponto de entrada apropriado quando um novo serviço for iniciado.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-121">Create a new thread to call the appropriate entry point when a new service is started.</span></span>
-   <span data-ttu-id="2b3a7-122">Chame a [função de manipulador](service-control-handler-function.md) apropriada para manipular solicitações de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="2b3a7-122">Call the appropriate [handler function](service-control-handler-function.md) to handle service control requests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b3a7-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b3a7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b3a7-124">Escrevendo a função main de um programa de serviço</span><span class="sxs-lookup"><span data-stu-id="2b3a7-124">Writing a Service Program's main Function</span></span>](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



