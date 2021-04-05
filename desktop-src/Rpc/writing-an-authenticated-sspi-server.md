---
title: Gravando um servidor SSPI autenticado
description: Antes que a comunicação autenticada possa ocorrer entre os programas cliente e servidor, o servidor deve registrar suas informações de autenticação.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- RPC de chamada de procedimento remoto, tarefas, gravando um servidor SSPI autenticado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b1cb06cfc626bc8130f3c4b0cee0a7b6d7893e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005469"
---
# <a name="writing-an-authenticated-sspi-server"></a>Gravando um servidor SSPI autenticado

Antes que a comunicação autenticada possa ocorrer entre os programas cliente e servidor, o servidor deve registrar suas informações de autenticação. Em particular, o servidor deve registrar seu nome principal e especificar o serviço de autenticação que ele usa. Para obter mais informações sobre nomes de entidade de segurança, consulte [nomes de entidade de segurança](principal-names.md). Para obter detalhes sobre os serviços de autenticação, consulte [serviços de autenticação](authentication-services.md).

Para registrar suas informações de autenticação, os servidores chamam a função [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) . Passe um ponteiro para o nome da entidade de segurança como o valor do primeiro parâmetro. Defina o segundo parâmetro como uma constante que indica o serviço de autenticação que o aplicativo usará. Para obter uma descrição dos serviços de autenticação, consulte as [constantes de serviço de autenticação](authentication-service-constants.md).

O servidor também pode passar o endereço de uma função de aquisição de chave como o valor do terceiro parâmetro. Consulte [funções de aquisição de chave](key-acquisition-functions.md). Para usar a função de aquisição de chave padrão para o serviço de autenticação selecionado, defina o terceiro parâmetro como **nulo**. O último parâmetro para a função [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) é um ponteiro de dados para passar para a função de aquisição de chave, se você fornecer uma função de aquisição de chave. Uma chamada para **RpcServerRegisterAuthInfo** é mostrada no fragmento de código a seguir.


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



Além disso, o servidor pode fornecer a biblioteca de tempo de execução RPC com uma função de autorização. Para definir uma função de autorização, chame a função [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) .

A parte do servidor de um aplicativo distribuído pode chamar a função [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) ou [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) para consultar um identificador de associação para obter informações de autenticação.

Se o seu servidor se registrar com um provedor de suporte de segurança, as chamadas de cliente com credenciais inválidas não serão expedidas. No entanto, chamadas sem credenciais serão expedidas. Há três maneiras de evitar que isso aconteça:

-   Registrar a interface usando [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), com uma função de retorno de chamada de segurança; Isso fará com que a biblioteca de tempo de execução RPC rejeite automaticamente as chamadas não autenticadas para essa interface. O registro de uma função de retorno de chamada é compatível com outros métodos de verificação de credenciais de acesso; a função de retorno de chamada pode chamar as funções [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)ou [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) , ou outras. No entanto, essas funções não podem usar os argumentos passados para a função, pois eles não são desempacotados nesse ponto.

> [!IMPORTANT]
> Registrar a interface usando o [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) com uma função de retorno de chamada de segurança é o método mais intensamente recomendado para verificar as credenciais do cliente.

 

-   Chame [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) para determinar o nível de segurança que o cliente está usando. Seu stub poderá retornar um erro se o cliente não estiver autenticado.

 

 




