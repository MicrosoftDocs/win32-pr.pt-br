---
title: Alterações na melhor rota para uma rede
description: Uma alteração em qualquer um dos seguintes valores para a melhor rota para uma determinada rede de destino faz com que o Gerenciador de tabela de roteamento gere uma mensagem de notificação enviada para cada cliente registrado e para os encaminhadores
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8c43483dbd69f5407f9859d5943e515e8825d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105787034"
---
# <a name="changes-to-the-best-route-to-a-network"></a>Alterações na melhor rota para uma rede

**Windows Server 2003:** Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Novos aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.

Uma alteração em qualquer um dos seguintes valores para a melhor rota para uma determinada rede de destino faz com que o Gerenciador de tabela de roteamento gere uma mensagem de notificação enviada para cada cliente registrado e para os encaminhadores:

-   Identificador de protocolo
-   Índice de interface
-   Endereço do roteador do próximo salto
-   Dados específicos da família de protocolos que incluem métricas de rota

Uma alteração no identificador de protocolo, índice de interface ou endereço de roteador do próximo salto ocorre quando uma nova entrada de rota melhor é adicionada ou quando a entrada de melhor rota atual é excluída ou expirada e deixa outra rota como a nova rota recomendada.

 

 




