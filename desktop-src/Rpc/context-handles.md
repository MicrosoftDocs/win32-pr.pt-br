---
title: Identificadores de contexto
description: Às vezes, é o caso em que aplicativos distribuídos exigem que o programa de servidor mantenha informações de status entre chamadas de cliente.
ms.assetid: 91732a75-0a3a-44bd-9db9-c11be6fd2d70
keywords:
- Chamada de procedimento remoto RPC, descrito, identificadores de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ff36ff8f1a36843293060e091b7eecee0d8666
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105775655"
---
# <a name="context-handles"></a>Identificadores de contexto

Às vezes, é o caso em que aplicativos distribuídos exigem que o programa de servidor mantenha informações de status entre chamadas de cliente. Os programas de servidor que são atendidos mais de um cliente por vez devem manter as informações de estado de cada cliente. Como o cliente e o servidor usam espaços de endereço diferentes em computadores diferentes, e eles não necessariamente confiam uns nos outros, as abordagens comuns ao compartilhamento de dados geralmente não funcionam. Por exemplo, o cliente e o servidor não podem manter informações de status em suas sessões remotas em variáveis globais porque elas não compartilham o mesmo espaço de endereço global. É difícil manter as informações em um arquivo compartilhado porque elas são executadas em computadores diferentes. Uma abordagem simplista pode ser enviar todo o estado para o cliente e fazer com que o cliente o retorne na próxima chamada, mas essa abordagem tem falhas: o servidor não confia necessariamente no cliente para retornar o estado certo e o estado pode estar implicitamente ligado a algum outro Estado no servidor, como identificadores de arquivo ou soquetes abertos.

O Microsoft RPC fornece um mecanismo poderoso e seguro chamado identificadores de contexto para manter o estado associado a um determinado cliente em um servidor. As informações de estado são chamadas de contexto do servidor. Os clientes podem obter um identificador de contexto para identificar o contexto do servidor para suas sessões RPC individuais.

Por exemplo, cada cliente em um aplicativo distribuído pode fazer com que o programa do servidor crie e atualize um arquivo de dados para a sessão RPC. O servidor pode usar seu identificador de arquivo para cada arquivo de dados do cliente como o identificador de contexto. Cada vez que um cliente solicita operações no arquivo de dados que o servidor cria para ele, o cliente passa o identificador de contexto para o servidor. O cliente não obtém realmente o próprio identificador do arquivo; Ele obtém um token opaco que o tempo de execução do RPC do servidor pode associar exclusivamente ao identificador do arquivo. Como o identificador de contexto é realmente um identificador de arquivo, a alça de contexto só faz sentido no espaço de endereço do servidor. No entanto, o programa cliente pode usar o identificador de contexto para informar ao servidor em qual arquivo executar atualizações.

Outros dados também podem ser identificadores de contexto. Por exemplo, um cliente e um servidor podem usar um número de registro de um registro de banco de dados como um identificador de arquivo. Se o cliente precisar executar várias atualizações em um registro específico, ele poderá obter o número do registro como um identificador de contexto. Ele passaria o número do registro para o servidor sempre que ele invocasse um procedimento remoto para atualizar o registro do banco de dados.

Geralmente, um identificador de contexto aponta para um bloco de memória no servidor onde o servidor mantém várias informações de gerenciamento.

Esta seção apresenta informações sobre como definir e usar identificadores de contexto. A discussão é apresentada nos seguintes tópicos:

-   [Desenvolvimento de interface usando identificadores de contexto](interface-development-using-context-handles.md)
-   [Desenvolvimento de servidor usando identificadores de contexto](server-development-using-context-handles.md)
-   [Desenvolvimento de cliente usando identificadores de contexto](client-development-using-context-handles.md)
-   [Rotina de execução de contexto de servidor](server-context-run-down-routine.md)
-   [Redefinição de contexto de cliente](client-context-reset.md)
-   [Clientes multithread e identificadores de contexto](multithreaded-clients-and-context-handles.md)

 

 




