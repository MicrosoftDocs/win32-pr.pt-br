---
title: Indicar erros por exceções
description: Para programadores C tradicionais, os erros são normalmente retornados por meio de valores de retorno ou um parâmetro "out \" especial que retorna o código de erro.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 816f63f9378c3f2338c7bed6f6a9b5f785d3e138e4762c355aa1932887fd14c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928912"
---
# <a name="indicate-errors-by-exceptions"></a>Indicar erros por exceções

Para programadores C tradicionais, os erros são normalmente retornados por meio de valores de retorno ou um \[ parâmetro de saída especial \] que retorna o código de erro. Isso leva a interfaces implementadas da seguinte maneira:

``` syntax
long sample(...)
{
    ...
    p = new Cbar(...);
    if (p == NULL)
    {
        // cleanup
        ...
        return ERROR_OUTOFMEMORY;
    }
}
```

O problema dessa abordagem é que os valores de retorno de RPC são simplesmente inteiros longos. Eles não têm um significado especial como erros (Observe que o [**status de erro \_ \_ t**](/windows/desktop/Midl/error-status-t) não tem semântica especial no lado do servidor), o que transporta implicações importantes.

Primeiro, o RPC não é alertado de que a operação falhou; Ele tenta desempacotar todos os \[ argumentos de entrada, saída \] e \[ saída \] . A semântica de falha dos identificadores de contexto também é diferente. O pacote retornado para o cliente é essencialmente um pacote de êxito, com o código de erro enterrado em profundidade no pacote. Isso também significa que o RPC não usa informações de erro estendidas, portanto, o software cliente geralmente não é capaz de distinguir onde a chamada falhou.

Indicar erros nas rotinas do servidor RPC lançando Exceções SEH (manipulação de exceção estruturada) (e não C++) é uma abordagem muito melhor. Quando uma exceção SEH é gerada, o controle vai diretamente para o tempo de execução RPC. Às vezes, um erro ocorre em uma rotina que não pode ser limpa corretamente e precisa indicar um erro para seu chamador. A rotina deve retornar um erro para seu chamador, que, por sua vez, pode retornar um erro para seu chamador e assim por diante. No entanto, a última rotina de servidor na pilha deve lançar uma exceção antes que ela retorne ao RPC para indicar ao RPC que ocorreu um erro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de exceção](exception-handling.md)
</dt> </dl>

 

 