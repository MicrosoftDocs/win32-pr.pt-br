---
description: Um programa de serviço contém código executável para um ou mais serviços.
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: Programas de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836973"
---
# <a name="service-programs"></a><span data-ttu-id="97a1b-103">Programas de serviço</span><span class="sxs-lookup"><span data-stu-id="97a1b-103">Service Programs</span></span>

<span data-ttu-id="97a1b-104">Um *programa de serviço* contém código executável para um ou mais serviços.</span><span class="sxs-lookup"><span data-stu-id="97a1b-104">A *service program* contains executable code for one or more services.</span></span> <span data-ttu-id="97a1b-105">Um programa de serviço criado com o próprio processo do tipo serviço do \_ Win32 \_ \_ contém o código para apenas um serviço.</span><span class="sxs-lookup"><span data-stu-id="97a1b-105">A service program created with the type SERVICE\_WIN32\_OWN\_PROCESS contains the code for only one service.</span></span> <span data-ttu-id="97a1b-106">Um programa de serviço criado com o processo de compartilhamento Win32 do serviço de tipo \_ \_ \_ contém código para mais de um serviço, permitindo que eles compartilhem código.</span><span class="sxs-lookup"><span data-stu-id="97a1b-106">A service program created with the type SERVICE\_WIN32\_SHARE\_PROCESS contains code for more than one service, enabling them to share code.</span></span> <span data-ttu-id="97a1b-107">Um exemplo de um programa de serviço que faz isso é o processo de host de serviço genérico, Svchost.exe, que hospeda serviços internos do Windows.</span><span class="sxs-lookup"><span data-stu-id="97a1b-107">An example of a service program that does this is the generic service host process, Svchost.exe, which hosts internal Windows services.</span></span> <span data-ttu-id="97a1b-108">Observe que Svchost.exe é reservado para uso pelo sistema operacional e não deve ser usado por serviços que não sejam do Windows.</span><span class="sxs-lookup"><span data-stu-id="97a1b-108">Note that Svchost.exe is reserved for use by the operating system and should not be used by non-Windows services.</span></span> <span data-ttu-id="97a1b-109">Em vez disso, os desenvolvedores devem implementar seus próprios programas de Hospedagem de serviços.</span><span class="sxs-lookup"><span data-stu-id="97a1b-109">Instead, developers should implement their own service hosting programs.</span></span>

<span data-ttu-id="97a1b-110">Um programa de serviço pode ser configurado para ser executado no contexto de uma conta de usuário tanto do domínio interno (local), primário ou confiável.</span><span class="sxs-lookup"><span data-stu-id="97a1b-110">A service program can be configured to execute in the context of a user account from either the built-in (local), primary, or trusted domain.</span></span> <span data-ttu-id="97a1b-111">Ele também pode ser configurado para ser executado em uma [conta de usuário de serviço](service-user-accounts.md)especial.</span><span class="sxs-lookup"><span data-stu-id="97a1b-111">It can also be configured to run in a special [service user account](service-user-accounts.md).</span></span>

<span data-ttu-id="97a1b-112">Os tópicos a seguir descrevem os requisitos de interface do SCM ( [Gerenciador de controle de serviço](service-control-manager.md) ) que um programa de serviço deve incluir:</span><span class="sxs-lookup"><span data-stu-id="97a1b-112">The following topics describe the interface requirements of the [service control manager](service-control-manager.md) (SCM) that a service program must include:</span></span>

-   [<span data-ttu-id="97a1b-113">Ponto de entrada de serviço</span><span class="sxs-lookup"><span data-stu-id="97a1b-113">Service Entry Point</span></span>](service-entry-point.md)
-   [<span data-ttu-id="97a1b-114">Função Service-Main</span><span class="sxs-lookup"><span data-stu-id="97a1b-114">Service ServiceMain Function</span></span>](service-servicemain-function.md)
-   [<span data-ttu-id="97a1b-115">Função do manipulador do controle de serviço</span><span class="sxs-lookup"><span data-stu-id="97a1b-115">Service Control Handler Function</span></span>](service-control-handler-function.md)

<span data-ttu-id="97a1b-116">Esses tópicos não se aplicam aos serviços de driver.</span><span class="sxs-lookup"><span data-stu-id="97a1b-116">These topics do not apply to driver services.</span></span> <span data-ttu-id="97a1b-117">Para obter os requisitos de interface dos serviços de driver, consulte o WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="97a1b-117">For interface requirements of driver services, see the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="97a1b-118">Um serviço é executado como um processo em segundo plano que pode afetar o desempenho do sistema, a capacidade de resposta, a eficiência de energia e a segurança.</span><span class="sxs-lookup"><span data-stu-id="97a1b-118">A service runs as a background process that can affect system performance, responsiveness, energy efficiency, and security.</span></span> <span data-ttu-id="97a1b-119">Para obter diretrizes de otimização de serviço, consulte [desenvolvendo processos em segundo plano eficientes para o Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span><span class="sxs-lookup"><span data-stu-id="97a1b-119">For service optimization guidelines, see [Developing Efficient Background Processes for Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span></span> <span data-ttu-id="97a1b-120">Os tópicos a seguir descrevem considerações de programação adicionais:</span><span class="sxs-lookup"><span data-stu-id="97a1b-120">The following topics describe additional programming considerations:</span></span>

-   [<span data-ttu-id="97a1b-121">Transições de estado do serviço</span><span class="sxs-lookup"><span data-stu-id="97a1b-121">Service State Transitions</span></span>](service-status-transitions.md)
-   [<span data-ttu-id="97a1b-122">Recebendo eventos em um serviço</span><span class="sxs-lookup"><span data-stu-id="97a1b-122">Receiving Events in a Service</span></span>](receiving-events-in-a-service.md)
-   [<span data-ttu-id="97a1b-123">Serviços multithread</span><span class="sxs-lookup"><span data-stu-id="97a1b-123">Multithreaded Services</span></span>](multithreaded-services.md)
-   [<span data-ttu-id="97a1b-124">Serviços e o registro</span><span class="sxs-lookup"><span data-stu-id="97a1b-124">Services and the Registry</span></span>](services-and-the-registry.md)
-   [<span data-ttu-id="97a1b-125">Serviços e unidades redirecionadas</span><span class="sxs-lookup"><span data-stu-id="97a1b-125">Services and Redirected Drives</span></span>](services-and-redirected-drives.md)
-   [<span data-ttu-id="97a1b-126">Eventos de gatilho de serviço</span><span class="sxs-lookup"><span data-stu-id="97a1b-126">Service Trigger Events</span></span>](service-trigger-events.md)

<span data-ttu-id="97a1b-127">Observe que, se o programa de serviço funcionar como um servidor RPC, ele deverá usar pontos de extremidade dinâmicos e autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="97a1b-127">Note that if the service program functions as an RPC server, it should use dynamic endpoints and mutual authentication.</span></span>

 

 
