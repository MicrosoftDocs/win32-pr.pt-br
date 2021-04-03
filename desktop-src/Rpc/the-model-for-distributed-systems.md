---
title: O modelo para sistemas distribuídos
description: Tradicionalmente, ter um sistema monolítico executado em vários computadores significava dividir o sistema em componentes de cliente e servidor separados.
ms.assetid: 6055bcef-e34c-4f2d-92b9-9aec75cf3cec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cd1ea3301d68e77562a63c542bc075692e5192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916100"
---
# <a name="the-model-for-distributed-systems"></a>O modelo para sistemas distribuídos

Tradicionalmente, ter um sistema monolítico executado em vários computadores significava dividir o sistema em componentes de cliente e servidor separados. Nesses sistemas, o componente cliente tratou a interface do usuário e o processamento de back-end fornecido pelo servidor, como acesso ao banco de dados, impressão e assim por diante. À medida que os computadores proliferaram, descartaram custos e se tornaram conectados por redes de largura de banda cada vez mais altas, dividir os sistemas de software em vários componentes se tornou mais conveniente, com cada componente em execução em um computador diferente e executando uma função especializada. Essa abordagem simplificava o desenvolvimento, o gerenciamento, a administração e, muitas vezes, o desempenho e a robustez aprimorados, uma vez que a falha em um computador não desabilitou necessariamente o sistema inteiro.

Em muitos casos, o sistema aparece para o cliente como uma nuvem opaca que executa as operações necessárias, embora o sistema distribuído seja composto por nós individuais, conforme ilustrado na figura a seguir.

![Os clientes acessam serviços em um sistema de servidores RPC que aparece como uma nuvem opaca para clientes externos](images/indy-nodes.png)

A opacidade da nuvem é mantida porque as operações de computação são invocadas em nome do cliente. Assim, os clientes podem localizar um computador (um *nó*) na nuvem e solicitar uma determinada operação; ao executar a operação, esse computador pode invocar a funcionalidade em outros computadores na nuvem sem expor as etapas adicionais ou o computador no qual eles foram executados, para o cliente.

Com esse paradigma, a mecânica de um sistema distribuído, semelhante à nuvem, pode ser dividida em muitas trocas de pacotes individuais ou conversas entre nós individuais.

Os sistemas cliente-servidor tradicionais têm dois nós com funções e responsabilidades fixas. Os sistemas distribuídos modernos podem ter mais de dois nós, e suas funções são geralmente dinâmicas. Em uma conversa, um nó pode ser um cliente, enquanto em outra conversa o nó pode ser o servidor. Em muitos casos, o consumidor final da funcionalidade exposta é um cliente com um usuário que está sentado em um teclado, assistindo à saída. Em outros casos, as funções de sistema distribuído autônomas, executando operações em segundo plano.

O sistema distribuído pode não ter clientes e servidores dedicados para cada troca de pacotes em particular, mas é importante lembrar que há um chamador, (ou iniciador, que é geralmente referido como o cliente). Também há o destinatário da chamada (geralmente chamado de servidor). Não é necessário ter trocas de pacotes de duas vias no formato de solicitação-resposta de um sistema distribuído; muitas vezes, as mensagens são enviadas apenas uma delas.

 

 




