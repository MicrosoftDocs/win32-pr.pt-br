---
title: Localizar dispositivos
description: A arquitetura UPnP é uma arquitetura de rede dinâmica que permite aos dispositivos ingressar e sair da rede a qualquer momento.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccf5626f7d941d9e3fa73b6d3d46ef9f51ef256ee8371e7594c312d225bba865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867586"
---
# <a name="finding-devices"></a>Localizar dispositivos

A arquitetura UPnP é uma arquitetura de rede dinâmica que permite aos dispositivos ingressar e sair da rede a qualquer momento. Devido a essa arquitetura dinâmica, os aplicativos não podem depender de dispositivos específicos baseados em UPnP para que eles sejam disponibilizados em um determinado momento. Por esse motivo, os aplicativos (ou pontos de controle) pesquisam a rede para encontrar dispositivos que mais corresponderem aos critérios especificados. Os aplicativos também aguardam mensagens de anúncio do dispositivo que indicam que novos dispositivos foram adicionados à rede.

A seguir estão os critérios de pesquisa válidos para dispositivos baseados em UPnP:

-   Tipo de dispositivo
-   Tipo de serviço
-   Nome exclusivo do dispositivo (UDN)
-   Todos os dispositivos raiz

O tipo de dispositivo e as pesquisas de tipo de serviço normalmente são usados para encontrar uma classe de dispositivos com características comuns. A pesquisa de UDN é usada para encontrar um dispositivo específico.

Para pesquisar dispositivos, um aplicativo deve primeiro insinuar o objeto Device Finder. Esse objeto expõe a interface [**IUPnPDevice Ltda.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) seus métodos executam as pesquisas descritas anteriormente.

As seções a seguir descrevem o processo de localizar dispositivos:

-   [Criando o Device Finder](creating-the-device-finder.md)
-   [Pesquisa assíncrona](asynchronous-searching.md)
-   [Pesquisa síncrona](synchronous-searching.md)
-   [Coleções de dispositivos retornadas por pesquisas síncronas](device-collections-returned-by-synchronous-searches.md)

 

 




