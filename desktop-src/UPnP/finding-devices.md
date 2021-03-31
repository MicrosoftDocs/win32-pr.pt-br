---
title: Localizando dispositivos
description: A arquitetura UPnP é uma arquitetura de rede dinâmica que permite que os dispositivos ingressem e saiam da rede a qualquer momento.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b8feebd430252b118353681a90ce4cd683ee7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005983"
---
# <a name="finding-devices"></a>Localizando dispositivos

A arquitetura UPnP é uma arquitetura de rede dinâmica que permite que os dispositivos ingressem e saiam da rede a qualquer momento. Devido a essa arquitetura dinâmica, os aplicativos não podem depender de dispositivos baseados em UPnP específicos para que estejam disponíveis em um determinado momento. Por esse motivo, os aplicativos (ou pontos de controle) pesquisam a rede para localizar os dispositivos que mais correspondam aos critérios especificados. Os aplicativos também esperam mensagens de anúncio de dispositivo que indicam que novos dispositivos foram adicionados à rede.

Estes são os critérios de pesquisa válidos para dispositivos baseados em UPnP:

-   Tipo de dispositivo
-   Tipo de serviço
-   Nome de dispositivo exclusivo (UDN)
-   Todos os dispositivos raiz

As pesquisas de tipo de dispositivo e de serviço normalmente são usadas para encontrar uma classe de dispositivos com características comuns. A pesquisa UDN é usada para localizar um dispositivo específico.

Para procurar dispositivos, um aplicativo deve primeiro instanciar o objeto do localizador de dispositivos. Esse objeto expõe a interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) ; seus métodos executam as pesquisas descritas anteriormente.

As seções a seguir descrevem o processo de localizar dispositivos:

-   [Criando o localizador de dispositivos](creating-the-device-finder.md)
-   [Pesquisa assíncrona](asynchronous-searching.md)
-   [Pesquisa síncrona](synchronous-searching.md)
-   [Coleções de dispositivos retornadas por pesquisas síncronas](device-collections-returned-by-synchronous-searches.md)

 

 




