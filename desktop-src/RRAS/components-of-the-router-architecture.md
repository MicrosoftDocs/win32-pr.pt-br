---
title: Componentes da arquitetura do roteador
description: A documentação de administração do roteador faz referência frequente aos seguintes componentes do roteador.
ms.assetid: 841a5728-39d6-4bd7-a41a-6543b4ed9985
keywords:
- roteadores RRAS, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb0cc69de5402b03550873b3b052f6329b5238
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453602"
---
# <a name="components-of-the-router-architecture"></a>Componentes da arquitetura do roteador

A documentação de administração do roteador faz referência frequente aos seguintes componentes do roteador.

Gerenciador de interface dinâmica (DIM)

Todas as funções de administração de roteador passam por DIM. Dependendo da natureza da função, DIM pode passar a chamada para um dos gerenciadores do roteador. Funções que lidam apenas com interfaces são manipuladas por DIM. Se a função afetar os protocolos de roteamento, DIM chamará o Gerenciador do roteador para o transporte correspondente a esse protocolo. Por exemplo, se a função afetar o protocolo OSPF (abrir caminho mais curto primeiro), DIM chamará o Gerenciador do roteador IP, pois o OSPF é um protocolo de roteamento IP.

Gerenciadores de roteador

Cada transporte roteável que se encaixa na arquitetura do roteador tem seu próprio Gerenciador de roteador. Atualmente, os gerenciadores de roteadores existem para os transportes IP e IPX. Os gerenciadores de roteadores gerenciam protocolos de roteador e outros tipos de clientes de roteamento que são executados em interfaces no computador local.

Protocolos de roteamento e outros clientes

Os clientes são provedores de serviços que funcionam dentro da estrutura da arquitetura do roteador. Os protocolos de roteamento são um tipo de cliente com suporte pelo roteador.

Os clientes são específicos de um transporte roteável específico: IP ou IPX. Os protocolos de roteamento para o transporte IP incluem OSPF (Open Shortest Path First) e RIP (protocolo de informações de roteamento). Os exemplos de protocolos de roteamento IPX são SAP (Service Advertising Protocol) e RIP para IPX. Um exemplo de um cliente que não é um protocolo de roteamento é NAT (conversão de endereços de rede) para IP.

A interface entre o Gerenciador de roteador e um cliente é descrita na seção [interface do protocolo de roteamento](about-routing-protocol-interface.md). Todos os clientes estão em conformidade com essa interface. Usando essa interface, os fornecedores podem implementar seus próprios clientes que são compatíveis com o roteador.

[Interfaces](interfaces.md)

Uma interface é uma conexão com uma rede externa. Cada interface é identificada por um *índice* de interface exclusivo. As interfaces são entidades lógicas; clientes de roteador, como NAT ou OSPF, lidam com todos os tipos de interfaces da mesma forma. No entanto, em termos de implementação, uma interface pode representar uma conexão dedicada (como para uma LAN) ou uma conexão dial-up não dedicada (como uma conexão PPP com uma WAN (rede de longa distância)).

No caso de uma interface de LAN, a interface corresponde a um dispositivo físico real no computador, um adaptador de LAN. No caso de uma interface WAN, a interface é mapeada para uma porta no momento em que uma conexão é estabelecida. A porta pode ser uma porta COM, uma porta paralela ou uma porta virtual (para túneis como PPTP e L2TP).

As interfaces WAN têm a qualidade adicional em que normalmente recebem um endereço de rede somente no momento em que uma conexão é estabelecida. Por exemplo, uma interface WAN que usa o PPP recebe seu endereço da camada de rede do par remoto durante o processo de conexão. O recebimento de um endereço de rede como parte do processo de conexão, às vezes, é chamado de *associação tardia*.

 

 




