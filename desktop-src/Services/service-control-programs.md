---
description: Um programa de controle de serviço inicia e controla os serviços.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Programas de controle de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b34232f5f87d84bdf30acd51f57afbf79a8385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827021"
---
# <a name="service-control-programs"></a><span data-ttu-id="eb78b-103">Programas de controle de serviço</span><span class="sxs-lookup"><span data-stu-id="eb78b-103">Service Control Programs</span></span>

<span data-ttu-id="eb78b-104">Um programa de controle de serviço inicia e controla os serviços.</span><span class="sxs-lookup"><span data-stu-id="eb78b-104">A service control program starts and controls services.</span></span> <span data-ttu-id="eb78b-105">Ele executa as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="eb78b-105">It performs the following actions:</span></span>

-   <span data-ttu-id="eb78b-106">Inicia um serviço de serviço ou de driver se o tipo de inicialização for início da demanda de serviço \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="eb78b-106">Starts a service or driver service, if the start type is SERVICE\_DEMAND\_START.</span></span>
-   <span data-ttu-id="eb78b-107">Envia solicitações de controle para um serviço em execução.</span><span class="sxs-lookup"><span data-stu-id="eb78b-107">Sends control requests to a running service.</span></span>
-   <span data-ttu-id="eb78b-108">Consulta o status atual de um serviço em execução.</span><span class="sxs-lookup"><span data-stu-id="eb78b-108">Queries the current status of a running service.</span></span>

<span data-ttu-id="eb78b-109">Essas ações exigem um identificador aberto para o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="eb78b-109">These actions require an open handle to the service object.</span></span> <span data-ttu-id="eb78b-110">Para obter o identificador, o programa de controle de serviço deve:</span><span class="sxs-lookup"><span data-stu-id="eb78b-110">To obtain the handle, the service control program must:</span></span>

1.  <span data-ttu-id="eb78b-111">Use a função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para obter um identificador para o banco de dados SCM em um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="eb78b-111">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="eb78b-112">Use a função [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) ou [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para obter um identificador para o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="eb78b-112">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="eb78b-113">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="eb78b-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="eb78b-114">Inicialização do serviço</span><span class="sxs-lookup"><span data-stu-id="eb78b-114">Service Startup</span></span>](service-startup.md)
-   [<span data-ttu-id="eb78b-115">Solicitações de controle de serviço</span><span class="sxs-lookup"><span data-stu-id="eb78b-115">Service Control Requests</span></span>](service-control-requests.md)
-   [<span data-ttu-id="eb78b-116">Controlando um serviço usando SC</span><span class="sxs-lookup"><span data-stu-id="eb78b-116">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)

 

 



