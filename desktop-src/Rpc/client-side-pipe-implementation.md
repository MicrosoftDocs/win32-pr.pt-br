---
title: Implementação de pipe de Client-Side
description: Implementação de pipe do lado do cliente na chamada de procedimento remoto (RPC).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822902"
---
# <a name="client-side-pipe-implementation"></a>Implementação de pipe de Client-Side

O aplicativo cliente deve implementar os seguintes procedimentos, que o stub do cliente chamará durante a transferência de dados:

-   Um procedimento de pull (para um pipe de entrada)
-   Um procedimento de push (para um pipe de saída)
-   Um procedimento de alocação para alocar um buffer para os dados de transferência

Todos esses procedimentos devem usar os argumentos especificados pelo arquivo de cabeçalho gerado por MIDL. Além disso, o aplicativo cliente deve ter uma variável de estado para identificar onde localizar ou colocar os dados.

O procedimento de alocação também pode ser simples ou tão complexo quanto necessário. Por exemplo, ele pode retornar um ponteiro para o mesmo buffer sempre que o stub chamar a função, ou pode alocar uma quantidade de memória diferente a cada vez. Se os dados já estiverem no formato adequado (uma matriz de elementos de pipe, por exemplo), você poderá coordenar o procedimento de alocação com o procedimento de pull para alocar um buffer que já contém os dados. Nesse caso, o procedimento de pull pode ser uma rotina vazia.

A alocação de buffer deve estar em bytes. Os procedimentos de push e pull, por outro lado, manipulam elementos, cujo tamanho em bytes depende de como eles foram definidos.

Esta seção aborda a implementação do cliente de pipes de entrada e saída nas seguintes seções:

-   [Implementando pipes de entrada no cliente](implementing-input-pipes-on-the-client.md)
-   [Implementando os pipes de saída no cliente](implementing-output-pipes-on-the-client.md)

 

 




