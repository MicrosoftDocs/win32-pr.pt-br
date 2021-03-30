---
description: Um provedor de serviços de telefonia TAPI (TSP) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: Sobre o provedor de serviços de telefonia (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646972"
---
# <a name="about-the-telephony-service-provider-tsp"></a>Sobre o provedor de serviços de telefonia (TSP)

\[ O H323 e o IPConf TSPs não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

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
> Um TSP é uma DLL criada pelo usuário. Se você estiver criando um TSP para uma plataforma do Windows de 64 bits, deverá compilá-lo como uma DLL ou DLLs de 64 bits.

 

 

 
