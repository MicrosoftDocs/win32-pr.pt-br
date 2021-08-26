---
title: Alças de contexto
description: Às vezes, os aplicativos distribuídos exigem que o programa de servidor mantenha informações de status entre chamadas de cliente.
ms.assetid: 91732a75-0a3a-44bd-9db9-c11be6fd2d70
keywords:
- RPC de Chamada de Procedimento Remoto , descrito, alças de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73fb49a2e4c09ec818777389194df98e0d7b8bcac618d05ff7b519aefe5eb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073416"
---
# <a name="context-handles"></a>Alças de contexto

Às vezes, os aplicativos distribuídos exigem que o programa de servidor mantenha informações de status entre chamadas de cliente. Os programas de servidor que a serviço mais de um cliente por vez devem manter as informações de estado para cada cliente. Como o cliente e o servidor usam espaços de endereço diferentes em computadores diferentes e não confiam necessariamente uns nos outros, abordagens comuns ao compartilhamento de dados geralmente não funcionam. Por exemplo, o cliente e o servidor não conseguem manter informações de status em sua sessão remota em variáveis globais porque não compartilham o mesmo espaço de endereço global. É difícil manter as informações em um arquivo compartilhado porque elas são executados em computadores diferentes. Uma abordagem simplista pode ser enviar todo o estado para o cliente e fazer com que o cliente o retorne na próxima chamada, mas essa abordagem tem falhas: o servidor não confia necessariamente no cliente para retornar o estado certo e o estado pode ser implicitamente vinculado a algum outro estado no servidor, como alças de arquivo ou soquetes abertos.

O Microsoft RPC fornece um mecanismo poderoso e seguro chamado de alças de contexto para manter o estado associado a um determinado cliente em um servidor. As informações de estado são chamadas de contexto do servidor. Os clientes podem obter um identificador de contexto para identificar o contexto do servidor para suas sessões RPC individuais.

Por exemplo, cada cliente em um aplicativo distribuído pode fazer com que o programa de servidor crie e atualize um arquivo de dados para sua sessão RPC. O servidor pode usar seu alça de arquivo para o arquivo de dados de cada cliente como o alça de contexto. Sempre que um cliente solicita operações no arquivo de dados que o servidor cria para ele, o cliente passa o handle de contexto para o servidor. Na verdade, o cliente não tem o próprio lidar com o arquivo; ele obtém um token opaco que o tempo de executar RPC do servidor pode associar exclusivamente ao alça de arquivo. Como o alça de contexto é realmente um alça de arquivo, o alça de contexto só faz sentido no espaço de endereço do servidor. No entanto, o programa cliente pode usar o alça de contexto para dizer ao servidor em qual arquivo executar atualizações.

Outros dados também podem ser alças de contexto. Por exemplo, um cliente e um servidor podem usar um número de registro de um banco de dados como um alça de arquivo. Se o cliente precisar executar várias atualizações em um registro específico, ele poderá obter o número do registro como um alça de contexto. Ele transmitiria o número de registro para o servidor sempre que ele invocasse um procedimento remoto para atualizar o registro do banco de dados.

Geralmente, um handle de contexto aponta para um bloco de memória no servidor em que o servidor mantém várias informações de gerenciamento.

Esta seção apresenta informações sobre como definir e usar alças de contexto. A discussão é apresentada nos seguintes tópicos:

-   [Desenvolvimento de interface usando alças de contexto](interface-development-using-context-handles.md)
-   [Desenvolvimento de servidor usando alças de contexto](server-development-using-context-handles.md)
-   [Desenvolvimento de cliente usando alças de contexto](client-development-using-context-handles.md)
-   [Rotina de run-down do contexto do servidor](server-context-run-down-routine.md)
-   [Redefinição de contexto do cliente](client-context-reset.md)
-   [Clientes multithread e alças de contexto](multithreaded-clients-and-context-handles.md)

 

 




