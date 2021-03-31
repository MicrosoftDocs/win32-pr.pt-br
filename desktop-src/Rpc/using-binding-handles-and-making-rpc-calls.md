---
title: Usando identificadores de associação e fazendo chamadas RPC
description: Um erro comum entre os programadores de RPC é A manipulação de todas as exceções.
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b285fc3030b92e2616c850bf79c73e37f0341c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641487"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a>Usando identificadores de associação e fazendo chamadas RPC

Um erro comum entre os programadores de RPC é A manipulação de todas as exceções. Muitos programadores estruturam seus identificadores de exceção como o seguinte:

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    RpcExcept(1)
        {
        log an error or do something else
        }
    RpcEndExcept
```

O problema com esse manipulador é que ele captura todos os erros, incluindo erros no programa cliente. A captura de erros no programa cliente torna a depuração mais difícil. A maneira apropriada de estruturar um manipulador de exceção é a seguinte:

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    // Return "non-fatal" errors to clients.  Catching fatal errors
    // makes it harder to debug.
    RpcExcept( ( ( (RpcExceptionCode() != STATUS_ACCESS_VIOLATION) &&
                   (RpcExceptionCode() != STATUS_POSSIBLE_DEADLOCK) &&
                   (RpcExceptionCode() != STATUS_INSTRUCTION_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_DATATYPE_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_PRIVILEGED_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_ILLEGAL_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_BREAKPOINT) &&
                   (RpcExceptionCode() != STATUS_STACK_OVERFLOW) &&
                   (RpcExceptionCode() != STATUS_HANDLE_NOT_CLOSABLE) &&
                   (RpcExceptionCode() != STATUS_IN_PAGE_ERROR) &&
                   (RpcExceptionCode() != STATUS_ASSERTION_FAILURE) &&
                   (RpcExceptionCode() != STATUS_STACK_BUFFER_OVERRUN) &&
                   (RpcExceptionCode() != STATUS_GUARD_PAGE_VIOLATION)
                    )
                    ? EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH ) )
        {
        log an error or do something else
        }
    RpcEndExcept
```

Esse manipulador de exceção tem a vantagem de permitir um determinado intervalo de erros por meio do. Esses erros nunca serão retornados pelo servidor, pois eles indicam um problema no lado do cliente.

Além disso, o uso do **\[** [ \_ \_ identificador de contexto estrito](/windows/desktop/Midl/strict-context-handle) **\]** e o tipo de atributos de **\[** [ \_ \_ \_ identificador de contexto estrito](/windows/desktop/Midl/type-strict-context-handle) **\]** são recomendados para garantir que o tempo de execução de RPC crie um identificador de contexto em uma interface que possa ser passada como um argumento somente para métodos dessa interface. Isso impedirá falhas de servidor que ocorrem quando os identificadores de contexto são abertos e passados entre diferentes interfaces que existem dentro do mesmo processo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_identificador de contexto estrito \_](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[tipo \_ de \_ identificador de contexto estrito \_](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 