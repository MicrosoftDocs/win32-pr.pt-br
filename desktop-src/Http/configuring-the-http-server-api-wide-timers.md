---
title: Configurando os temporizadores largos da API do servidor HTTP
description: Configurando os temporizadores largos da API do servidor HTTP
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0eb5fc40bedd51884830893673b3bae2341a21110fa2c3b33878dba7a4aef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047346"
---
# <a name="configuring-the-http-server-api-wide-timers"></a>Configurando os temporizadores largos da API do servidor HTTP

Os temporizadores **HeaderWait** e **IdleConnection** em todo o SERVIDOR HTTP Server são configurados chamando a função [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) versão 1.0. O parâmetro *ConfigId* é definido como **HttpServiceConfigTimeout** e o parâmetro *pConfigInformation* especifica a estrutura [**HTTP SERVICE \_ \_ CONFIG \_ TIMEOUT \_ SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) que contém o temporizador definido e o valor do temporizador.

A configuração de tempos-tempoouts em toda a API do servidor HTTP requer privilégios administrativos, no entanto, a consulta deles não exige. Essas configurações são definidas para todos os aplicativos no computador e persistem quando o serviço HTTP é reiniciado ou o computador é reiniciado. Para consultar temposouts existentes em toda a API do Servidor HTTP, o aplicativo [**chama HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).

 

 




