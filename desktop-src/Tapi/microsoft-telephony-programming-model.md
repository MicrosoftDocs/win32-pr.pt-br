---
description: O modelo de programação de telefonia da Microsoft abstrai o controle de comunicação do controle de dispositivo, liberando aplicativos de usuário final e fabricantes de dispositivos da necessidade de março no atrelada.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Modelo de programação de telefonia da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33407069c8ff489006c3cb85e03b676126eca1abedf484d9d1bb5b1305677a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518636"
---
# <a name="microsoft-telephony-programming-model"></a>Modelo de programação de telefonia da Microsoft

O modelo de programação de telefonia da Microsoft abstrai o controle de comunicação do controle de dispositivo, liberando aplicativos de usuário final e fabricantes de dispositivos da necessidade de março no atrelada. Usando esse modelo, um usuário final ou um aplicativo de servidor não requer informações detalhadas sobre o controle de dispositivo e o dispositivo não precisa ser ajustado para o aplicativo. Aplicativos e dispositivos podem passar por inovações e alterações sem renderizar outros inúteis para os clientes.

O diagrama a seguir ilustra como essa abstração é realizada.

![como a TAPI abstrai o controle de comunicação do controle de dispositivo](images/tapicomp.png)

Esses componentes podem ser exibidos como repositórios de conhecimento especializado. O aplicativo da TAPI (interface de programação de aplicativo) de telefonia sabe que as necessidades do usuário, a DLL de TAPI e o TAPISRV entendem a telefonia geral e os provedores de serviços (TSP e MSP) sabem controle de dispositivo detalhado. Os desenvolvedores de aplicativos e os fabricantes de dispositivos exigem apenas conhecimento geral dos requisitos uns dos outros.

-   Um aplicativo carrega a DLL TAPI em seu espaço de processo e usa a TAPI para comunicar as necessidades.
-   A TAPI estabelece uma comunicação de link RPC com o servidor TAPI.
-   Além disso, a TAPI 3. x cria um objeto MSP e se comunica com ele usando um conjunto definido de comandos, a MSPI (interface do provedor de serviços de mídia).
-   Quando um aplicativo chama uma operação TAPI, a biblioteca de vínculo dinâmico TAPI valida e realiza marshaling dos parâmetros e, em seguida, encaminha as informações para TAPISRV.
-   O TAPISRV rastreia os recursos de comunicação disponíveis para o computador local e as interfaces com os provedores de serviços de telefonia (TSPs) usando a interface do provedor de serviços de telefonia (TSPI).
-   As comunicações entre um TSP e um MSP ocorrem usando uma conexão virtual que passa pela DLL de TAPI e TAPISRV.
-   O par de TSP/MSP fornece informações sobre o estado do dispositivo e os recursos e implementa os comandos específicos necessários para uma resposta desejada.

O resultado do uso desse modelo de programação é que os aplicativos podem ignorar ou ajustar às alterações do dispositivo, e novos dispositivos podem ser instantaneamente úteis em vez de aguardar as alterações na base do código. A possível participação no mercado é expandida para os desenvolvedores de aplicativos e para os fabricantes de dispositivos.

Os tópicos a seguir descrevem os componentes de telefonia da Microsoft com mais detalhes:

-   [Aplicativos TAPI](tapi-applications.md)
-   [DLL TAPI](tapi-dll.md)
-   [Servidor TAPI](tapi-server.md)
-   [Provedores de serviço](service-providers.md)
-   [Modelo síncrono/assíncrono](synchronous-asynchronous-model.md)
-   [Estruturas de dados TAPI](tapi-data-structures.md)
-   [Níveis de serviço TAPI](tapi-levels-of-service.md)

 

 



