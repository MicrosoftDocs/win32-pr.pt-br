---
title: Protocolo de roteamento
description: Um protocolo de roteamento é um tipo de cliente que se registra com o gerenciador de tabela de roteamento. Os roteadores usam protocolos de roteamento para trocar informações sobre rotas para um destino.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 879d540662db7d1a1603bf40818101d0e7f9cb6988d4c0065f922fdc8f73e381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977839"
---
# <a name="routing-protocol"></a>Protocolo de roteamento

Um protocolo de roteamento é um tipo de cliente que se registra com o gerenciador de tabela de roteamento. Os roteadores usam protocolos de roteamento para trocar informações sobre rotas para um destino.

Os protocolos de roteamento são unicast ou multicast. Protocolos de roteamento anunciam rotas para um destino.

Uma rota unicast para um destino é usada por um protocolo de roteamento unicast para encaminhar dados unicast para esse destino. Exemplos de protocolos de roteamento unicast incluem: ROUTING INFORMATION PROTOCOL (RAS), OSPF (Abrir Caminho Mais Curto Primeiro) e Border Gateway Protocol (BGP).

Uma rota multicast para um destino é usada por alguns protocolos de roteamento multicast para criar as informações usadas para encaminhar dados multicast de hosts na rede de destino da rota (conhecida como encaminhamento de caminho reverso). Exemplos de protocolos de roteamento multicast incluem: Multicast Open Shortest Path First (MOSPF), DVMRP (Distance Vector Multicast Routing Protocol) e PIM (Multicast Independente de Protocolo).

O gerenciador de tabela de roteamento dá suporte a várias instâncias do mesmo protocolo (como a implementação do OSPF pela Microsoft e um OSPF de terceiros) em execução no roteador. Isso permite que os roteadores usem os diferentes recursos de cada versão. Esses protocolos têm identificadores de protocolo diferentes.

Os identificadores de protocolo são compostos por um identificador de fornecedor e um identificador específico do protocolo. O identificador específico do protocolo é o mesmo para implementações diferentes do protocolo, como a implementação do OSPF pela Microsoft e uma implementação de terceiros do OSPF. Somente quando os identificadores específicos do fornecedor e do protocolo são combinados há um identificador exclusivo para um protocolo de roteamento.

Um protocolo com o mesmo identificador de protocolo (ou seja, o mesmo identificador de fornecedor e identificador específico do protocolo) pode se registrar com o gerenciador de tabelas de roteamento várias vezes. Cada vez, o protocolo é registrado usando um identificador de instância de protocolo diferente. Por exemplo, uma implementação do OSPF de um fornecedor específico pode se registrar como Vendor-OSPF-1 e Vendor-OSPF-2. Isso permite que uma implementação de protocolo específica particione as informações que ela mantém na tabela de roteamento.

 

 




