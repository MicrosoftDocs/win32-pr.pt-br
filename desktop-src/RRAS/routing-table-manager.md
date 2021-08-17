---
title: Gerenciador de tabela de roteamento
description: O Gerenciador de tabela de roteamento é o repositório central de informações de roteamento para todos os protocolos de roteamento que operam no RRAS (serviço de roteamento e acesso remoto).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 850726cd2203eca85be33aea3bd33f1ed903ba2d197d102ff7de294c5e852626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787464"
---
# <a name="routing-table-manager"></a>Gerenciador de tabela de roteamento

O Gerenciador de tabela de roteamento é o repositório central de informações de roteamento para todos os protocolos de roteamento que operam no RRAS (serviço de roteamento e acesso remoto). Ele notifica os clientes quando as alterações ocorreram e permite que os clientes troquem informações particulares.

O Gerenciador de tabela de roteamento fornece informações de roteamento para todos os clientes interessados, como protocolos de roteamento, programas de gerenciamento e programas de monitoramento. O Gerenciador de tabela de roteamento também determina a melhor rota para cada rede de destino conhecida pelos protocolos de roteamento. O Gerenciador de tabela de roteamento determina essa rota com base nas prioridades do protocolo de roteamento e nas métricas associadas às rotas. A pessoa que administra o roteador pode configurar as prioridades do protocolo de roteamento usando o console de gerenciamento do RRAS.

O Gerenciador de tabela de roteamento passa as informações de melhor rota para os encaminhadores (uma por família de endereços ou uma por interface) e para todos os clientes interessados.

Cada cliente é registrado com o Gerenciador de tabela de roteamento e, em retorno, recebe um identificador que o cliente usa para adicionar ou excluir rotas. Os clientes podem recuperar informações armazenadas na tabela de roteamento. Além disso, os clientes podem se registrar no Gerenciador de tabelas de roteamento para receber notificações de alterações na melhor rota para um destino.

 

 




