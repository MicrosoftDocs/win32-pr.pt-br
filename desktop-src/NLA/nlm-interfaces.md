---
title: NLM Interfaces
description: NLM Interfaces
ms.assetid: 57cc2a07-4551-428c-a303-9b1a4510f225
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07751a3f28c713b699cf60aa391d7141b19db0fcafd3ef13437f951c944dcb04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798502"
---
# <a name="nlm-interfaces"></a>NLM Interfaces

A seguir estão as interfaces NLM.

| Interface                                                            | Descrição                                                                                                                                                                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumNetworkConnections**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworkconnections)           | Fornece um enumerador padrão para conexões de rede. Ele enumera ativas, desconectadas ou todas as conexões de rede dentro de uma rede. Essa interface pode ser obtida da interface [**INetwork.**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) |
| [**IEnumNetworks**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworks)                               | Enumera todas as redes disponíveis no servidor. Essa interface pode ser obtida da interface [**INetwork.**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                                                                         |
| [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                         | Representa uma rede no servidor. Ele também pode representar uma coleção de conexões de rede com uma assinatura de rede semelhante.                                                                                          |
| [**INetworkConnection**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnection)                     | Representa uma única conexão de rede.                                                                                                                                                                                  |
| [**INetworkConnectionCost**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncost)                | Usado para consultar o custo de rede atual e o status do plano de dados associado a uma conexão.                                                                                                                                    |
| [**INetworkConnectionCostEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncostevents) | Usado para notificar um aplicativo de eventos de alteração de status de custo e de plano de dados para uma conexão.                                                                                                                               |
| [**INetworkConnectionEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectionevents)         | Uma interface de sink que um cliente implementa para receber eventos relacionados a conexões de rede. Aplicativos interessados em eventos de nível granular inferior, como alterações de autenticação, implementam essa interface.       |
| [**INetworkCostManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanager)                   | Usado para consultar informações de status de plano de dados e custo em todo o computador associadas a uma conexão usada para conectividade com a Internet em todo o computador ou o primeiro salto de roteamento para um destino específico em uma conexão. |
| [**INetworkCostManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanagerevents)       | Usado para notificar um aplicativo de eventos relacionados ao plano de dados e custo em todo o computador.                                                                                                                                         |
| [**INetworkEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkevents)                             | Uma interface de sink que um cliente implementa para receber eventos relacionados à rede. Essas APIs são todas funções de retorno de chamada que são chamadas automaticamente quando os respectivos eventos são gerados.                                  |
| [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager)                   | Fornece um conjunto de métodos para executar funções de gerenciamento de lista de rede.                                                                                                                                                  |
| [**INetworkListManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanagerevents)       | Uma interface de sink que um cliente implementa para receber eventos relacionados ao Gerenciador de Lista de Rede. Aplicativos interessados em eventos de nível granular mais alto, como conectividade com a Internet, implementam a interface .   |



 

 

 




