---
title: Interfaces NLM
description: Interfaces NLM
ms.assetid: 57cc2a07-4551-428c-a303-9b1a4510f225
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322086a2860ff9bade47c9971662931f9ecada60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453735"
---
# <a name="nlm-interfaces"></a>Interfaces NLM

A seguir estão as interfaces NLM.

| Interface                                                            | Descrição                                                                                                                                                                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumNetworkConnections**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworkconnections)           | Fornece um enumerador padrão para conexões de rede. Ele enumera as conexões de rede ativas, desconectadas ou todas em uma rede. Essa interface pode ser obtida da interface de ti da [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) . |
| [**IEnumNetworks**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworks)                               | Enumera todas as redes disponíveis no servidor. Essa interface pode ser obtida da interface de ti da [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) .                                                                                         |
| [**Da INet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                         | Representa uma rede no servidor. Ele também pode representar uma coleção de conexões de rede com uma assinatura de rede semelhante.                                                                                          |
| [**INetworkConnection**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnection)                     | Representa uma única conexão de rede.                                                                                                                                                                                  |
| [**INetworkConnectionCost**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncost)                | Usado para consultar o custo atual da rede e o status do plano de dados associado a uma conexão.                                                                                                                                    |
| [**INetworkConnectionCostEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncostevents) | Usado para notificar um aplicativo de eventos de alteração de status de custo e de plano de dados para uma conexão.                                                                                                                               |
| [**INetworkConnectionEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectionevents)         | Uma interface de coletor que um cliente implementa para receber eventos relacionados a conexões de rede. Aplicativos que estão interessados em eventos de nível granular mais baixos, como alterações de autenticação, implementam essa interface.       |
| [**INetworkCostManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanager)                   | Usado para consultar as informações de custo de todo o computador e de status do plano de dados associadas a uma conexão usada para conectividade com a Internet em todo o computador ou o primeiro salto de roteamento para um destino específico em uma conexão. |
| [**INetworkCostManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanagerevents)       | Usado para notificar um aplicativo de custo em todo o computador e eventos relacionados ao plano de dados.                                                                                                                                         |
| [**INetworkEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkevents)                             | Uma interface de coletor que um cliente implementa para receber eventos relacionados à rede. Essas APIs são todas as funções de retorno de chamada que são chamadas automaticamente quando os respectivos eventos são gerados.                                  |
| [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager)                   | Fornece um conjunto de métodos para executar funções de gerenciamento de lista de rede.                                                                                                                                                  |
| [**INetworkListManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanagerevents)       | Uma interface de coletor que um cliente implementa para receber eventos relacionados ao Gerenciador de lista de rede. Aplicativos que estão interessados em eventos de nível mais granular, como conectividade com a Internet, implementam a interface.   |



 

 

 




