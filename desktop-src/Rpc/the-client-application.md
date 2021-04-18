---
title: O aplicativo cliente
description: O exemplo a seguir é do aplicativo ' Olá, Mundo ' no diretório RPC \\ Hello do SDK (Software Development Kit) da plataforma.
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f97c7c35e00d3f36c645bfad2825dbada5e3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454295"
---
# <a name="the-client-application"></a>O aplicativo cliente

O exemplo a seguir é do aplicativo ' Olá, Mundo ' no diretório RPC \\ Hello do SDK (Software Development Kit) da plataforma. O arquivo de origem Helloc. c contém uma diretiva para incluir o arquivo de cabeçalho gerado por MIDL, Olá. h. No Hello. h estão as diretivas para incluir RPC. h e Rpcndr. h, que contêm as definições para as rotinas de tempo de execução RPC, **HelloProc** e **Shutdown**, e os tipos de dados que os aplicativos cliente e servidor usam. O compilador MIDL deve ser usado com o exemplo abaixo.

Como o cliente está gerenciando sua conexão com o servidor, o aplicativo cliente chama funções de tempo de execução para estabelecer um identificador para o servidor e liberar esse identificador depois que as chamadas de procedimento remoto forem concluídas. A função [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combina os componentes do identificador de ligação em uma representação de cadeia de caracteres desse identificador e aloca memória para a associação de cadeia de caracteres. A função [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) cria um identificador de associação de servidor, **Olá \_ ClientIfHandle**, para o aplicativo cliente dessa representação de cadeia de caracteres.

Na chamada de [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), os parâmetros não especificam o UUID porque este tutorial pressupõe que há apenas uma implementação da interface "Hello". Além disso, a chamada não especifica um endereço de rede porque o aplicativo usará o padrão, que é o computador host local. A sequência de protocolo é uma cadeia de caracteres que representa o transporte de rede subjacente. O ponto de extremidade é um nome que é específico para a sequência de protocolo. Este exemplo usa pipes nomeados para seu transporte de rede, portanto, a sequência de protocolo é "ncacn \_ NP". O nome do ponto de extremidade é " \\ pipe de \\ saudação".

As chamadas de procedimento remoto, **HelloProc** e **Shutdown**, ocorrem dentro do manipulador de exceção RPC — um conjunto de macros que permitem controlar as exceções que ocorrem fora do código do aplicativo. Se o módulo de tempo de execução RPC reportar uma exceção, o controle passará para o bloco [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) . É aí que você deve inserir o código para fazer qualquer limpeza necessária e sair normalmente. Esse programa de exemplo simplesmente informa ao usuário que ocorreu uma exceção. Se você não quiser usar exceções, poderá usar os atributos de ACF status de [comunicação \_ ](/windows/desktop/Midl/comm-status) e [ \_ status de falha](/windows/desktop/Midl/fault-status) para relatar erros.

Depois que as chamadas de procedimento remoto são concluídas, o cliente primeiro chama [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para liberar a memória que foi alocada para a associação de cadeia de caracteres. Observe que depois que o identificador de associação tiver sido criado, um programa cliente poderá liberar uma associação de cadeia de caracteres a qualquer momento. Em seguida, o cliente chama [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) para liberar o identificador.


```C++
/* file: helloc.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h" 
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszUuid             = NULL;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszNetworkAddress   = NULL;
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned char * pszOptions          = NULL;
    unsigned char * pszStringBinding    = NULL;
    unsigned char * pszString           = "hello, world";
    unsigned long ulCode;
 
    status = RpcStringBindingCompose(pszUuid,
                                     pszProtocolSequence,
                                     pszNetworkAddress,
                                     pszEndpoint,
                                     pszOptions,
                                     &pszStringBinding);
    if (status) exit(status);

    status = RpcBindingFromStringBinding(pszStringBinding, &hello_ClientIfHandle);
 
    if (status) exit(status);
 
    RpcTryExcept  
    {
        HelloProc(pszString);
        Shutdown();
    }
    RpcExcept(1) 
    {
        ulCode = RpcExceptionCode();
        printf("Runtime reported exception 0x%lx = %ld\n", ulCode, ulCode);
    }
    RpcEndExcept
 
    status = RpcStringFree(&pszStringBinding); 
 
    if (status) exit(status);
 
    status = RpcBindingFree(&hello_IfHandle);
 
    if (status) exit(status);

    exit(0);
}

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 