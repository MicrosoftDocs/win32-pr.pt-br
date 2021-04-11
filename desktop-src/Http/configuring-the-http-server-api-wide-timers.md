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
# <a name="configuring-the-http-server-api-wide-timers"></a>Configurando os timers de longa duração da API do servidor HTTP

Os temporizadores **HeaderWait** e **IdleConnection** de toda a API do servidor http são configurados chamando a função [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) da versão 1,0. O parâmetro *configid* é definido como **HttpServiceConfigTimeout** e o parâmetro *pConfigInformation* especifica a estrutura do [**\_ \_ \_ \_ conjunto de tempo limite da configuração do serviço http**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) que contém o timer definido e o valor do temporizador.

Configurar os tempos limite de toda a API do servidor HTTP requer privilégios administrativos, no entanto, consultá-los não. Essas configurações são definidas para todos os aplicativos no computador e elas são mantidas quando o serviço HTTP é reiniciado ou quando o computador é reiniciado. Para consultar os tempos limite de toda a API do servidor HTTP existentes, o aplicativo chama [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).

 

 




