---
title: Visão geral da arquitetura dos serviços de enfileiramento de mensagens
description: O MSMQ (serviços de enfileiramento de mensagens) usa um modelo de site/empresa. Normalmente, um site é um local físico, como um edifício. Uma empresa consiste em um ou mais sites e representa uma organização.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292531"
---
# <a name="overview-of-message-queuing-services-architecture"></a><span data-ttu-id="9571e-105">Visão geral da arquitetura dos serviços de enfileiramento de mensagens</span><span class="sxs-lookup"><span data-stu-id="9571e-105">Overview of Message Queuing Services Architecture</span></span>

<span data-ttu-id="9571e-106">O MSMQ (serviços de enfileiramento de mensagens) usa um modelo de site/empresa.</span><span class="sxs-lookup"><span data-stu-id="9571e-106">Message Queuing Services (MSMQ) uses a site/enterprise model.</span></span> <span data-ttu-id="9571e-107">Normalmente, um site é um local físico, como um edifício.</span><span class="sxs-lookup"><span data-stu-id="9571e-107">Typically, a site is a physical location, such as a building.</span></span> <span data-ttu-id="9571e-108">Uma empresa consiste em um ou mais sites e representa uma organização.</span><span class="sxs-lookup"><span data-stu-id="9571e-108">An enterprise consists of one or more sites and represents an organization.</span></span>

<span data-ttu-id="9571e-109">O diagrama a seguir ilustra a arquitetura do serviço MSMQ.</span><span class="sxs-lookup"><span data-stu-id="9571e-109">The following diagram illustrates the architecture of the MSMQ Service.</span></span>

![arquitetura do MSMQ](images/msmq.png)

<span data-ttu-id="9571e-111">No coração do MSMQ está o banco de dados do serviço de informações de fila de mensagens (MQIS), que é executado sobre SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9571e-111">At the heart of MSMQ is the Message Queue Information Service (MQIS) database, which runs on top of SQL Server.</span></span> <span data-ttu-id="9571e-112">Uma empresa tem um único MQIS mestre, chamado de controlador corporativo primário.</span><span class="sxs-lookup"><span data-stu-id="9571e-112">An enterprise has a single master MQIS, called the Primary Enterprise Controller.</span></span> <span data-ttu-id="9571e-113">Cada site tem seu próprio MQIS, chamado de *controlador de site primário* e zero ou mais *controladores de site de backup*.</span><span class="sxs-lookup"><span data-stu-id="9571e-113">Each site has its own MQIS, called a *primary site controller* and zero or more *backup site controllers*.</span></span> <span data-ttu-id="9571e-114">Por fim, há os computadores cliente individuais, cada um com seu próprio Gerenciador de filas, implementado como um serviço.</span><span class="sxs-lookup"><span data-stu-id="9571e-114">Finally, there are the individual client computers, each of which has its own queue manager, implemented as a service.</span></span> <span data-ttu-id="9571e-115">O controlador corporativo primário também pode ser um controlador de site primário e qualquer controlador também pode ser um cliente.</span><span class="sxs-lookup"><span data-stu-id="9571e-115">The Primary Enterprise Controller can also be a Primary Site Controller, and any controller can also be a client.</span></span>

<span data-ttu-id="9571e-116">As filas de mensagens podem ser públicas ou privadas.</span><span class="sxs-lookup"><span data-stu-id="9571e-116">Message queues can be either public or private.</span></span> <span data-ttu-id="9571e-117">As filas públicas são registradas em Active Directory e podem ser acessadas pela rede.</span><span class="sxs-lookup"><span data-stu-id="9571e-117">Public queues are registered in Active Directory and are accessible across the network.</span></span> <span data-ttu-id="9571e-118">As mensagens em uma fila pública são roteadas em toda a empresa, sob o controle do MSMQ.</span><span class="sxs-lookup"><span data-stu-id="9571e-118">Messages in a public queue are routed throughout the enterprise, under the control of MSMQ.</span></span> <span data-ttu-id="9571e-119">As mensagens do aplicativo cliente são movidas do Gerenciador de filas do cliente para a fila de destino viajando entre os gerenciadores de filas dos controladores de site.</span><span class="sxs-lookup"><span data-stu-id="9571e-119">Client application messages move from the client's queue manager to the destination queue by traveling between the queue managers of the site controllers.</span></span>

<span data-ttu-id="9571e-120">As filas particulares são mantidas pelo Gerenciador de filas local e não são registradas no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9571e-120">Private queues are maintained by the local queue manager and are not registered in Active Directory.</span></span> <span data-ttu-id="9571e-121">O escopo de mensagens de fila particular é limitado ao computador no qual residem.</span><span class="sxs-lookup"><span data-stu-id="9571e-121">The scope of private queue messages is limited to the computer on which they reside.</span></span>

 

 




