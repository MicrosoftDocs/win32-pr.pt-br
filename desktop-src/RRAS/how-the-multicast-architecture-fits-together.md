---
title: Como a arquitetura multicast se encaixa
description: Esta seção descreve uma configuração de exemplo e como os principais componentes se encaixam.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94f4ca79b9fdd6b2e2fd9e75dc61d780af4380ed958a491f69231f7d541f0aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791302"
---
# <a name="how-the-multicast-architecture-fits-together"></a>Como a arquitetura multicast se encaixa

Esta seção descreve uma configuração de exemplo e como os principais componentes se encaixam.

A ilustração a seguir mostra a relação entre os vários componentes de um roteador.

![relação entre componentes do roteador windows 2000](images/mrarch1.png)

O gerenciador de grupos multicast faz parte do serviço RRAS que é executado em um servidor que está operando como um roteador.

O roteador mostrado tem três protocolos de roteamento multicast (Protocolo 1, Protocolo 2, Protocolo 3) em execução nele. Cada protocolo pode ter uma ou mais interfaces (nesta ilustração, o Protocolo 1 possui a Interface 1, o Protocolo 2 possui a Interface 2 e o Protocolo 3 possui a Interface 3). Cada interface pode ser de propriedade de apenas um protocolo de roteamento (além do IGMP, que é um caso especial).

O gerenciador de grupos multicast é executado no roteador e coordena a distribuição de informações de grupo entre os protocolos de roteamento.

A ilustração a seguir mostra a relação entre dois roteadores em uma arquitetura multicast.

![relação entre dois roteadores na arquitetura multicast](images/mrarch2.png)

Na ilustração anterior, o Roteador 2 envia uma mensagem multicast para a Rede 2 na Interface 3. O roteador 1 recebe a mensagem multicast da Rede 2 na Interface 3. Em ambos os roteadores, o Protocolo 3 possui a respectiva Interface 3.

A ilustração a seguir mostra o caminho que uma mensagem de uma fonte multicast (para um grupo multicast) leva para alcançar o host que ingressou no grupo multicast. Os roteadores na ilustração usam a mesma configuração que as ilustrações anteriores; no entanto, os detalhes da interface e do protocolo não são mostrados para manter a figura simples.

![caminho da mensagem da origem multicast para o host de destino](images/mrarch3.png)

O cenário a seguir descreve os eventos que ocorrem quando um host inscrevo em um grupo de multicast. Consulte a ilustração anterior para ver as relações entre as várias entidades.

1.  O Host 1 une o grupo multicast G na Rede 3.
2.  O roteador 3 aprende sobre G por meio de IGMP.
3.  O gerenciador de grupos multicast no Roteador 3 notifica o Protocolo 3 no Roteador 3 de que há novos receptores para G.
4.  O protocolo 3 no Roteador 3 notifica o Protocolo 3 no Roteador 1 sobre G.
5.  Por sua vez, o Protocolo 3 no Roteador 1 notifica o gerenciador de grupos multicast no Roteador 1 sobre G.
6.  O gerenciador de grupos multicast no Roteador 1 notifica o Protocolo 1 e o Protocolo 2 sobre G.
7.  O protocolo 2 pode informar o Roteador 2 sobre G, se o protocolo foi projetado para fazer isso.

O cenário a seguir descreve os eventos que ocorrem quando uma mensagem é enviada a um grupo multicast. Consulte a ilustração anterior para ver as relações entre as várias entidades.

1.  Uma fonte na Rede 1 envia uma mensagem para o Grupo G.
2.  A mensagem enviada da Origem S vai primeiro para o Roteador 2, que a encaminha para o Roteador 1 usando a Interface 2 (já que o Roteador 2 foi informado pelo Protocolo 2 de que os receptores estão presentes downstream).
3.  O roteador 1 encaminha a mensagem para o Roteador 3 (já que o Roteador 1 foi informado pelo Protocolo 2 de que os receptores estão presentes downstream).
4.  O roteador 3 encaminha a mensagem para a Rede 3 e, portanto, ela chega ao Host 1.

Para obter mais informações sobre a interação do protocolo de roteamento multicast, consulte [RFC 2715](routing-protocols-request-for-comments.md), Regras de interoperabilidade para protocolos de roteamento multicast.

 

 




