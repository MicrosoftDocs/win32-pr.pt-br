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
# <a name="writing-an-authenticated-sspi-client"></a><span data-ttu-id="3844b-104">Gravando um cliente SSPI autenticado</span><span class="sxs-lookup"><span data-stu-id="3844b-104">Writing an Authenticated SSPI Client</span></span>

<span data-ttu-id="3844b-105">Todas as sessões de cliente/servidor RPC exigem uma associação entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="3844b-105">All RPC client/server sessions require a binding between the client and the server.</span></span> <span data-ttu-id="3844b-106">Para adicionar segurança a aplicativos cliente/servidor, os programas devem usar uma associação autenticada.</span><span class="sxs-lookup"><span data-stu-id="3844b-106">To add security to client/server applications, the programs must use an authenticated binding.</span></span> <span data-ttu-id="3844b-107">Esta seção descreve o processo de criação de uma associação autenticada entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="3844b-107">This section describes the process of creating an authenticated binding between the client and the server.</span></span>

-   [<span data-ttu-id="3844b-108">Criando identificadores de associação do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="3844b-108">Creating Client-side Binding Handles</span></span>](#creating-client-side-binding-handles)
-   [<span data-ttu-id="3844b-109">Fornecendo credenciais de cliente ao servidor</span><span class="sxs-lookup"><span data-stu-id="3844b-109">Providing Client Credentials to the Server</span></span>](#providing-client-credentials-to-the-server)

<span data-ttu-id="3844b-110">Para obter informações relacionadas, consulte os [procedimentos usados com a maioria dos pacotes de segurança e protocolos](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) no SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="3844b-110">For related information, see [Procedures Used with Most Security Packages and Protocols](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) in the Platform Software Development Kit (SDK).</span></span>

## <a name="creating-client-side-binding-handles"></a><span data-ttu-id="3844b-111">Criando identificadores de associação do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="3844b-111">Creating Client-side Binding Handles</span></span>

<span data-ttu-id="3844b-112">Para criar uma sessão autenticada com um programa de servidor, os aplicativos cliente devem fornecer informações de autenticação com seu identificador de ligação.</span><span class="sxs-lookup"><span data-stu-id="3844b-112">To create an authenticated session with a server program, client applications must provide authentication information with their binding handle.</span></span> <span data-ttu-id="3844b-113">Para configurar um identificador de associação autenticado, os clientes invocam a função [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) .</span><span class="sxs-lookup"><span data-stu-id="3844b-113">To set up an authenticated binding handle, clients invoke the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function.</span></span> <span data-ttu-id="3844b-114">Essas duas funções são quase idênticas.</span><span class="sxs-lookup"><span data-stu-id="3844b-114">These two functions are nearly identical.</span></span> <span data-ttu-id="3844b-115">A única diferença entre eles é que o cliente pode especificar a qualidade do serviço com a função **RpcBindingSetAuthInfoEx** .</span><span class="sxs-lookup"><span data-stu-id="3844b-115">The only difference between them is that the client can specify the quality of service with the **RpcBindingSetAuthInfoEx** function.</span></span>

<span data-ttu-id="3844b-116">O fragmento de código a seguir mostra como uma chamada para [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) pode parecer.</span><span class="sxs-lookup"><span data-stu-id="3844b-116">The following code fragment shows how a call to [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) might look.</span></span>


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



<span data-ttu-id="3844b-117">Depois que o cliente chama com êxito as funções [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) ou [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) , a biblioteca de tempo de execução RPC autentica automaticamente todas as chamadas RPC na associação.</span><span class="sxs-lookup"><span data-stu-id="3844b-117">After the client successfully calls the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) functions, the RPC run-time library automatically authenticates all RPC calls on the binding.</span></span> <span data-ttu-id="3844b-118">O nível de segurança e autenticação que o cliente seleciona aplica somente a esse identificador de ligação.</span><span class="sxs-lookup"><span data-stu-id="3844b-118">The level of security and authentication that the client selects applies only to that binding handle.</span></span> <span data-ttu-id="3844b-119">Os identificadores de contexto derivados do identificador de associação usarão as mesmas informações de segurança, mas as modificações subsequentes no identificador de associação não serão refletidas nas alças de contexto.</span><span class="sxs-lookup"><span data-stu-id="3844b-119">Context handles derived from the binding handle will use the same security information, but subsequent modifications to the binding handle will not be reflected in the context handles.</span></span> <span data-ttu-id="3844b-120">Para obter mais informações, consulte [identificadores de contexto](context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="3844b-120">For more information, see [Context Handles](context-handles.md).</span></span>

<span data-ttu-id="3844b-121">O nível de autenticação permanece em vigor até que o cliente escolha outro nível, ou até que o processo seja encerrado.</span><span class="sxs-lookup"><span data-stu-id="3844b-121">The authentication level stays in effect until the client chooses another level, or until the process terminates.</span></span> <span data-ttu-id="3844b-122">A maioria dos aplicativos não exigirá uma alteração no nível de segurança.</span><span class="sxs-lookup"><span data-stu-id="3844b-122">Most applications will not require a change in the security level.</span></span> <span data-ttu-id="3844b-123">O cliente pode consultar qualquer identificador de ligação para obter suas informações de autorização invocando [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) e passando o identificador de ligação.</span><span class="sxs-lookup"><span data-stu-id="3844b-123">The client can query any binding handle to obtain its authorization information by invoking [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) and passing it the binding handle.</span></span>

## <a name="providing-client-credentials-to-the-server"></a><span data-ttu-id="3844b-124">Fornecendo credenciais de cliente ao servidor</span><span class="sxs-lookup"><span data-stu-id="3844b-124">Providing Client Credentials to the Server</span></span>

<span data-ttu-id="3844b-125">Os servidores usam as informações de associação do cliente para impor a segurança.</span><span class="sxs-lookup"><span data-stu-id="3844b-125">Servers use the client's binding information to enforce security.</span></span> <span data-ttu-id="3844b-126">Os clientes sempre passam um identificador de associação como o primeiro parâmetro de uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="3844b-126">Clients always pass a binding handle as the first parameter of a remote procedure call.</span></span> <span data-ttu-id="3844b-127">No entanto, os servidores não podem usar o identificador, a menos que ele seja declarado como o primeiro parâmetro para procedimentos remotos no arquivo IDL ou no arquivo de configuração de aplicativo (ACF) do servidor.</span><span class="sxs-lookup"><span data-stu-id="3844b-127">However, servers cannot use the handle unless it is declared as the first parameter to remote procedures in either the IDL file or in the server's application configuration file (ACF).</span></span> <span data-ttu-id="3844b-128">Você pode optar por listar o identificador de associação no arquivo IDL, mas isso forçará todos os clientes a declarar e manipular o identificador de associação em vez de usar a associação automática ou implícita.</span><span class="sxs-lookup"><span data-stu-id="3844b-128">You can choose to list the binding handle in the IDL file, but this forces all clients to declare and manipulate the binding handle rather than using automatic or implicit binding.</span></span> <span data-ttu-id="3844b-129">Para obter mais informações, consulte [os arquivos IDL e ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="3844b-129">For further information, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="3844b-130">Outro método é deixar os identificadores de associação fora do arquivo IDL e colocar o atributo **\_ identificador explícito** no ACF do servidor.</span><span class="sxs-lookup"><span data-stu-id="3844b-130">Another method is to leave the binding handles out of the IDL file and to place the **explicit\_handle** attribute into the server's ACF.</span></span> <span data-ttu-id="3844b-131">Dessa forma, o cliente pode usar o tipo de associação mais adequado para o aplicativo, enquanto o servidor usa o identificador de associação como se ele fosse declarado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="3844b-131">In this way, the client can use the type of binding best suited to the application, while the server uses the binding handle as though it were declared explicitly.</span></span>

<span data-ttu-id="3844b-132">O processo de extração das credenciais do cliente do identificador de associação ocorre da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3844b-132">The process of extracting the client credentials from the binding handle occurs as follows:</span></span>

-   <span data-ttu-id="3844b-133">Os clientes RPC chamam [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) e incluem suas informações de autenticação como parte das informações de associação passadas para o servidor.</span><span class="sxs-lookup"><span data-stu-id="3844b-133">RPC clients call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) and include their authentication information as part of the binding information passed to the server.</span></span>
-   <span data-ttu-id="3844b-134">Normalmente, o servidor chama [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) para se comportar como se fosse o cliente.</span><span class="sxs-lookup"><span data-stu-id="3844b-134">Usually, the server calls [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) in order to behave as though it were the client.</span></span> <span data-ttu-id="3844b-135">Se o identificador de associação não for autenticado, a chamada falhará com RPC \_ S \_ nenhum \_ contexto \_ disponível.</span><span class="sxs-lookup"><span data-stu-id="3844b-135">If the binding handle is not authenticated, the call fails with RPC\_S\_NO\_CONTEXT\_AVAILABLE.</span></span> <span data-ttu-id="3844b-136">Para obter o nome de usuário do cliente, chame [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) enquanto estiver representando ou no Windows XP ou em versões posteriores do Windows, chame [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) para obter o contexto de autorização e, em seguida, use as funções AuthZ para recuperar o nome.</span><span class="sxs-lookup"><span data-stu-id="3844b-136">To obtain the client's user name, call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) while impersonating, or on Windows XP or later versions of Windows, call [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) to get the authorization context, then use Authz functions to retrieve the name.</span></span>
-   <span data-ttu-id="3844b-137">Normalmente, o servidor chamará [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) para criar objetos com ACLs.</span><span class="sxs-lookup"><span data-stu-id="3844b-137">The server will normally call [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) to create objects with ACLs.</span></span> <span data-ttu-id="3844b-138">Depois que isso for feito, as verificações de segurança posteriores se tornarão automáticas.</span><span class="sxs-lookup"><span data-stu-id="3844b-138">After this is accomplished, later security checks become automatic.</span></span>

 

 