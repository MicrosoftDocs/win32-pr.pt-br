---
title: Configurando os timers de longa duração da API do servidor HTTP
description: Configurando os timers de longa duração da API do servidor HTTP
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae91abb1c89419e99fa13273cd55b0783df3906a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159853"
---
# <a name="configuring-the-http-server-api-wide-timers"></a><span data-ttu-id="ab08f-103">Configurando os timers de longa duração da API do servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="ab08f-103">Configuring the HTTP Server API Wide Timers</span></span>

<span data-ttu-id="ab08f-104">Os temporizadores **HeaderWait** e **IdleConnection** de toda a API do servidor http são configurados chamando a função [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) da versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="ab08f-104">The HTTP Server API-wide **HeaderWait** and **IdleConnection** timers are configured by calling the version 1.0 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function.</span></span> <span data-ttu-id="ab08f-105">O parâmetro *configid* é definido como **HttpServiceConfigTimeout** e o parâmetro *pConfigInformation* especifica a estrutura do [**\_ \_ \_ \_ conjunto de tempo limite da configuração do serviço http**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) que contém o timer definido e o valor do temporizador.</span><span class="sxs-lookup"><span data-stu-id="ab08f-105">The *ConfigId* parameter is set to **HttpServiceConfigTimeout** and the *pConfigInformation* parameter specifies the [**HTTP\_SERVICE\_CONFIG\_TIMEOUT\_SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) structure that contains the timer that is set and the value for the timer.</span></span>

<span data-ttu-id="ab08f-106">Configurar os tempos limite de toda a API do servidor HTTP requer privilégios administrativos, no entanto, consultá-los não.</span><span class="sxs-lookup"><span data-stu-id="ab08f-106">Configuring the HTTP Server API-wide timeouts requires administrative privileges, however querying them does not.</span></span> <span data-ttu-id="ab08f-107">Essas configurações são definidas para todos os aplicativos no computador e elas são mantidas quando o serviço HTTP é reiniciado ou quando o computador é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="ab08f-107">These configurations are set for all applications on the computer and they persist when the HTTP service is restarted or the computer is restarted.</span></span> <span data-ttu-id="ab08f-108">Para consultar os tempos limite de toda a API do servidor HTTP existentes, o aplicativo chama [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).</span><span class="sxs-lookup"><span data-stu-id="ab08f-108">To query existing HTTP Server API-wide timeouts, the application calls [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).</span></span>

 

 




