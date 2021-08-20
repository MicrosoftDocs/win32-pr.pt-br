---
description: Um provedor de serviços de telefonia TAPI (TSP) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: Sobre o provedor de serviços de telefonia (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab5f7d1d1631c1146bfb06223fa722bf27daa5cd6ec8e3f4f4b83d1d23c5554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949263"
---
# <a name="about-the-telephony-service-provider-tsp"></a>Sobre o provedor de serviços de telefonia (TSP)

\[o H323 e o IPConf TSPs não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

Um provedor de serviços de telefonia TAPI (TSP) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas. Um aplicativo TAPI usa comandos padronizados, a TAPI passa na formação de informações para o provedor de serviços de telefonia e o TSP lida com os comandos específicos que devem ser trocados pelo dispositivo.

As seções a seguir descrevem brevemente o TSPs fornecido com o Microsoft Windows:

-   [H323 TSP](h323-tsp.md)
-   [IPConf TSP](ipconf-tsp.md)
-   [Driver de dispositivo no modo kernel TSP](kernel-mode-device-driver-tsp.md)
-   [TSP do proxy NDIS](ndis-proxy-tsp.md)
-   [TSP remoto](remote-tsp.md)
-   [TSP de terceiros](third-party-tsp.md)
-   [Unimodem TSP](unimodem-tsp.md)

Para obter informações detalhadas, consulte o kit de recursos para o sistema operacional de destino. Os TSPs de terceiros para dispositivos de comunicação especializados normalmente serão fornecidos pelo fabricante e serão instalados com o dispositivo.

Os tópicos a seguir descrevem como criar um TSP que funcionará corretamente dentro do ambiente de telefonia da Microsoft e como criar um par de TSP/MSP:

-   [Interface do provedor de serviços de telefonia (TSPI)](telephony-service-provider-interface-tspi-.md)
-   [Referência de TSPI](tspi-reference.md)
-   [Provedores de serviços de mídia](./media-service-providers-start-page.md)

> [!Note]  
> Um TSP é uma DLL criada pelo usuário. se você estiver criando um TSP para uma plataforma de Windows de 64 bits, deverá compilá-lo como uma DLL ou DLLs de 64 bits.

 

 

 
