---
title: Acessando o armazenamento de reserva
description: A API do servidor HTTP mantém a lista de reserva de namespace para todos os usuários no computador.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Acessando o armazenamento de reserva HTTP
- Armazenamento de reserva HTTP, acessando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a138a0a2385e6338877e5e8623527a64a6eca796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364012"
---
# <a name="accessing-the-reservation-store"></a><span data-ttu-id="85409-105">Acessando o armazenamento de reserva</span><span class="sxs-lookup"><span data-stu-id="85409-105">Accessing the Reservation Store</span></span>

<span data-ttu-id="85409-106">A API do servidor HTTP mantém a lista de reserva de namespace para todos os usuários no computador.</span><span class="sxs-lookup"><span data-stu-id="85409-106">The HTTP Server API maintains the namespace reservation list for all users on the computer.</span></span> <span data-ttu-id="85409-107">Uma entrada de reserva consiste em um [URLPrefix](urlprefix-strings.md) e uma ACL correspondente.</span><span class="sxs-lookup"><span data-stu-id="85409-107">A reservation entry consists of a [UrlPrefix](urlprefix-strings.md) and corresponding ACL.</span></span> <span data-ttu-id="85409-108">Cada UrlPrefix no repositório tem uma ACL que lista todos os usuários que têm permissão para se registrar para receber solicitações para o namespace.</span><span class="sxs-lookup"><span data-stu-id="85409-108">Each UrlPrefix in the store has an ACL that lists all the users that are permitted to register to receive requests for the namespace.</span></span> <span data-ttu-id="85409-109">Os usuários com privilégios de delegação podem delegar subárvores do namespace que eles possuem a outros usuários ou excluir reservas existentes usando as APIs de configuração.</span><span class="sxs-lookup"><span data-stu-id="85409-109">Users with delegation privileges can delegate subtrees of the namespace that they own to other users or delete existing reservations using the configuration APIs.</span></span>

<span data-ttu-id="85409-110">Para adicionar uma reserva ao repositório de reserva persistente, o aplicativo chama a função [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) com o parâmetro de ID de configuração definido como o valor **HttpServiceConfigUrlAclInfo** .</span><span class="sxs-lookup"><span data-stu-id="85409-110">To add a reservation to the persistent reservation store, the application calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value.</span></span> <span data-ttu-id="85409-111">A API do servidor HTTP verifica a propriedade do namespace e a ID do usuário antes de adicionar uma reserva à loja.</span><span class="sxs-lookup"><span data-stu-id="85409-111">The HTTP Server API verifies the ownership of the namespace and the user ID before adding a reservation to the store.</span></span>

<span data-ttu-id="85409-112">A API do servidor HTTP também fornece funções para consultar e excluir as configurações de serviço para namespaces de URL.</span><span class="sxs-lookup"><span data-stu-id="85409-112">The HTTP Server API also supplies functions to query and delete the Service configurations for URL namespaces.</span></span> <span data-ttu-id="85409-113">A função [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) chamada com o parâmetro de ID de configuração definido como as consultas de valor de **HttpServiceConfigUrlAclInfo** e a função [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) exclui no repositório de namespace de URL.</span><span class="sxs-lookup"><span data-stu-id="85409-113">The [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) function called with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value queries, and the [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) function deletes on the URL namespace store.</span></span>

 

 




