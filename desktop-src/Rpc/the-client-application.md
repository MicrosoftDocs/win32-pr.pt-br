---
title: O aplicativo cliente
description: Veja a parte do aplicativo cliente de um exemplo de RPC (chamada de procedimento remoto). O exemplo a seguir é do aplicativo "Olá, Mundo" no SDK da Plataforma.
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e0b798543cd70e61f3ff1161503fa64710e53e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405009"
---
# <a name="the-client-application"></a>O aplicativo cliente

O exemplo a seguir é do aplicativo "Olá, Mundo" no diretório RPC Hello do SDK (Kit de Desenvolvimento de Software de \\ Plataforma). O arquivo de origem Helloc.c contém uma diretiva para incluir o arquivo de header gerado por MIDL, Hello.h. No Hello.h, há diretivas para incluir Rpc.h e rpcndr.h, que contêm as definições para as rotinas de tempo de executar RPC, **HelloProc** e **Shutdown** e tipos de dados que os aplicativos cliente e servidor usam. O compilador MIDL deve ser usado com o exemplo abaixo.

Como o cliente está gerenciando sua conexão com o servidor, o aplicativo cliente chama funções em tempo de executar para estabelecer um alça para o servidor e para liberar esse lidar depois que as chamadas de procedimento remoto são concluídas. A função [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combina os componentes do alça de associação em uma representação de cadeia de caracteres desse manipular e aloca memória para a associação de cadeia de caracteres. A função [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) cria um alça de associação de servidor, **hello \_ ClientIfHandle**, para o aplicativo cliente dessa representação de cadeia de caracteres.

Na chamada para [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), os parâmetros não especificam o UUID porque este tutorial pressupõe que há apenas uma implementação da interface "hello". Além disso, a chamada não especifica um endereço de rede porque o aplicativo usará o padrão, que é o computador host local. A sequência de protocolo é uma cadeia de caracteres que representa o transporte de rede subjacente. O ponto de extremidade é um nome específico para a sequência de protocolo. Este exemplo usa pipes nomeados para seu transporte de rede, portanto, a sequência de protocolo é "ncacn \_ np". O nome do ponto de extremidade é " \\ pipe \\ hello".

As chamadas de procedimento remoto real, **HelloProc** e **Shutdown,** ocorrem dentro do manipulador de exceção RPC – um conjunto de macros que permite controlar exceções que ocorrem fora do código do aplicativo. Se o módulo de tempo de run time RPC relata uma exceção, o controle passa para o [**bloco RpcExcept.**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) É aqui que você inseriria o código para fazer qualquer limpeza necessária e, em seguida, saia normalmente. Este programa de exemplo simplesmente informa ao usuário que ocorreu uma exceção. Se você não quiser usar exceções, poderá usar o status de [comm \_ ](/windows/desktop/Midl/comm-status) de atributos do ACF e o [status de \_ falha](/windows/desktop/Midl/fault-status) para relatar erros.

Depois que as chamadas de procedimento remoto são concluídas, o cliente primeiro chama [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para liberar a memória alocada para a associação de cadeia de caracteres. Observe que, depois que o alça de associação tiver sido criado, um programa cliente poderá liberar uma associação de cadeia de caracteres a qualquer momento. Em seguida, o cliente [**chama RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) para liberar o handle.


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



 

 