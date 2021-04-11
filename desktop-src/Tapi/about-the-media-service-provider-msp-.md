---
description: Um MSP (provedor de serviços de mídia) da TAPI 3 permite um controle considerável do aplicativo sobre a mídia para um mecanismo de transporte específico.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: Sobre o MSP (provedor de serviços de mídia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef4d19a2f01c047d5fc2afd4a0323d7908fcac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091873"
---
# <a name="about-the-media-service-provider-msp"></a>Sobre o MSP (provedor de serviços de mídia)

Um MSP (provedor de serviços de mídia) da TAPI 3 permite um controle considerável do aplicativo sobre a mídia para um mecanismo de transporte específico. Um MSP sempre existe emparelhado com um provedor de serviços de telefonia (TSP). Assim como um TSP é uma camada de abstração para o controle de chamada, o MSP controla a mídia sem a necessidade de codificação específica do dispositivo. Para obter um exemplo de comunicação MSP/TSP, consulte [visão geral do provedor de serviços TAPI](./tapi-service-provider-overview.md).

Um MSP permite o controle de mídia por meio do uso de interfaces especiais de terminal, Stream e substream definidas pela TAPI. O diagrama em [sobre controles de mídia e de chamada](about-call-and-media-controls.md) ilustra como essas interfaces aparecem para um aplicativo TAPI 3.

Além disso, um MSP pode implementar [interfaces específicas de provedor](provider-specific-interfaces.md)privada, que a TAPI agregará aos objetos padrão expostos a um aplicativo. Por exemplo, o Microsoft IPConf MSP, que é instalado com o Microsoft Windows 2000, implementa a interface [**ITParticipant**](itparticipant.md) , que fornece controles para membros individuais de uma conferência.

O tópico a seguir descreve brevemente o MSPs que pode ser instalado com um sistema operacional da Microsoft. Para obter detalhes sobre a configuração e o uso, consulte o kit de recursos para a plataforma de destino.

Provedores de serviço de mídia de terceiros adicionais podem ser gravados para protocolos específicos ou para dispositivos físicos. A [MSPI (interface do provedor de serviços de mídia)](media-service-provider-interface-mspi-.md) descreve as interfaces que devem ser implementadas para permitir que um MSP interaja com os componentes da telefonia da Microsoft.

 

 
