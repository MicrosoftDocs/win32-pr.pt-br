---
description: Um TSPI (Provedor de Serviços de Telefonia) lida com controles específicos do dispositivo para programação de comunicações.
ms.assetid: da54e219-9adb-4a12-baab-52f2b2fb7c66
title: Interface do provedor de serviços de telefonia (TSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fac57f3b86acdf105c4c78f46f4f1d1d0e270c2a0b1be2d8bd1f55009926329
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681796"
---
# <a name="telephony-service-provider-interface-tspi"></a>Interface do provedor de serviços de telefonia (TSPI)

Um TSPI (Provedor de Serviços de Telefonia) lida com controles específicos do dispositivo para programação de comunicações. Um TSP deve estar em conformidade com o TSPI (Provedor de Serviços de Telefonia) para funcionar como um provedor de serviços no ambiente de Telefonia da Microsoft. O TSPI define as funções externas expostas por um provedor de serviços de telefonia fornecido com equipamentos de comunicação.

Um autor do TSP deve estar familiarizado com o material na Visão geral de telefonia da [Microsoft,](./microsoft-telephony-overview.md)que aborda a arquitetura de telefonia geral e fornece uma visão geral do material comum a várias APIs de telefonia. Por exemplo, esta seção contém uma lista de operações de controle de sessão, como Park, com descrições de cada operação e vai para os elementos de programação TAPI 2.2, TAPI 3 e TSPI relacionados.

As visão geral a seguir abrangem material específico para as necessidades de um autor do TSP. Observe que as partes mais difíceis de escrever um TSP são detalhes específicos do dispositivo e do sistema operacional, que estão fora do escopo deste documento.

A visão geral do TSPI é dividida nas seguintes seções:

-   As Considerações gerais sobre programação abrangem [requisitos](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) de DLL, tratamento adequado de versões, verificações de erro executadas pela TAPI, um resumo de como as funções TSPI correspondem às funções TAPI 2.2 (TAPI/C) e uma discussão sobre níveis de serviço, conforme expresso em TSPI.
-   O [Ciclo de Vida de um](life-cycle-of-a-telephony-service-provider.md) Provedor de Serviços de Telefonia contém um resumo de alto nível das fases operacionais de um TSP.
-   [O Acesso ao](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) Dispositivo aborda as noções básicas de como um TSP expõe informações e controles do dispositivo à TAPI.
-   [O Acesso à](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) Sessão abrange o que a TAPI espera de um TSP durante uma sessão de comunicação.
-   [O Acesso à](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) Mídia fornece um conjunto limitado de controles sobre fluxos de mídia. Um controle muito mais fino é possível por meio do uso de um provedor de serviços de mídia, e os autores do provedor de serviços devem usar essa API sempre que possível. O TSPI fornece comunicações entre um par TSP/MSP.
-   [Telefone Dispositivos abrangem](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85)) as informações complementares e as operações expostas se um TSP manipular o controle de conjunto de telefone. Essas operações são opcionais.
-   [A Interface de DLL](the-telephony-service-provider-ui-dll-interface.md) da interface do usuário do Provedor de Serviços de Telefonia abrange funções especiais que podem ser implementadas para permitir que um usuário de definir diretamente muitos aspectos da funcionalidade de um TSP.

Consulte a Referência [de TSPI para](tspi-reference.md) obter detalhes dos elementos de programação TSPI.

 

 
