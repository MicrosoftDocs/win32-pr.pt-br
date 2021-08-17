---
title: O modelo para sistemas distribuídos
description: Tradicionalmente, ter um sistema monolítico executado em vários computadores significa dividir o sistema em componentes separados do cliente e do servidor.
ms.assetid: 6055bcef-e34c-4f2d-92b9-9aec75cf3cec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859b2a0a83e7f12bd7caf372e60acf2736a114a0cdf46893830032a47a548019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924164"
---
# <a name="the-model-for-distributed-systems"></a>O modelo para sistemas distribuídos

Tradicionalmente, ter um sistema monolítico executado em vários computadores significa dividir o sistema em componentes separados do cliente e do servidor. Nesses sistemas, o componente cliente manipulava a interface do usuário e o servidor forneceu processamento de back-end, como acesso ao banco de dados, impressão e assim por diante. À medida que os computadores proliferam, rebaixam o custo e se conectam por redes de largura de banda cada vez maiores, a divisão de sistemas de software em vários componentes tornou-se mais conveniente, com cada componente em execução em um computador diferente e executando uma função especializada. Essa abordagem simplificou o desenvolvimento, o gerenciamento, a administração e, muitas vezes, melhorou o desempenho e a robustez, pois a falha em um computador não desabilitou necessariamente todo o sistema.

Em muitos casos, o sistema aparece para o cliente como uma nuvem opaca que executa as operações necessárias, embora o sistema distribuído seja composto por nós individuais, conforme ilustrado na figura a seguir.

![os clientes acessam serviços em um sistema de servidores rpc que aparece como uma nuvem opaca para clientes externos](images/indy-nodes.png)

A opacidade da nuvem é mantida porque as operações de computação são invocadas em nome do cliente. Assim, os clientes podem localizar um computador (um *nó*) dentro da nuvem e solicitar uma determinada operação; ao executar a operação, esse computador pode invocar a funcionalidade em outros computadores na nuvem sem expor as etapas adicionais ou o computador no qual eles foram executados, ao cliente.

Com esse paradigma, a mecânica de um sistema distribuído e parecido com a nuvem pode ser dividida em muitas trocas de pacotes individuais ou conversas entre nós individuais.

Sistemas cliente-servidor tradicionais têm dois nós com funções e responsabilidades fixas. Sistemas distribuídos modernos podem ter mais de dois nós e suas funções geralmente são dinâmicas. Em uma conversa, um nó pode ser um cliente, enquanto em outra conversa o nó pode ser o servidor. Em muitos casos, o consumidor final da funcionalidade exposta é um cliente com um usuário em um teclado, observando a saída. Em outros casos, o sistema distribuído funciona de forma autônoma, executando operações em segundo plano.

O sistema distribuído pode não ter clientes e servidores dedicados para cada troca de pacotes específica, mas é importante lembrar que há um chamador (ou iniciador, que geralmente é chamado de cliente). Também há o destinatário da chamada (geralmente conhecido como servidor). Não é necessário ter trocas de pacotes de duas vias no formato de solicitação-resposta de um sistema distribuído; geralmente, as mensagens são enviadas apenas de uma maneira.

 

 




