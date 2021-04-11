---
title: Como a arquitetura de multicast se encaixa
description: Esta seção descreve uma configuração de exemplo e como os principais componentes se encaixam.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc82178568bac01e89eb0a4d6ea9222d45e7f5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160057"
---
# <a name="how-the-multicast-architecture-fits-together"></a>Como a arquitetura de multicast se encaixa

Esta seção descreve uma configuração de exemplo e como os principais componentes se encaixam.

A ilustração a seguir mostra a relação entre os vários componentes de um roteador.

![relação entre componentes do roteador do Windows 2000](images/mrarch1.png)

O Gerenciador do grupo de multicast faz parte do serviço RRAS que é executado em um servidor que está operando como um roteador.

O roteador mostrado tem três protocolos de roteamento multicast (protocolo 1, protocolo 2, protocolo 3) em execução. Cada protocolo pode possuir uma ou mais interfaces (nesta ilustração, o protocolo 1 possui a interface 1, o protocolo 2 possui a interface 2 e o protocolo 3 possui a interface 3). Cada interface pode pertencer apenas a um protocolo de roteamento (além de IGMP, que é um caso especial).

O Gerenciador do grupo de multicast é executado no roteador e coordena a distribuição de informações de grupo entre os protocolos de roteamento.

A ilustração a seguir mostra a relação entre dois roteadores em uma arquitetura de multicast.

![relação entre dois roteadores na arquitetura de multicast](images/mrarch2.png)

Na ilustração anterior, o roteador 2 envia uma mensagem de multicast para a rede 2 na interface 3. O roteador 1 recebe a mensagem de multicast da rede 2 na interface 3. Em ambos os roteadores, o protocolo 3 possui a respectiva interface 3.

A ilustração a seguir mostra o caminho em que uma mensagem de uma fonte multicast (para um grupo de multicast) leva para alcançar o host que ingressou no grupo de multicast. Os roteadores na ilustração usam a mesma configuração das ilustrações anteriores; no entanto, os detalhes da interface e do protocolo não são mostrados para manter a figura simples.

![caminho da mensagem da origem de multicast para o host de destino](images/mrarch3.png)

O cenário a seguir descreve os eventos que ocorrem quando um host ingressa em um grupo de multicast. Consulte a ilustração anterior para obter relações entre as várias entidades.

1.  O host 1 une o grupo de multicast G na rede 3.
2.  O roteador 3 aprende sobre o G via IGMP.
3.  O Gerenciador de grupo de multicast no roteador 3 notifica o protocolo 3 no roteador 3 de que há novos destinatários para G.
4.  O protocolo 3 no roteador 3 notifica o protocolo 3 no roteador 1 sobre G.
5.  Por sua vez, o protocolo 3 no roteador 1 notifica o Gerenciador de grupo de multicast no roteador 1 sobre G.
6.  O Gerenciador de grupo de multicast no roteador 1 notifica o protocolo 1 e o protocolo 2 sobre G.
7.  O protocolo 2 pode informar ao roteador 2 sobre G, se o protocolo for projetado para fazer isso.

O cenário a seguir descreve os eventos que ocorrem quando uma mensagem é enviada a um grupo de multicast. Consulte a ilustração anterior para obter as relações entre as várias entidades.

1.  Uma fonte na rede 1 envia uma mensagem para o Grupo G.
2.  A mensagem enviada dos S de origem é primeiro para o roteador 2, que, em seguida, a encaminha para o roteador 1 usando a interface 2 (já que o roteador 2 foi informado pelo protocolo 2 que os receptores estão presentes no downstream).
3.  O roteador 1 encaminha a mensagem para o roteador 3 (uma vez que o roteador 1 foi informado pelo protocolo 2 que os receptores estão presentes no downstream).
4.  O roteador 3 encaminha a mensagem para a rede 3 e, portanto, chega no host 1.

Para obter mais informações sobre a interação do protocolo de roteamento de multicast, consulte [RFC 2715](routing-protocols-request-for-comments.md), regras de interoperabilidade para protocolos de roteamento de multicast.

 

 




