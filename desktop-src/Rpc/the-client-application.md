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
# <a name="the-client-application"></a><span data-ttu-id="f1df8-104">O aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="f1df8-104">The Client Application</span></span>

<span data-ttu-id="f1df8-105">O exemplo a seguir é do aplicativo "Olá, Mundo" no diretório RPC Hello do SDK (Kit de Desenvolvimento de Software de \\ Plataforma).</span><span class="sxs-lookup"><span data-stu-id="f1df8-105">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="f1df8-106">O arquivo de origem Helloc.c contém uma diretiva para incluir o arquivo de header gerado por MIDL, Hello.h.</span><span class="sxs-lookup"><span data-stu-id="f1df8-106">The Helloc.c source file contains a directive to include the MIDL-generated header file, Hello.h.</span></span> <span data-ttu-id="f1df8-107">No Hello.h, há diretivas para incluir Rpc.h e rpcndr.h, que contêm as definições para as rotinas de tempo de executar RPC, **HelloProc** e **Shutdown** e tipos de dados que os aplicativos cliente e servidor usam.</span><span class="sxs-lookup"><span data-stu-id="f1df8-107">Within Hello.h are directives to include Rpc.h and rpcndr.h, which contain the definitions for the RPC run-time routines, **HelloProc** and **Shutdown**, and data types that the client and server applications use.</span></span> <span data-ttu-id="f1df8-108">O compilador MIDL deve ser usado com o exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="f1df8-108">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="f1df8-109">Como o cliente está gerenciando sua conexão com o servidor, o aplicativo cliente chama funções em tempo de executar para estabelecer um alça para o servidor e para liberar esse lidar depois que as chamadas de procedimento remoto são concluídas.</span><span class="sxs-lookup"><span data-stu-id="f1df8-109">Because the client is managing its connection to the server, the client application calls run-time functions to establish a handle to the server and to release this handle after the remote procedure calls are complete.</span></span> <span data-ttu-id="f1df8-110">A função [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combina os componentes do alça de associação em uma representação de cadeia de caracteres desse manipular e aloca memória para a associação de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f1df8-110">The function [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combines the components of the binding handle into a string representation of that handle and allocates memory for the string binding.</span></span> <span data-ttu-id="f1df8-111">A função [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) cria um alça de associação de servidor, **hello \_ ClientIfHandle**, para o aplicativo cliente dessa representação de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f1df8-111">The function [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) creates a server binding handle, **hello\_ClientIfHandle**, for the client application from that string representation.</span></span>

<span data-ttu-id="f1df8-112">Na chamada para [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), os parâmetros não especificam o UUID porque este tutorial pressupõe que há apenas uma implementação da interface "hello".</span><span class="sxs-lookup"><span data-stu-id="f1df8-112">In the call to [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), the parameters do not specify the UUID because this tutorial assumes there is just one implementation of the interface "hello."</span></span> <span data-ttu-id="f1df8-113">Além disso, a chamada não especifica um endereço de rede porque o aplicativo usará o padrão, que é o computador host local.</span><span class="sxs-lookup"><span data-stu-id="f1df8-113">In addition, the call does not specify a network address because the application will use the default, which is the local host machine.</span></span> <span data-ttu-id="f1df8-114">A sequência de protocolo é uma cadeia de caracteres que representa o transporte de rede subjacente.</span><span class="sxs-lookup"><span data-stu-id="f1df8-114">The protocol sequence is a character string that represents the underlying network transport.</span></span> <span data-ttu-id="f1df8-115">O ponto de extremidade é um nome específico para a sequência de protocolo.</span><span class="sxs-lookup"><span data-stu-id="f1df8-115">The endpoint is a name which is specific to the protocol sequence.</span></span> <span data-ttu-id="f1df8-116">Este exemplo usa pipes nomeados para seu transporte de rede, portanto, a sequência de protocolo é "ncacn \_ np".</span><span class="sxs-lookup"><span data-stu-id="f1df8-116">This example uses named pipes for its network transport, so the protocol sequence is "ncacn\_np".</span></span> <span data-ttu-id="f1df8-117">O nome do ponto de extremidade é " \\ pipe \\ hello".</span><span class="sxs-lookup"><span data-stu-id="f1df8-117">The endpoint name is "\\pipe\\hello".</span></span>

<span data-ttu-id="f1df8-118">As chamadas de procedimento remoto real, **HelloProc** e **Shutdown,** ocorrem dentro do manipulador de exceção RPC – um conjunto de macros que permite controlar exceções que ocorrem fora do código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1df8-118">The actual remote procedure calls, **HelloProc** and **Shutdown**, take place within the RPC exception handler—a set of macros that let you control exceptions that occur outside the application code.</span></span> <span data-ttu-id="f1df8-119">Se o módulo de tempo de run time RPC relata uma exceção, o controle passa para o [**bloco RpcExcept.**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)</span><span class="sxs-lookup"><span data-stu-id="f1df8-119">If the RPC run-time module reports an exception, control passes to the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) block.</span></span> <span data-ttu-id="f1df8-120">É aqui que você inseriria o código para fazer qualquer limpeza necessária e, em seguida, saia normalmente.</span><span class="sxs-lookup"><span data-stu-id="f1df8-120">This is where you would insert code to do any needed cleanup and then exit gracefully.</span></span> <span data-ttu-id="f1df8-121">Este programa de exemplo simplesmente informa ao usuário que ocorreu uma exceção.</span><span class="sxs-lookup"><span data-stu-id="f1df8-121">This example program simply informs the user that an exception occurred.</span></span> <span data-ttu-id="f1df8-122">Se você não quiser usar exceções, poderá usar o status de [comm \_ ](/windows/desktop/Midl/comm-status) de atributos do ACF e o [status de \_ falha](/windows/desktop/Midl/fault-status) para relatar erros.</span><span class="sxs-lookup"><span data-stu-id="f1df8-122">If you do not want to use exceptions, you can use the ACF attributes [comm\_status](/windows/desktop/Midl/comm-status) and [fault\_status](/windows/desktop/Midl/fault-status) to report errors.</span></span>

<span data-ttu-id="f1df8-123">Depois que as chamadas de procedimento remoto são concluídas, o cliente primeiro chama [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para liberar a memória alocada para a associação de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f1df8-123">After the remote procedure calls are completed, the client first calls [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) to free the memory that was allocated for the string binding.</span></span> <span data-ttu-id="f1df8-124">Observe que, depois que o alça de associação tiver sido criado, um programa cliente poderá liberar uma associação de cadeia de caracteres a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="f1df8-124">Note that once the binding handle has been created, a client program can free a string binding at any time.</span></span> <span data-ttu-id="f1df8-125">Em seguida, o cliente [**chama RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) para liberar o handle.</span><span class="sxs-lookup"><span data-stu-id="f1df8-125">The client next calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to release the handle.</span></span>


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



 

 