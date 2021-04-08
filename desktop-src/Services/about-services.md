---
description: O SCM (Gerenciador de controle de serviços) mantém um banco de dados de serviços e serviços de driver instalados e fornece meios unificados e seguros de controlá-los.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: Sobre serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922098"
---
# <a name="about-services"></a><span data-ttu-id="322e0-103">Sobre serviços</span><span class="sxs-lookup"><span data-stu-id="322e0-103">About Services</span></span>

<span data-ttu-id="322e0-104">O SCM ( [Gerenciador de controle de serviços](service-control-manager.md) ) mantém um banco de dados de serviços e serviços de driver instalados e fornece meios unificados e seguros de controlá-los.</span><span class="sxs-lookup"><span data-stu-id="322e0-104">The [service control manager](service-control-manager.md) (SCM) maintains a database of installed services and driver services, and provides a unified and secure means of controlling them.</span></span> <span data-ttu-id="322e0-105">O banco de dados inclui informações sobre como cada serviço de serviço ou de driver deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="322e0-105">The database includes information on how each service or driver service should be started.</span></span> <span data-ttu-id="322e0-106">Ele também permite que os administradores de sistema personalizem os requisitos de segurança para cada serviço e, portanto, controlem o acesso ao serviço.</span><span class="sxs-lookup"><span data-stu-id="322e0-106">It also enables system administrators to customize security requirements for each service and thereby control access to the service.</span></span>

<span data-ttu-id="322e0-107">Os tipos de programas a seguir usam as funções fornecidas pelo SCM.</span><span class="sxs-lookup"><span data-stu-id="322e0-107">The following types of programs use the functions provided by the SCM.</span></span>



| <span data-ttu-id="322e0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="322e0-108">Type</span></span>                          | <span data-ttu-id="322e0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="322e0-109">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="322e0-110">Programa de serviço</span><span class="sxs-lookup"><span data-stu-id="322e0-110">Service program</span></span>               | <span data-ttu-id="322e0-111">Um programa que fornece código executável para um ou mais serviços.</span><span class="sxs-lookup"><span data-stu-id="322e0-111">A program that provides executable code for one or more services.</span></span> <span data-ttu-id="322e0-112">Os programas de serviço usam funções que se conectam ao SCM e enviam informações de status para o SCM.</span><span class="sxs-lookup"><span data-stu-id="322e0-112">Service programs use functions that connect to the SCM and send status information to the SCM.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="322e0-113">Programa de configuração de serviço</span><span class="sxs-lookup"><span data-stu-id="322e0-113">Service configuration program</span></span> | <span data-ttu-id="322e0-114">Um programa que consulta ou modifica o banco de dados de serviços.</span><span class="sxs-lookup"><span data-stu-id="322e0-114">A program that queries or modifies the services database.</span></span> <span data-ttu-id="322e0-115">Os programas de configuração de serviço usam funções que abrem o banco de dados, instalam ou excluem serviços no banco de dados e consultam ou modificam os parâmetros de configuração e segurança dos serviços instalados.</span><span class="sxs-lookup"><span data-stu-id="322e0-115">Service configuration programs use functions that open the database, install or delete services in the database, and query or modify the configuration and security parameters for installed services.</span></span> <span data-ttu-id="322e0-116">Os programas de configuração de serviço gerenciam serviços e serviços de driver.</span><span class="sxs-lookup"><span data-stu-id="322e0-116">Service configuration programs manage both services and driver services.</span></span> |
| <span data-ttu-id="322e0-117">Programa de controle de serviço</span><span class="sxs-lookup"><span data-stu-id="322e0-117">Service control program</span></span>       | <span data-ttu-id="322e0-118">Um programa que inicia e controla serviços e serviços de driver.</span><span class="sxs-lookup"><span data-stu-id="322e0-118">A program that starts and controls services and driver services.</span></span> <span data-ttu-id="322e0-119">Os programas de controle de serviço usam funções que enviam solicitações para o SCM, que realiza a solicitação.</span><span class="sxs-lookup"><span data-stu-id="322e0-119">Service control programs use functions that send requests to the SCM, which carries out the request.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="322e0-120">Esta visão geral aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="322e0-120">This overview discusses the following topics:</span></span>

-   [<span data-ttu-id="322e0-121">Gerenciador de Controle de Serviço</span><span class="sxs-lookup"><span data-stu-id="322e0-121">Service Control Manager</span></span>](service-control-manager.md)
-   [<span data-ttu-id="322e0-122">Programas de serviço</span><span class="sxs-lookup"><span data-stu-id="322e0-122">Service Programs</span></span>](service-programs.md)
-   [<span data-ttu-id="322e0-123">Programas de configuração de serviço</span><span class="sxs-lookup"><span data-stu-id="322e0-123">Service Configuration Programs</span></span>](service-configuration-programs.md)
-   [<span data-ttu-id="322e0-124">Programas de controle de serviço</span><span class="sxs-lookup"><span data-stu-id="322e0-124">Service Control Programs</span></span>](service-control-programs.md)
-   [<span data-ttu-id="322e0-125">Contas de usuário de serviço</span><span class="sxs-lookup"><span data-stu-id="322e0-125">Service User Accounts</span></span>](service-user-accounts.md)
-   [<span data-ttu-id="322e0-126">Serviços interativos</span><span class="sxs-lookup"><span data-stu-id="322e0-126">Interactive Services</span></span>](interactive-services.md)
-   [<span data-ttu-id="322e0-127">Segurança do serviço e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="322e0-127">Service Security and Access Rights</span></span>](service-security-and-access-rights.md)
-   [<span data-ttu-id="322e0-128">Depurar um serviço</span><span class="sxs-lookup"><span data-stu-id="322e0-128">Debugging a Service</span></span>](debugging-a-service.md)
-   [<span data-ttu-id="322e0-129">Eventos de gatilho de serviço</span><span class="sxs-lookup"><span data-stu-id="322e0-129">Service Trigger Events</span></span>](service-trigger-events.md)

 

 



