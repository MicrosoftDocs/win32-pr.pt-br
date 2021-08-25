---
title: Alterações na melhor rota para uma rede
description: Uma alteração em qualquer um dos seguintes valores para a melhor rota para uma determinada rede de destino faz com que o Gerenciador de tabela de roteamento gere uma mensagem de notificação enviada para cada cliente registrado e para os encaminhadores
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fe96a0b339325c2290c346ba581d5b892db24d1cd972f7a83a0b2ec525eeb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030356"
---
# <a name="changes-to-the-best-route-to-a-network"></a>Alterações na melhor rota para uma rede

**Windows Server 2003:** esta api foi substituída pela api do [gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Novos aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.

Uma alteração em qualquer um dos seguintes valores para a melhor rota para uma determinada rede de destino faz com que o Gerenciador de tabela de roteamento gere uma mensagem de notificação enviada para cada cliente registrado e para os encaminhadores:

-   Identificador de protocolo
-   Índice de interface
-   Endereço do roteador do próximo salto
-   Dados específicos da família de protocolos que incluem métricas de rota

Uma alteração no identificador de protocolo, índice de interface ou endereço de roteador do próximo salto ocorre quando uma nova entrada de rota melhor é adicionada ou quando a entrada de melhor rota atual é excluída ou expirada e deixa outra rota como a nova rota recomendada.

 

 




