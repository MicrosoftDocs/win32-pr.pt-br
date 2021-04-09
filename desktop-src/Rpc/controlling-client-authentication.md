---
title: Controlando a autenticação do cliente
description: O melhor método para autenticar um cliente é instalar uma função de retorno de chamada de segurança usando a função RpcServerRegisterIf2 ou RpcServerRegisterIfEx; aceita uma função de retorno de chamada de segurança como um argumento.
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3508e99b351cd57fb67a3727710b60562ffe25dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822562"
---
# <a name="controlling-client-authentication"></a><span data-ttu-id="99b52-103">Controlando a autenticação do cliente</span><span class="sxs-lookup"><span data-stu-id="99b52-103">Controlling Client Authentication</span></span>

<span data-ttu-id="99b52-104">O melhor método para autenticar um cliente é instalar uma função de retorno de chamada de segurança usando a função [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) ou [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) ; aceita uma função de retorno de chamada de segurança como um argumento.</span><span class="sxs-lookup"><span data-stu-id="99b52-104">The best method for authenticating a client is installing a security callback function using the [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) or [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) function; either accepts a security callback function as an argument.</span></span> <span data-ttu-id="99b52-105">Quando a função de retorno de chamada de segurança for chamada, faça as verificações necessárias.</span><span class="sxs-lookup"><span data-stu-id="99b52-105">When the security callback function is called, make the necessary checks.</span></span> <span data-ttu-id="99b52-106">Os atributos na conexão, identidade do chamador ou ambos, podem ser verificados.</span><span class="sxs-lookup"><span data-stu-id="99b52-106">The attributes on the connection, identity of the caller, or both, can be checked.</span></span> <span data-ttu-id="99b52-107">Para verificar os atributos de uma conexão, chame a função [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) ou [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) .</span><span class="sxs-lookup"><span data-stu-id="99b52-107">To check the attributes of a connection, call the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) or [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) function.</span></span> <span data-ttu-id="99b52-108">Isso permite a filtragem de clientes que não são autenticados, clientes que usam um provedor de segurança específico ou clientes que não usam proteção suficientemente forte (como privacidade).</span><span class="sxs-lookup"><span data-stu-id="99b52-108">This enables the filtering of clients that are not authenticated, clients that use a specific security provider, or clients that do not use strong enough protection (like privacy).</span></span>

<span data-ttu-id="99b52-109">Para permitir o acesso a um subconjunto de usuários autenticados, use [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient).</span><span class="sxs-lookup"><span data-stu-id="99b52-109">To allow access to a subset of the authenticated users, use [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient).</span></span> <span data-ttu-id="99b52-110">Essa função retorna um contexto de cliente AuthZ que pode ser usado para fazer verificações de acesso muito sofisticadas.</span><span class="sxs-lookup"><span data-stu-id="99b52-110">This function returns an Authz client context that can be used to make very sophisticated access checks.</span></span> <span data-ttu-id="99b52-111">Por exemplo, esse método pode ser usado para permitir o acesso somente ao presidentes em uma organização durante o horário comercial normal e ao CEO durante qualquer hora usando os serviços Active Directory para mapear um nome de usuário para seu título.</span><span class="sxs-lookup"><span data-stu-id="99b52-111">For example, this method could be used to allow access only to the vice presidents in an organization during normal business hours, and to the CEO during any hour using Active Directory services to map a user name to their title.</span></span> <span data-ttu-id="99b52-112">O usuário pode ser representado e seu nome obtido.</span><span class="sxs-lookup"><span data-stu-id="99b52-112">The user can be impersonated, and their name obtained.</span></span> <span data-ttu-id="99b52-113">Depois que sua identidade for conhecida, quaisquer verificações desejadas poderão ser feitas.</span><span class="sxs-lookup"><span data-stu-id="99b52-113">Once their identity is known, any desired checks can be made.</span></span>

 

 




