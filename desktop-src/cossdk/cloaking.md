---
description: Há dois ingredientes para determinar o comportamento da representação da autoridade que o cliente concede explicitamente ao servidor por meio de um nível de representação e a capacidade dos servidores de mascarar sua própria identidade ao fazer chamadas nos clientes.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Encobrimento (serviços de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646295"
---
# <a name="cloaking-component-services"></a><span data-ttu-id="7927a-103">Encobrimento (serviços de componentes)</span><span class="sxs-lookup"><span data-stu-id="7927a-103">Cloaking (Component Services)</span></span>

<span data-ttu-id="7927a-104">Há dois ingredientes para determinar o comportamento da representação: a autoridade que o cliente concede explicitamente ao servidor por meio de um nível de representação e a capacidade do servidor de mascarar sua própria identidade ao fazer chamadas em nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="7927a-104">There are two ingredients in determining the behavior of impersonation: the authority the client explicitly grants the server through an impersonation level and the server's ability to mask its own identity when making calls on the client's behalf.</span></span> <span data-ttu-id="7927a-105">Essa última funcionalidade é conhecida como *encobrindo*.</span><span class="sxs-lookup"><span data-stu-id="7927a-105">This latter capability is known as *cloaking*.</span></span> <span data-ttu-id="7927a-106">O encobrimento tem a ver com a identidade de segurança sob a qual o servidor faz chamadas.</span><span class="sxs-lookup"><span data-stu-id="7927a-106">Cloaking has to do with the security identity under which the server makes calls.</span></span>

<span data-ttu-id="7927a-107">Quando o servidor representa o cliente, ele tem acesso direto às credenciais de segurança do cliente.</span><span class="sxs-lookup"><span data-stu-id="7927a-107">When the server impersonates the client, it has direct access to the client's security credentials.</span></span> <span data-ttu-id="7927a-108">Em um sentido muito local, o thread do servidor assume a identidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="7927a-108">In a very local sense, the server thread takes on the identity of the client.</span></span> <span data-ttu-id="7927a-109">Mas quando o servidor faz chamadas fora de seu processo, a identidade do cliente não será necessariamente projetada como a identidade sob a qual a chamada é feita.</span><span class="sxs-lookup"><span data-stu-id="7927a-109">But when the server makes calls outside of its process, the client identity will not necessarily be projected as the identity under which the call is made.</span></span>

<span data-ttu-id="7927a-110">Quando o encobrimento está habilitado, as chamadas feitas pelo servidor representando o cliente podem ser feitas sob a identidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="7927a-110">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="7927a-111">Quando o encobrimento estiver desabilitado, as chamadas pelo servidor serão feitas sob a identidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="7927a-111">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

<span data-ttu-id="7927a-112">Além disso, há duas formas de encobrimento, encobrimento *estático* e *encobrimento dinâmico*, que podem ser descritas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7927a-112">Moreover, there are two forms of cloaking, *static cloaking* and *dynamic cloaking*, which can be described as follows:</span></span>

-   <span data-ttu-id="7927a-113">Representação com encobrimento estático.</span><span class="sxs-lookup"><span data-stu-id="7927a-113">Impersonation with static cloaking.</span></span> <span data-ttu-id="7927a-114">A identidade do cliente original (realizada como o token de thread do servidor) pode ser apresentada uma vez a um servidor downstream em uma chamada usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), definindo a identidade do cliente original uma vez no proxy e esse token de thread será usado em chamadas de método subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7927a-114">The original client identity (realized as the server thread token) can be presented once to a downstream server on a call using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), setting the original client identity once on the proxy, and that thread token will be used on subsequent method calls.</span></span>
-   <span data-ttu-id="7927a-115">Representação com o encobrimento dinâmico.</span><span class="sxs-lookup"><span data-stu-id="7927a-115">Impersonation with dynamic cloaking.</span></span> <span data-ttu-id="7927a-116">A identidade original do cliente é descoberta como o token de thread do servidor em cada chamada de método para o servidor downstream.</span><span class="sxs-lookup"><span data-stu-id="7927a-116">The original client identity is discovered as the server thread token on each method call to the downstream server.</span></span> <span data-ttu-id="7927a-117">Na verdade, a identidade apresentada pode ser determinada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="7927a-117">In effect, the identity that is presented can be determined dynamically.</span></span> <span data-ttu-id="7927a-118">A sobrecarga necessária para fazer isso pode ser consideravelmente mais cara.</span><span class="sxs-lookup"><span data-stu-id="7927a-118">The overhead required to do this can be considerably more expensive.</span></span>

<span data-ttu-id="7927a-119">Para aplicativos COM+, a configuração padrão é para o recurso de encobrimento dinâmico.</span><span class="sxs-lookup"><span data-stu-id="7927a-119">For COM+ applications, the default configuration is for dynamic cloaking capability.</span></span> <span data-ttu-id="7927a-120">Isso pode ser alterado programaticamente e administrativamente.</span><span class="sxs-lookup"><span data-stu-id="7927a-120">This can be changed programmatically and administratively.</span></span> <span data-ttu-id="7927a-121">Embora o encobrimento dinâmico possa ter sobrecarga de desempenho, ele fornece a flexibilidade que geralmente é exigida pelas circunstâncias que exigem o uso da representação em primeiro lugar.</span><span class="sxs-lookup"><span data-stu-id="7927a-121">While dynamic cloaking can have performance overhead, it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

<span data-ttu-id="7927a-122">Para obter mais detalhes sobre o encobrimento e descrições precisas de possíveis comportamentos, consulte [encobrindo](/windows/desktop/com/cloaking) na documentação com.</span><span class="sxs-lookup"><span data-stu-id="7927a-122">For more detail regarding cloaking and precise descriptions of possible behaviors, see [Cloaking](/windows/desktop/com/cloaking) in the COM documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7927a-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7927a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7927a-124">Representação e delegação de cliente</span><span class="sxs-lookup"><span data-stu-id="7927a-124">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="7927a-125">Requisitos do lado do cliente para representação</span><span class="sxs-lookup"><span data-stu-id="7927a-125">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="7927a-126">Requisitos do lado do servidor para representação</span><span class="sxs-lookup"><span data-stu-id="7927a-126">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
