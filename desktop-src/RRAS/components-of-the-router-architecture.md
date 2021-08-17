---
title: Componentes da arquitetura do roteador
description: A documentação de administração do roteador faz referência frequente aos seguintes componentes do roteador.
ms.assetid: 841a5728-39d6-4bd7-a41a-6543b4ed9985
keywords:
- roteadores RRAS , componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f39f104e001db99076dcd29d9d5b603d5cf9f3c526d54cd16e1ed0e4d10c575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791590"
---
# <a name="components-of-the-router-architecture"></a>Componentes da arquitetura do roteador

A documentação de administração do roteador faz referência frequente aos seguintes componentes do roteador.

DIM (Dynamic Interface Manager)

Todas as funções de administração de roteador passam pelo DIM. Dependendo da natureza da função, o DIM pode passar a chamada para um dos gerenciadores de roteador. As funções que lidam apenas com interfaces são tratadas pelo DIM. Se a função afetar os protocolos de roteamento, o DIM chamará o gerenciador do roteador para o transporte correspondente a esse protocolo. Por exemplo, se a função afetar o protocolo OSPF (Abrir Caminho Mais Curto Primeiro), o DIM chamará o Gerenciador de Roteador IP, pois o OSPF é um protocolo de roteamento ip.

Gerenciadores de roteador

Cada transporte de tabela que se ajusta à arquitetura do roteador tem seu próprio gerenciador de roteadores. Atualmente, os gerenciadores de roteador existem para os transportes IP e IPX. Os gerenciadores de roteadores gerenciam protocolos de roteador e outros tipos de clientes de roteamento que são executados em interfaces no computador local.

Protocolos de roteamento e outros clientes

Os clientes são provedores de serviços que funcionam dentro da estrutura da arquitetura do roteador. Os protocolos de roteamento são um tipo de cliente com suporte do roteador.

Os clientes são específicos para um transporte de tabela específica: IP ou IPX. Os protocolos de roteamento para o transporte ip incluem OSPF (Open Shortest Path First) e ROUTING INFORMATION PROTOCOL (PATH). Exemplos de protocolos de roteamento IPX são SAP (Service Advertising Protocol) eWL para IPX. Um exemplo de um cliente que não é um protocolo de roteamento é NAT (Conversão de Endereços de Rede) para IP.

A interface entre o gerenciador de roteador e um cliente é descrita na seção Interface do [protocolo de roteamento](about-routing-protocol-interface.md). Todos os clientes estão em conformidade com essa interface. Usando essa interface, os fornecedores podem implementar seus próprios clientes compatíveis com o roteador.

[Interfaces](interfaces.md)

Uma interface é uma conexão com uma rede externa. Cada interface é identificada por um índice de interface *exclusivo*. Interfaces são entidades lógicas; clientes de roteador, como NAT ou OSPF, lidam com todos os tipos de interfaces da mesma forma. No entanto, em termos de implementação, uma interface pode representar uma conexão dedicada (como uma LAN (Rede de Área Local) ou uma conexão discada não dedicada (como uma conexão PPP com uma WAN (Rede de Área Larga).

No caso de uma interface LAN, a interface corresponde a um dispositivo físico real no computador, um adaptador de LAN. No caso de uma interface WAN, a interface é mapeada para uma porta no momento em que uma conexão é estabelecida. A porta pode ser uma porta COM, uma porta paralela ou uma porta virtual (para túneis como PPTP e L2TP).

As interfaces WAN têm a qualidade adicional que normalmente recebem um endereço de rede somente no momento em que uma conexão é estabelecida. Por exemplo, uma interface WAN usando PPP recebe seu endereço de camada de rede do par remoto durante o processo de conexão. Receber um endereço de rede como parte do processo de conexão às vezes é chamado de *associação tardia.*

 

 




