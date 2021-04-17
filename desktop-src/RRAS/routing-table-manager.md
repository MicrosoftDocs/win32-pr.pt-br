---
title: Gerenciador de tabela de roteamento
description: O Gerenciador de tabela de roteamento é o repositório central de informações de roteamento para todos os protocolos de roteamento que operam no RRAS (serviço de roteamento e acesso remoto).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759601"
---
# <a name="routing-table-manager"></a>Gerenciador de tabela de roteamento

O Gerenciador de tabela de roteamento é o repositório central de informações de roteamento para todos os protocolos de roteamento que operam no RRAS (serviço de roteamento e acesso remoto). Ele notifica os clientes quando as alterações ocorreram e permite que os clientes troquem informações particulares.

O Gerenciador de tabela de roteamento fornece informações de roteamento para todos os clientes interessados, como protocolos de roteamento, programas de gerenciamento e programas de monitoramento. O Gerenciador de tabela de roteamento também determina a melhor rota para cada rede de destino conhecida pelos protocolos de roteamento. O Gerenciador de tabela de roteamento determina essa rota com base nas prioridades do protocolo de roteamento e nas métricas associadas às rotas. A pessoa que administra o roteador pode configurar as prioridades do protocolo de roteamento usando o console de gerenciamento do RRAS.

O Gerenciador de tabela de roteamento passa as informações de melhor rota para os encaminhadores (uma por família de endereços ou uma por interface) e para todos os clientes interessados.

Cada cliente é registrado com o Gerenciador de tabela de roteamento e, em retorno, recebe um identificador que o cliente usa para adicionar ou excluir rotas. Os clientes podem recuperar informações armazenadas na tabela de roteamento. Além disso, os clientes podem se registrar no Gerenciador de tabelas de roteamento para receber notificações de alterações na melhor rota para um destino.

 

 




