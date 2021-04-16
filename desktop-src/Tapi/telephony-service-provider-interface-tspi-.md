---
description: Um TSPI (provedor de serviços de telefonia) lida com controles específicos do dispositivo para a programação de comunicações.
ms.assetid: da54e219-9adb-4a12-baab-52f2b2fb7c66
title: Interface do provedor de serviços de telefonia (TSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a9d8ac4fd15fbc2685073e5954e14951f33acd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753530"
---
# <a name="telephony-service-provider-interface-tspi"></a>Interface do provedor de serviços de telefonia (TSPI)

Um TSPI (provedor de serviços de telefonia) lida com controles específicos do dispositivo para a programação de comunicações. Um TSP deve estar em conformidade com o provedor de serviços de telefonia (TSPI) para funcionar como um provedor de serviços no ambiente de telefonia da Microsoft. TSPI define as funções externas expostas por um provedor de serviços de telefonia fornecido com equipamentos de comunicação.

Um autor do TSP deve estar familiarizado com o material na [visão geral de telefonia da Microsoft](./microsoft-telephony-overview.md), que abrange a arquitetura de telefonia geral e fornece uma visão geral do material comum a várias APIs de telefonia. Por exemplo, esta seção contém uma lista de operações de controle de sessão, como o parque, com descrições de cada operação e salta para os elementos de programação TAPI 2,2, TAPI 3 e TSPI relacionados.

As visões gerais a seguir abrangem material específico às necessidades de um autor de TSP. Observe que as partes mais difíceis de escrever um TSP são detalhes específicos do sistema operacional e do dispositivo, que estão fora do escopo deste documento.

A visão geral do TSPI é dividida nas seguintes seções:

-   As [Considerações gerais de programação](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) abordam os requisitos de dll, a manipulação adequada de versões, verificações de erros executadas pela TAPI, um resumo de como as funções do TSPI correspondem às funções TAPI 2,2 (TAPI/C) e uma discussão sobre níveis de serviço, conforme expresso em TSPI.
-   O [ciclo de vida de um provedor de serviços de telefonia](life-cycle-of-a-telephony-service-provider.md) contém um resumo de alto nível das fases operacionais de um tsp.
-   O [acesso ao dispositivo](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) abrange as noções básicas de como um TSP expõe informações de dispositivo e controles para a TAPI.
-   O [acesso à sessão](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) aborda o que a TAPI espera de um TSP durante uma sessão de comunicações.
-   O [acesso à mídia](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) fornece um conjunto limitado de controles sobre fluxos de mídia. Um controle muito mais refinado é possível por meio do uso de um provedor de serviços de mídia, e os autores do provedor de serviços devem usar essa API sempre que possível. O TSPI fornece comunicações entre um par de TSP/MSP.
-   Os [dispositivos de telefone](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85)) abrangem as informações complementares e as operações expostas se um TSP processar o controle de conjunto de telefone. Essas operações são opcionais.
-   [A interface DLL da interface do usuário do provedor de serviços de telefonia](the-telephony-service-provider-ui-dll-interface.md) abrange funções especiais que podem ser implementadas para permitir que um usuário defina diretamente muitos aspectos da funcionalidade de um tsp.

Consulte a [referência de TSPI](tspi-reference.md) para obter detalhes dos elementos de programação do TSPI.

 

 
