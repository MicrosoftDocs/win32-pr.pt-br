---
title: Lista de escuta de IP
description: As APIs do servidor HTTP não se associam a nenhum endereço IP e a pares de portas TCP até que um usuário registre um UrlPrefix.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916596"
---
# <a name="ip-listen-list"></a><span data-ttu-id="57c62-103">Lista de escuta de IP</span><span class="sxs-lookup"><span data-stu-id="57c62-103">IP Listen List</span></span>

<span data-ttu-id="57c62-104">As APIs do servidor HTTP não se associam a nenhum endereço IP e a pares de portas TCP até que um usuário registre um UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="57c62-104">The HTTP Server APIs do not bind to any IP address and TCP port pairs until a user registers a UrlPrefix.</span></span> <span data-ttu-id="57c62-105">Por padrão, depois que um registro é inserido na fila de solicitações, a API do servidor HTTP é vinculada à porta especificada no UrlPrefix (por exemplo, a porta 80) para todos os endereços IP (inaddr \_ any ou INADDR6 \_ any) disponíveis no computador.</span><span class="sxs-lookup"><span data-stu-id="57c62-105">By default, once a registration is entered in the request queue, the HTTP Server API binds to the port specified in the UrlPrefix (for example port 80) for all IP addresses (INADDR\_ANY or INADDR6\_ANY) available on the machine.</span></span> <span data-ttu-id="57c62-106">Os problemas surgem quando os aplicativos de terceiros (não usando as APIs do servidor HTTP) são vinculados ao endereço IP e aos pares da porta 80 no computador.</span><span class="sxs-lookup"><span data-stu-id="57c62-106">Problems arise when third party applications (not using the HTTP Server APIs) bind to IP address and port 80 pairs on the machine.</span></span> <span data-ttu-id="57c62-107">A API do servidor HTTP fornece uma maneira de configurar a lista de endereços IP que ele associa e resolve esse problema de coexistência.</span><span class="sxs-lookup"><span data-stu-id="57c62-107">The HTTP Server API provides a way to configure the list of IP addresses that it binds and solves this coexistence issue.</span></span> <span data-ttu-id="57c62-108">O administrador do sistema chama a função [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) com o parâmetro *configid* definido como o valor HttpServiceConfigIPListenList para especificar a lista de escuta de IP.</span><span class="sxs-lookup"><span data-stu-id="57c62-108">The system administrator calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the *ConfigId* parameter set to the HttpServiceConfigIPListenList value to specify the IP listen list.</span></span> <span data-ttu-id="57c62-109">Os endereços IPv4 e IPv6 podem ser adicionados à lista.</span><span class="sxs-lookup"><span data-stu-id="57c62-109">Both IPv4 and IPv6 addresses can be added to the list.</span></span> <span data-ttu-id="57c62-110">Os endereços IP inseridos se aplicam a todos os aplicativos no computador usando a API do servidor HTTP e persistem entre reinicializações do computador.</span><span class="sxs-lookup"><span data-stu-id="57c62-110">The IP addresses entered apply to all applications on the machine using the HTTP Server API and persist across reboots of the machine.</span></span> <span data-ttu-id="57c62-111">No entanto, quaisquer alterações na configuração da lista de escuta de IP não ocorrem dinamicamente; na maioria dos casos, uma reinicialização do sistema pode ser necessária.</span><span class="sxs-lookup"><span data-stu-id="57c62-111">However, any changes to the IP listen list configuration do not take place dynamically; in most cases, a system reboot may be necessary.</span></span>

 

 




