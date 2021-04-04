---
title: O aplicativo de servidor
description: O exemplo a seguir é do aplicativo ' Olá, Mundo ' no diretório RPC \\ Hello do SDK (Software Development Kit) da plataforma.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6f13e2c8fecdcff820c62f3076dd2a8edd1a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822658"
---
# <a name="the-server-application"></a>O aplicativo de servidor

O exemplo a seguir é do aplicativo ' Olá, Mundo ' no diretório RPC \\ Hello do SDK (Software Development Kit) da plataforma. O lado do servidor do aplicativo distribuído informa ao sistema que seus serviços estão disponíveis. Em seguida, ele aguarda as solicitações do cliente. O compilador MIDL deve ser usado com o exemplo abaixo.

Dependendo do tamanho do seu aplicativo e das suas preferências de codificação, você pode optar por implementar procedimentos remotos em um ou mais arquivos separados. Neste programa tutorial, o arquivo de origem hellos. c contém a rotina de servidor principal. O arquivo Hellop. c contém o procedimento remoto.

O benefício de organizar os procedimentos remotos em arquivos separados é que os procedimentos podem ser vinculados a um programa autônomo para depurar o código antes que ele seja convertido em um aplicativo distribuído. Depois que os procedimentos funcionam no programa autônomo, você pode compilar e vincular os arquivos de origem que contêm os procedimentos remotos com o aplicativo de servidor. Assim como no arquivo de origem do aplicativo cliente, o arquivo de origem do aplicativo do servidor deve incluir o arquivo de cabeçalho Hello. h.

O servidor chama as funções de tempo de execução RPC [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) e [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para tornar as informações de associação disponíveis para o cliente. Este programa de exemplo passa o nome do identificador de interface para **RpcServerRegisterIf**. Os outros parâmetros são definidos como **NULL**. Em seguida, o servidor chama a função [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para indicar que está aguardando as solicitações do cliente.

O aplicativo de servidor também deve incluir as duas funções de gerenciamento de memória que o stub de servidor chama: [**\_ \_ alocar usuário**](the-midl-user-allocate-function.md) de MIDL e [**usuário de MIDL \_ \_ gratuito**](the-midl-user-free-function.md). Essas funções alocam e liberam memória no servidor quando um procedimento remoto passa parâmetros para o servidor. Neste programa de exemplo, **o \_ usuário \_ de MIDL Allocate** e o **usuário de MIDL \_ \_ Free** são simplesmente invólucros para as funções [**malloc**](pointers-and-memory-allocation.md) e **Free** da biblioteca C. (Observe que, nas declarações de encaminhamento geradas pelo compilador MIDL, "MIDL" é maiúsculo. O arquivo de cabeçalho Rpcndr. h define o \_ usuário MIDL \_ gratuito e o \_ usuário de MIDL \_ alocar para ser o \_ usuário MIDL \_ gratuito e o \_ usuário MIDL \_ ALLOCATE, respectivamente.)


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
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



 

 




