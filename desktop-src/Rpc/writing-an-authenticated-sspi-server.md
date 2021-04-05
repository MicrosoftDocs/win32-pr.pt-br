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
# <a name="writing-an-authenticated-sspi-server"></a><span data-ttu-id="0a6ff-104">Gravando um servidor SSPI autenticado</span><span class="sxs-lookup"><span data-stu-id="0a6ff-104">Writing an Authenticated SSPI Server</span></span>

<span data-ttu-id="0a6ff-105">Antes que a comunicação autenticada possa ocorrer entre os programas cliente e servidor, o servidor deve registrar suas informações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-105">Before authenticated communication can take place between the client and server programs, the server must register its authentication information.</span></span> <span data-ttu-id="0a6ff-106">Em particular, o servidor deve registrar seu nome principal e especificar o serviço de autenticação que ele usa.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-106">In particular, the server must register its principal name and specify the authentication service it uses.</span></span> <span data-ttu-id="0a6ff-107">Para obter mais informações sobre nomes de entidade de segurança, consulte [nomes de entidade de segurança](principal-names.md).</span><span class="sxs-lookup"><span data-stu-id="0a6ff-107">For more information on principal names, see [Principal Names](principal-names.md).</span></span> <span data-ttu-id="0a6ff-108">Para obter detalhes sobre os serviços de autenticação, consulte [serviços de autenticação](authentication-services.md).</span><span class="sxs-lookup"><span data-stu-id="0a6ff-108">For details about authentication services, see [Authentication Services](authentication-services.md).</span></span>

<span data-ttu-id="0a6ff-109">Para registrar suas informações de autenticação, os servidores chamam a função [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) .</span><span class="sxs-lookup"><span data-stu-id="0a6ff-109">To register its authentication information, servers call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function.</span></span> <span data-ttu-id="0a6ff-110">Passe um ponteiro para o nome da entidade de segurança como o valor do primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-110">Pass a pointer to the principal name as the value of the first parameter.</span></span> <span data-ttu-id="0a6ff-111">Defina o segundo parâmetro como uma constante que indica o serviço de autenticação que o aplicativo usará.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-111">Set the second parameter to a constant indicating the authentication service that the application will use.</span></span> <span data-ttu-id="0a6ff-112">Para obter uma descrição dos serviços de autenticação, consulte as [constantes de serviço de autenticação](authentication-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0a6ff-112">For a description of authentication services, see [Authentication-Service Constants](authentication-service-constants.md).</span></span>

<span data-ttu-id="0a6ff-113">O servidor também pode passar o endereço de uma função de aquisição de chave como o valor do terceiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-113">The server may also pass the address of a key acquisition function as the value of the third parameter.</span></span> <span data-ttu-id="0a6ff-114">Consulte [funções de aquisição de chave](key-acquisition-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0a6ff-114">See [Key Acquisition Functions](key-acquisition-functions.md).</span></span> <span data-ttu-id="0a6ff-115">Para usar a função de aquisição de chave padrão para o serviço de autenticação selecionado, defina o terceiro parâmetro como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-115">To use the default key acquisition function for the selected authentication service, set the third parameter to **NULL**.</span></span> <span data-ttu-id="0a6ff-116">O último parâmetro para a função [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) é um ponteiro de dados para passar para a função de aquisição de chave, se você fornecer uma função de aquisição de chave.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-116">The last parameter to the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function is a pointer data to pass to the key acquisition function, if you provide a key acquisition function.</span></span> <span data-ttu-id="0a6ff-117">Uma chamada para **RpcServerRegisterAuthInfo** é mostrada no fragmento de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-117">A call to **RpcServerRegisterAuthInfo** is shown in the following code fragment.</span></span>


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



<span data-ttu-id="0a6ff-118">Além disso, o servidor pode fornecer a biblioteca de tempo de execução RPC com uma função de autorização.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-118">In addition, the server may provide the RPC run-time library with an authorization function.</span></span> <span data-ttu-id="0a6ff-119">Para definir uma função de autorização, chame a função [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) .</span><span class="sxs-lookup"><span data-stu-id="0a6ff-119">To set an authorization function, call the [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) function.</span></span>

<span data-ttu-id="0a6ff-120">A parte do servidor de um aplicativo distribuído pode chamar a função [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) ou [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) para consultar um identificador de associação para obter informações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-120">The server portion of a distributed application can call the function [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to query a binding handle for authentication information.</span></span>

<span data-ttu-id="0a6ff-121">Se o seu servidor se registrar com um provedor de suporte de segurança, as chamadas de cliente com credenciais inválidas não serão expedidas.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-121">If your server registers with a security support provider, client calls with invalid credentials will not be dispatched.</span></span> <span data-ttu-id="0a6ff-122">No entanto, chamadas sem credenciais serão expedidas.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-122">However, calls with no credentials will be dispatched.</span></span> <span data-ttu-id="0a6ff-123">Há três maneiras de evitar que isso aconteça:</span><span class="sxs-lookup"><span data-stu-id="0a6ff-123">There are three ways to prevent this from happening:</span></span>

-   <span data-ttu-id="0a6ff-124">Registrar a interface usando [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), com uma função de retorno de chamada de segurança; Isso fará com que a biblioteca de tempo de execução RPC rejeite automaticamente as chamadas não autenticadas para essa interface.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-124">Register the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), with a security callback function; this will cause the RPC run-time library to automatically reject unauthenticated calls to that interface.</span></span> <span data-ttu-id="0a6ff-125">O registro de uma função de retorno de chamada é compatível com outros métodos de verificação de credenciais de acesso; a função de retorno de chamada pode chamar as funções [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)ou [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) , ou outras.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-125">Registering a callback function is compatible with other methods of checking access credentials; the callback function can itself call the [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient), or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) functions, or others.</span></span> <span data-ttu-id="0a6ff-126">No entanto, essas funções não podem usar os argumentos passados para a função, pois eles não são desempacotados nesse ponto.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-126">However, these functions cannot use the arguments passed to the function, as they are not unmarshalled at that point.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a6ff-127">Registrar a interface usando o [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) com uma função de retorno de chamada de segurança é o método mais intensamente recomendado para verificar as credenciais do cliente.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-127">Registering the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) with a security callback function is the most heavily recommended method of checking client credentials.</span></span>

 

-   <span data-ttu-id="0a6ff-128">Chame [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) para determinar o nível de segurança que o cliente está usando.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-128">Call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) to determine the security level that the client is using.</span></span> <span data-ttu-id="0a6ff-129">Seu stub poderá retornar um erro se o cliente não estiver autenticado.</span><span class="sxs-lookup"><span data-stu-id="0a6ff-129">Your stub can then return an error if the client is unauthenticated.</span></span>

 

 




