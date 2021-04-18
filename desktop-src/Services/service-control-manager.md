---
description: O SCM (Gerenciador de controle de serviço) é iniciado na inicialização do sistema. É um servidor RPC (chamada de procedimento remoto), para que os programas de configuração de serviço e de controle de serviço possam manipular serviços em máquinas remotas.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Gerenciador de Controle de Serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771810"
---
# <a name="service-control-manager"></a><span data-ttu-id="fe198-104">Gerenciador de Controle de Serviço</span><span class="sxs-lookup"><span data-stu-id="fe198-104">Service Control Manager</span></span>

<span data-ttu-id="fe198-105">O SCM (Gerenciador de controle de serviço) é iniciado na inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="fe198-105">The service control manager (SCM) is started at system boot.</span></span> <span data-ttu-id="fe198-106">É um servidor RPC (chamada de procedimento remoto), para que os programas de configuração de serviço e de controle de serviço possam manipular serviços em máquinas remotas.</span><span class="sxs-lookup"><span data-stu-id="fe198-106">It is a remote procedure call (RPC) server, so that service configuration and service control programs can manipulate services on remote machines.</span></span>

<span data-ttu-id="fe198-107">As funções de serviço fornecem uma interface para as seguintes tarefas executadas pelo SCM:</span><span class="sxs-lookup"><span data-stu-id="fe198-107">The service functions provide an interface for the following tasks performed by the SCM:</span></span>

-   <span data-ttu-id="fe198-108">Manutenção do banco de dados dos serviços instalados.</span><span class="sxs-lookup"><span data-stu-id="fe198-108">Maintaining the database of installed services.</span></span>
-   <span data-ttu-id="fe198-109">Inicialização de serviços e serviços de driver na inicialização do sistema ou sob demanda.</span><span class="sxs-lookup"><span data-stu-id="fe198-109">Starting services and driver services either upon system startup or upon demand.</span></span>
-   <span data-ttu-id="fe198-110">Enumerando serviços instalados e serviços de driver.</span><span class="sxs-lookup"><span data-stu-id="fe198-110">Enumerating installed services and driver services.</span></span>
-   <span data-ttu-id="fe198-111">Manutenção de informações de status para a execução de serviços e serviços de driver.</span><span class="sxs-lookup"><span data-stu-id="fe198-111">Maintaining status information for running services and driver services.</span></span>
-   <span data-ttu-id="fe198-112">Transmissão de solicitações de controle para a execução de serviços.</span><span class="sxs-lookup"><span data-stu-id="fe198-112">Transmitting control requests to running services.</span></span>
-   <span data-ttu-id="fe198-113">Bloqueando e desbloqueando o banco de dados de serviço.</span><span class="sxs-lookup"><span data-stu-id="fe198-113">Locking and unlocking the service database.</span></span>

<span data-ttu-id="fe198-114">As seções a seguir descrevem o SCM mais detalhadamente:</span><span class="sxs-lookup"><span data-stu-id="fe198-114">The following sections describe the SCM in more detail:</span></span>

-   [<span data-ttu-id="fe198-115">Banco de dados dos serviços instalados</span><span class="sxs-lookup"><span data-stu-id="fe198-115">Database of Installed Services</span></span>](database-of-installed-services.md)
-   [<span data-ttu-id="fe198-116">Iniciando serviços automaticamente</span><span class="sxs-lookup"><span data-stu-id="fe198-116">Automatically Starting Services</span></span>](automatically-starting-services.md)
-   [<span data-ttu-id="fe198-117">Iniciando serviços sob demanda</span><span class="sxs-lookup"><span data-stu-id="fe198-117">Starting Services on Demand</span></span>](starting-services-on-demand.md)
-   [<span data-ttu-id="fe198-118">Lista de registros de serviço</span><span class="sxs-lookup"><span data-stu-id="fe198-118">Service Record List</span></span>](service-record-list.md)
-   [<span data-ttu-id="fe198-119">Identificadores SCM</span><span class="sxs-lookup"><span data-stu-id="fe198-119">SCM Handles</span></span>](scm-handles.md)

 

 



