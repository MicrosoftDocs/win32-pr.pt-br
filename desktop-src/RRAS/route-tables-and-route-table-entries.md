---
title: Tabelas de rotas e entradas da tabela de rotas
description: O Gerenciador de tabela de roteamento mantém tabelas de rotas distintas para cada família de protocolos.
ms.assetid: 3848d93d-cc54-4a08-bd36-a9700cde6ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f118ec1d0a6f8fe4ef301654e139f217257c3a0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105758574"
---
# <a name="route-tables-and-route-table-entries"></a>Tabelas de rotas e entradas da tabela de rotas

**Windows Server 2003:** Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Novos aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.

O Gerenciador de tabela de roteamento mantém tabelas de rotas distintas para cada família de protocolos. Atualmente, o suporte explícito é fornecido para as famílias de protocolo Internet (IP) e Internet Packet Exchange (IPX). Independentemente da família de protocolos, cada entrada de rota contém as seguintes informações:

-   Rede de destino.
-   Identificador do protocolo que adicionou a rota.
-   Índice da interface por meio da qual a rota foi obtida. Esse valor de índice é o valor numérico atribuído a um adaptador de rede (baseado em hardware ou virtual) que transmite os dados para a rede. (Por exemplo, uma NIC Ethernet ou uma placa sem fio 802.1 b.)
-   Endereço do roteador do próximo salto. O RRAS usa esse roteador para encaminhar pacotes para a rede de destino se a rede não estiver conectada diretamente.
-   A hora em que a rota foi criada ou atualizada pela última vez.
-   A quantidade de tempo em que essa rota é mantida na tabela de roteamento. Se essa quantidade de tempo decorrer e a rota não tiver sido atualizada, o Gerenciador de tabela de roteamento removerá a rota da tabela. Nesse caso, diz-se que a rota tem *expiração*.
-   Dados específicos para a família de protocolos. Esses dados são transparentes para RTMv1. No entanto, se esses dados forem alterados para uma rota designada como "melhor rota", o Gerenciador de tabela de roteamento enviará a notificação de alteração de rota.
-   Dados específicos para o protocolo de roteamento. Esses dados são completamente transparentes para o Gerenciador de tabelas de roteamento, nesse caso, as alterações a esses dados não causam a notificação de alteração de rota.

Os valores a seguir foram agrupados exclusivamente para identificar uma rota na tabela de roteamento:

-   Rede de destino
-   Identificador de protocolo
-   Índice de interface
-   Endereço do roteador do próximo salto

Em geral, o Gerenciador de tabela de roteamento cria entradas separadas para rotas que diferem em qualquer um desses valores de parâmetro. No entanto, uma exceção é feita para protocolos de roteamento que não mantêm mais de uma entrada para cada rede de destino. Para esses protocolos, o Gerenciador de tabela de roteamento ignora as diferenças no índice de interface ou no endereço de próximo salto. Um exemplo desse protocolo é a implementação de RRAS do OSPF (Open Shortest Path First).

 

 




