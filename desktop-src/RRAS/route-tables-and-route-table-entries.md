---
title: Tabelas de rotas e entradas de tabela de rotas
description: O gerenciador de tabelas de roteamento mantém tabelas de rotas distintas para cada família de protocolos.
ms.assetid: 3848d93d-cc54-4a08-bd36-a9700cde6ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31fea4ac965fe397d5bb7eba2b65479358a1e192f1583b1e7e73c2532dbd3a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788051"
---
# <a name="route-tables-and-route-table-entries"></a>Tabelas de rotas e entradas de tabela de rotas

**Windows Server 2003:** Essa API foi superada pela API do Gerenciador de Tabelas de Roteamento versão [2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Novos aplicativos devem usar a API do Gerenciador de Tabelas de Roteamento versão 2.

O gerenciador de tabelas de roteamento mantém tabelas de rotas distintas para cada família de protocolos. Atualmente, o suporte explícito é fornecido para as famílias de protocolo de roteamento ip (ip) e IPX (internet packet Exchange). Independentemente da família de protocolos, cada entrada de rota contém as seguintes informações:

-   Rede de destino.
-   Identificador do protocolo que adicionou a rota.
-   Índice de interface por meio do qual a rota foi obtida. Esse valor de índice é o valor numérico atribuído a um interface de rede (baseado em hardware ou virtual) que transmite os dados para a rede. (Por exemplo, uma NIC Ethernet ou uma placa sem fio 802.1b.)
-   Endereço do roteador do próximo salto. O RRAS usa esse roteador para encaminhar pacotes para a rede de destino se a rede não estiver conectada diretamente.
-   A hora em que a rota foi criada ou atualizada pela última vez.
-   A quantidade de tempo que essa rota é mantida na tabela de roteamento. Se esse tempo passar e a rota não tiver sido atualizada, o gerenciador de tabela de roteamento removerá a rota da tabela. Nesse caso, diz-se que a rota *foi desalojada.*
-   Dados específicos da família de protocolos. Esses dados são transparentes para RTMv1. No entanto, se esses dados mudarem para uma rota designada como uma "melhor rota", o gerenciador de tabela de roteamento enviará uma notificação de alteração de rota.
-   Dados específicos para o protocolo de roteamento. Esses dados são completamente transparentes para o gerenciador de tabela de roteamento, pois as alterações a esses dados não causam notificação de alteração de rota.

Os seguintes valores juntos identificam exclusivamente uma rota na tabela de roteamento:

-   Rede de destino
-   Identificador de protocolo
-   Índice de interface
-   Endereço do roteador de próximo salto

Em geral, o gerenciador de tabela de roteamento cria entradas separadas para rotas que diferem em qualquer um desses valores de parâmetro. No entanto, uma exceção é feita para protocolos de roteamento que não mantêm mais de uma entrada para cada rede de destino. Para esses protocolos, o gerenciador de tabela de roteamento ignora as diferenças no índice da interface ou no endereço do próximo salto. Um exemplo desse protocolo é a implementação RRAS do OSPF (Open Shortest Path First).

 

 




