---
title: Gravando um cliente SSPI autenticado
description: Gravar um cliente SSPI autenticado e RPC (chamada de procedimento remoto).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- RPC de chamada de procedimento remoto, tarefas, gravando um cliente SSPI autenticado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8476772a2ed652f6646b078c2876234cbcc0d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084737"
---
# <a name="writing-an-authenticated-sspi-client"></a>Gravando um cliente SSPI autenticado

Todas as sessões de cliente/servidor RPC exigem uma associação entre o cliente e o servidor. Para adicionar segurança a aplicativos cliente/servidor, os programas devem usar uma associação autenticada. Esta seção descreve o processo de criação de uma associação autenticada entre o cliente e o servidor.

-   [Criando identificadores de associação do lado do cliente](#creating-client-side-binding-handles)
-   [Fornecendo credenciais de cliente ao servidor](#providing-client-credentials-to-the-server)

Para obter informações relacionadas, consulte os [procedimentos usados com a maioria dos pacotes de segurança e protocolos](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) no SDK (Software Development Kit) da plataforma.

## <a name="creating-client-side-binding-handles"></a>Criando identificadores de associação do lado do cliente

Para criar uma sessão autenticada com um programa de servidor, os aplicativos cliente devem fornecer informações de autenticação com seu identificador de ligação. Para configurar um identificador de associação autenticado, os clientes invocam a função [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) . Essas duas funções são quase idênticas. A única diferença entre eles é que o cliente pode especificar a qualidade do serviço com a função **RpcBindingSetAuthInfoEx** .

O fragmento de código a seguir mostra como uma chamada para [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) pode parecer.


```C++
// This code fragment assumes that rpcBinding is a valid binding 
// handle between the client and the server. It also assumes that
// pAuthCredentials is a valid pointer to a data structure which
// contains the user's authentication credentials.

dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

//...

rpcStatus = RpcBindingSetAuthInfo(
    rpcBinding,                       // Valid binding handle
    pszSpn,                           // Principal name 
    RPC_C_AUTHN_LEVEL_PKT_INTEGRITY,  // Authentication level
    RPC_C_AUTHN_GSS_NEGOTIATE,        // Use Negotiate SSP
    NULL,                             // Authentication credentials <entity type="ndash"/> use current thread credentials
    RPC_C_AUTHZ_NAME);                // Authorization service
```



Depois que o cliente chama com êxito as funções [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) , a biblioteca de tempo de execução RPC autentica automaticamente todas as chamadas RPC na associação. O nível de segurança e autenticação que o cliente seleciona aplica somente a esse identificador de ligação. Os identificadores de contexto derivados do identificador de associação usarão as mesmas informações de segurança, mas as modificações subsequentes no identificador de associação não serão refletidas nas alças de contexto. Para obter mais informações, consulte [identificadores de contexto](context-handles.md).

O nível de autenticação permanece em vigor até que o cliente escolha outro nível, ou até que o processo seja encerrado. A maioria dos aplicativos não exigirá uma alteração no nível de segurança. O cliente pode consultar qualquer identificador de ligação para obter suas informações de autorização invocando [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) e passando o identificador de ligação.

## <a name="providing-client-credentials-to-the-server"></a>Fornecendo credenciais de cliente ao servidor

Os servidores usam as informações de associação do cliente para impor a segurança. Os clientes sempre passam um identificador de associação como o primeiro parâmetro de uma chamada de procedimento remoto. No entanto, os servidores não podem usar o identificador, a menos que ele seja declarado como o primeiro parâmetro para procedimentos remotos no arquivo IDL ou no arquivo de configuração de aplicativo (ACF) do servidor. Você pode optar por listar o identificador de associação no arquivo IDL, mas isso forçará todos os clientes a declarar e manipular o identificador de associação em vez de usar a associação automática ou implícita. Para obter mais informações, consulte [os arquivos IDL e ACF](the-idl-and-acf-files.md).

Outro método é deixar os identificadores de associação fora do arquivo IDL e colocar o atributo **\_ identificador explícito** no ACF do servidor. Dessa forma, o cliente pode usar o tipo de associação mais adequado para o aplicativo, enquanto o servidor usa o identificador de associação como se ele fosse declarado explicitamente.

O processo de extração das credenciais do cliente do identificador de associação ocorre da seguinte maneira:

-   Os clientes RPC chamam [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) e incluem suas informações de autenticação como parte das informações de associação passadas para o servidor.
-   Normalmente, o servidor chama [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) para se comportar como se fosse o cliente. Se o identificador de associação não for autenticado, a chamada falhará com RPC \_ S \_ nenhum \_ contexto \_ disponível. Para obter o nome de usuário do cliente, chame [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) enquanto estiver representando ou no Windows XP ou em versões posteriores do Windows, chame [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) para obter o contexto de autorização e, em seguida, use as funções AuthZ para recuperar o nome.
-   Normalmente, o servidor chamará [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) para criar objetos com ACLs. Depois que isso for feito, as verificações de segurança posteriores se tornarão automáticas.

 

 