---
title: O aplicativo de servidor
description: Veja a parte do aplicativo do servidor de um exemplo de RPC (chamada de procedimento remoto). O exemplo é do aplicativo "Olá, Mundo" no SDK da Plataforma.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b8a2bb66fd415a9b8f778134edb4903f88a717
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406059"
---
# <a name="the-server-application"></a>O aplicativo de servidor

O exemplo a seguir é do aplicativo "Olá, Mundo" no diretório RPC Hello do SDK (Kit de Desenvolvimento de Software de \\ Plataforma). O lado do servidor do aplicativo distribuído informa ao sistema que seus serviços estão disponíveis. Em seguida, ele aguarda solicitações do cliente. O compilador MIDL deve ser usado com o exemplo abaixo.

Dependendo do tamanho do aplicativo e das preferências de codificação, você pode optar por implementar procedimentos remotos em um ou mais arquivos separados. Neste programa de tutorial, o arquivo de origem Hellos.c contém a rotina principal do servidor. O arquivo Hellop.c contém o procedimento remoto.

O benefício de organizar os procedimentos remotos em arquivos separados é que os procedimentos podem ser vinculados a um programa autônomo para depurar o código antes que ele seja convertido em um aplicativo distribuído. Depois que os procedimentos funcionarem no programa autônomo, você poderá compilar e vincular os arquivos de origem que contêm os procedimentos remotos com o aplicativo de servidor. Assim como no arquivo de origem do aplicativo cliente, o arquivo de origem do aplicativo de servidor deve incluir o arquivo de header Hello.h.

O servidor chama as funções de tempo de run time [**RPC RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) e [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para disponibilizar informações de associação ao cliente. Este programa de exemplo passa o nome do alça de interface **para RpcServerRegisterIf.** Os outros parâmetros são definidos como **NULL.** Em seguida, o servidor chama a [**função RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para indicar que está aguardando solicitações do cliente.

O aplicativo de servidor também deve incluir as duas funções de gerenciamento de memória chamadas pelo stub do servidor: [**midl \_ user \_ allocate**](the-midl-user-allocate-function.md) e [**midl \_ user \_ free.**](the-midl-user-free-function.md) Essas funções alocam e liberam memória no servidor quando um procedimento remoto passa parâmetros para o servidor. Neste programa de exemplo, **\_ \_ alocar** usuário médio e usuário **midl \_ \_** gratuito são simplesmente wrappers para as funções de biblioteca C [**malloc**](pointers-and-memory-allocation.md) e **free**. (Observe que, nas declarações de encaminhamento geradas pelo compilador MIDL, "MIDL" está em letras maiúsculas. O arquivo de header Rpcndr.h define o usuário midl gratuito e o usuário médio alocado para ser usuário MIDL gratuito e alocar usuário \_ \_ \_ \_ \_ \_ \_ MIDL, \_ respectivamente.)


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



 

 




