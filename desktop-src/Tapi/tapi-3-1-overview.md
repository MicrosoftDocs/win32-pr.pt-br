---
description: A TAPI versão 3,1 é uma API baseada em COM que mescla a telefonia clássica e IP. Os aplicativos possíveis variam de chamadas simples de voz pela PSTN (rede telefônica pública comutada) à conferência de IP de multimídia de multicast com QOS (qualidade de serviço).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Visão geral da TAPI 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779895"
---
# <a name="tapi-31-overview"></a>Visão geral da TAPI 3,1

A TAPI versão 3,1 é uma API baseada em COM que mescla a telefonia clássica e IP. Os aplicativos possíveis variam de chamadas simples de voz pela PSTN (rede telefônica pública comutada) à conferência de IP de multimídia de multicast com QOS (qualidade de serviço).

Para obter informações adicionais sobre os recursos de telefonia IP TAPI 3,1, consulte a "telefonia IP com TAPI 3" white paper, que pode ser encontrada no site da Microsoft.

Há quatro componentes principais para a TAPI 3,1:

-   API COM
-   Servidor TAPI
-   Provedores de serviços de telefonia (TSPs)
-   Provedores de fluxo de mídia (MSPs)

O diagrama a seguir ilustra a arquitetura TAPI 3,1:

![arquitetura TAPI 3](images/callarc-gif-1.png)

A API é implementada como um conjunto de objetos COM (Component Object Model). Mover a TAPI para o modelo COM orientado a objeto permite que os desenvolvedores gravem aplicativos habilitados para TAPI em várias linguagens, como Java, Visual Basic ou C/C++. O uso de COM habilita atualizações de componentes de recursos TAPI.

O processo do servidor TAPI (TAPISRV) abstrai a interface do provedor de serviços TAPI (TSPI) da TAPI 3. x e TAPI 2. x, permitindo que os provedores de serviços de telefonia TAPI 2. x sejam usados com a TAPI 3. x, mantendo o estado interno da TAPI. O TAPISRV é implementado como um processo de serviço no SVCHOST.

[Provedores de serviço](./tapi-service-providers.md) abstratos mecanismos de transporte de mídia específicos do provedor. Eles normalmente existem em pares – um provedor de serviços de telefonia (TSP) para controle de chamada e um provedor de serviços de mídia (MSP) para controle de mídia.

Os TSPs ( [provedores de serviços de telefonia](./telephony-service-providers-start-page.md) ) são responsáveis por resolver o modelo de chamada independente de protocolo da TAPI em mecanismos de controle de chamada específicos de protocolo. A TAPI 3,1 fornece compatibilidade com versões anteriores do TAPI 2,1 TSPs. Dois provedores de serviço de telefonia IP (e seus MSPs associados) são enviados por padrão com TAPI 3,1: o H. 323 TSP e o IP multicast Conferencing TSP.

Os [provedores de serviço de mídia](media-service-providers-start-page.md) (MSPs) fornecem uma maneira uniforme de acessar os fluxos de mídia em uma chamada, dando suporte à API do DirectShow<sup>TM</sup> como o manipulador de fluxo de mídia primário. A TAPI MSPs implementa interfaces do DirectShow para um TSP específico e é necessária para qualquer serviço de telefonia que utiliza o streaming do DirectShow. Os fluxos genéricos são tratados pelo aplicativo.

 

 
