---
title: Sobre o Gerenciador de tabela de roteamento versão 1
description: O Gerenciador de tabela de roteamento é um repositório central de informações de roteamento para todos os protocolos de roteamento que operam em RRAS (serviço de roteamento e acesso remoto).
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de tabela de roteamento versão 1
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de tabela de roteamento versão 1, descrito
- Gerenciador de tabela de roteamento versão 1 RRAS
- Gerenciador de tabela de roteamento versão 1 RRAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005641"
---
# <a name="about-routing-table-manager-version-1"></a>Sobre o Gerenciador de tabela de roteamento versão 1

**Windows Server 2003:** Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Novos aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.

O Gerenciador de tabela de roteamento é um repositório central de informações de roteamento para todos os protocolos de roteamento que operam em RRAS (serviço de roteamento e acesso remoto). O Gerenciador de tabela de roteamento fornece informações de roteamento para todos os componentes interessados, como protocolos de roteamento, agentes de gerenciamento e agentes de monitoramento. O Gerenciador de tabela de roteamento também determina a melhor rota para cada rede de destino conhecida pelos protocolos de roteamento. Ele determina essa rota com base nas prioridades do protocolo de roteamento e nas métricas associadas às rotas. Observe que o administrador é capaz de configurar as prioridades do protocolo de roteamento. Em seguida, o Gerenciador de tabela de roteamento passa as informações de melhor rota para os encaminhadores e de volta para os protocolos de roteamento.

Cada protocolo de roteamento chama [**RtmRegisterClient**](rtmregisterclient.md) para registrar com o Gerenciador de tabela de roteamento. **RtmRegisterClient** retorna um identificador que é usado pelo protocolo de roteamento para adicionar ou excluir entradas de rota. O **RtmRegisterClient** também permite que o protocolo de roteamento registre um objeto de evento com o Gerenciador de tabela de roteamento. O Gerenciador de tabela de roteamento sinaliza esse objeto de evento para notificar o protocolo de roteamento das alterações nas informações de melhor rota. Todos os outros componentes podem obter informações armazenadas no Gerenciador de tabela de roteamento por meio de enumeração de rota.

 

 




