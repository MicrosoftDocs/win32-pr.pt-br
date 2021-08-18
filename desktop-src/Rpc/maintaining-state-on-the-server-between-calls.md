---
title: Mantendo o estado no servidor entre chamadas
description: Geralmente, é necessário manter o estado no servidor entre chamadas RPC separadas \ 8212; o uso de alças de contexto é a melhor maneira de fazer isso. Algumas palavras sobre como os lidares de contexto operam internamente ajudam a entender quando os tratadores de contexto funcionam melhor.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- RPC de Chamada de Procedimento Remoto , práticas recomendadas, mantendo o estado entre chamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e564acbb4748cd76988c1b064a58ede2169d3d20da4033774f3141883a7193bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928581"
---
# <a name="maintaining-state-on-the-server-between-calls"></a>Mantendo o estado no servidor entre chamadas

Geralmente, é necessário manter o estado no servidor entre chamadas RPC separadas – o uso de alças de contexto é a melhor maneira de fazer isso. Algumas palavras sobre como os lidares de contexto operam internamente ajudam a entender quando os tratadores de contexto funcionam melhor.

O cliente nunca recebe o estado mantido no servidor. Geralmente, o estado no servidor é um ponteiro para um bloco de memória e o cliente não tem informações sobre ele. Todos os recebimentos do cliente são um grande número exclusivo, com outras informações associadas a ele, que o servidor envia ao cliente e que representa o handle de contexto em todas as operações subsequentes. Sempre que o cliente se refere a um alça aberta, ele envia o grande número recebido do servidor quando esse alça de contexto foi aberto.

O servidor mantém o controle de todos os números grandes que ele envia a um cliente. Quando o servidor recebe um número grande que representa um alça de contexto, ele procura o número na coleção de alças de contexto válidas e pendentes para esse cliente e localiza o contexto do lado do servidor correspondente a um determinado número grande. Isso é passado para a rotina do servidor. Se o número grande não for encontrado, uma exceção RPC X SS CONTEXT MISMATCH será apurada e \_ \_ \_ \_ propagada para o cliente.

As corollaries desse design são as seguinte:

-   Um handle de contexto é válido somente no contexto da sessão de cliente/servidor existente. Ele não pode ser passado para outro cliente.
-   Um handle de contexto se tornará inválido se o servidor for reinicializado ou, caso contrário, perderá sua conexão com o cliente.
-   O cliente não pode interpretar o que o handle de contexto representa no servidor. Para um cliente, todos os alças de contexto são simplesmente números grandes.

Se o cliente falhar, o servidor receberá uma notificação e limpará seus alças de contexto usando o mecanismo de run-down.

 

 




