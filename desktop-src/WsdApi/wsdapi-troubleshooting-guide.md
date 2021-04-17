---
description: A finalidade deste guia é ajudar os usuários a solucionar problemas de falhas encontradas ao usar APIs de descoberta do WSDAPI, ao criar um host ou proxy de dispositivo do WSDAPI, ou ao usar funções do sistema operacional (como a descoberta de função ou o Gerenciador de rede) que dependem de WSDAPI.
ms.assetid: fc01fc66-627a-497f-98dd-613f5d85f6cb
title: Guia de solução de problemas de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c28e9a1fe4cc5b24b386cfb88e39276edc14cb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749502"
---
# <a name="wsdapi-troubleshooting-guide"></a>Guia de solução de problemas de WSDAPI

A finalidade deste guia é ajudar os usuários a solucionar problemas de falhas encontradas ao usar APIs de descoberta do WSDAPI, ao criar um host ou proxy de dispositivo do WSDAPI, ou ao usar funções do sistema operacional (como a [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) ou o Gerenciador de rede) que dependem de WSDAPI. O objetivo principal é ajudar a solucionar problemas quando um cliente e um host não puderem ver uns aos outros na rede.

Para usuários do WSDAPI, este guia contém informações que ajudarão você a solucionar com êxito um proxy de dispositivo (usando o [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)), um provedor de descoberta (usando o [**WSDCreateDiscoveryProvider**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoveryprovider)) ou um Publicador de descoberta (usando [**WSDCreateDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoverypublisher)).

Este guia pressupõe que o cliente e o host possam interoperar corretamente com o WSDAPI em um ambiente controlado. Da mesma forma, este guia não se destina a ajudar a solucionar problemas de pilhas do DPWS que podem estar gerando mensagens WS inadequadas. Para obter informações sobre como testar a interoperabilidade com o WSDAPI, consulte a [ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) no Windows Driver Kit (WDK).

Antes de começar a solucionar problemas de seu aplicativo, você deve se familiarizar com os [padrões de mensagem de troca de metadados e descoberta](discovery-and-metadata-exchange-message-patterns.md).

Este guia contém as seções a seguir.

-   [Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
-   [Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
