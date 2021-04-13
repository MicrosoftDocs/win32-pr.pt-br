---
description: O serviço de componentes em fila COM+ dá suporte total ao conceito de partições. Ou seja, quando um componente enfileirado dentro de uma partição é executado, a mensagem é enfileirada e o componente é eventualmente executado dentro da partição dos componentes.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Componentes e partições em fila COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589d7cb7c3e61be8ef53a248f990cde65447cf9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500858"
---
# <a name="com-queued-components-and-partitions"></a><span data-ttu-id="3cf31-104">Componentes e partições em fila COM+</span><span class="sxs-lookup"><span data-stu-id="3cf31-104">COM+ Queued Components and Partitions</span></span>

<span data-ttu-id="3cf31-105">O serviço de componentes em fila COM+ dá suporte total ao conceito de partições.</span><span class="sxs-lookup"><span data-stu-id="3cf31-105">The COM+ queued components service fully supports the concept of partitions.</span></span> <span data-ttu-id="3cf31-106">Ou seja, quando um componente enfileirado dentro de uma partição é executado, a mensagem é enfileirada e o componente é eventualmente executado dentro da partição do componente.</span><span class="sxs-lookup"><span data-stu-id="3cf31-106">That is, when a queued component within a partition is executed, the message is queued and the component is eventually executed within the component's partition.</span></span>

## <a name="queue-names-for-partitioned-components"></a><span data-ttu-id="3cf31-107">Nomes de fila para componentes particionados</span><span class="sxs-lookup"><span data-stu-id="3cf31-107">Queue Names for Partitioned Components</span></span>

<span data-ttu-id="3cf31-108">Tradicionalmente, o serviço de componentes em fila usa o nome do aplicativo como o nome da fila.</span><span class="sxs-lookup"><span data-stu-id="3cf31-108">Traditionally, the queued components service uses the application name as the queue name.</span></span> <span data-ttu-id="3cf31-109">Isso significa que em um cenário de não-partições, em que apenas uma instância de um nome de aplicativo existe em um computador, cada nome de aplicativo tem sua própria fila de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3cf31-109">This means that in a non-partitions scenario, where only one instance of an application name exists on a computer, each application name has its own message queue.</span></span>

<span data-ttu-id="3cf31-110">No entanto, no caso de partições, em que várias instâncias do mesmo nome de aplicativo podem existir em um computador, o serviço de componentes em fila usa a mesma fila para todos os componentes na fila que compartilham o mesmo nome de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3cf31-110">In the case of partitions, however, where multiple instances of the same application name can exist on a computer, the queued components service uses the same queue for any queued components that share the same application name.</span></span>

## <a name="activating-queued-components"></a><span data-ttu-id="3cf31-111">Ativando componentes na fila</span><span class="sxs-lookup"><span data-stu-id="3cf31-111">Activating Queued Components</span></span>

<span data-ttu-id="3cf31-112">As mesmas regras para como a ID da partição é usada para ativar um componente não enfileirado se aplicam a um componente enfileirado, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3cf31-112">The same rules for how the partition ID is used to activate a non-queued component applies to a queued component, as follows:</span></span>

-   <span data-ttu-id="3cf31-113">Se um moniker for usado para ativar o componente enfileirado e uma ID de partição estiver incluída, essa ID de partição será usada para localizar a partição.</span><span class="sxs-lookup"><span data-stu-id="3cf31-113">If a moniker is used to activate the queued component and a partition ID is included, this partition ID is used to locate the partition.</span></span> <span data-ttu-id="3cf31-114">Essa ID de partição tem precedência sobre qualquer ID de partição que possa existir no contexto do componente que está sendo ativado.</span><span class="sxs-lookup"><span data-stu-id="3cf31-114">This partition ID takes precedence over any partition ID that might exist in the context for the component being activated.</span></span>
-   <span data-ttu-id="3cf31-115">Se nenhum moniker estiver sendo usado para ativar o componente, a ID da partição que está no contexto do objeto será usada.</span><span class="sxs-lookup"><span data-stu-id="3cf31-115">If no moniker is being used to activate the component, the partition ID that is in the object's context is used.</span></span>
-   <span data-ttu-id="3cf31-116">Se não existir nenhuma ID de partição no contexto do objeto, o mapeamento padrão de usuário para partição dentro de Active Directory será usado.</span><span class="sxs-lookup"><span data-stu-id="3cf31-116">If no partition ID exists in the object's context, the default user-to-partition mapping within Active Directory is used.</span></span>

> [!Note]  
> <span data-ttu-id="3cf31-117">Se um computador servidor estiver desconectado da rede e se o mapeamento do conjunto de usuários para partições for alterado enquanto o servidor estiver desconectado, o cache de partição poderá conter mapeamento de conjunto de usuários para partições desatualizado.</span><span class="sxs-lookup"><span data-stu-id="3cf31-117">If a server computer is disconnected from the network and if the user-to-partition set mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition set mapping.</span></span> <span data-ttu-id="3cf31-118">Isso pode resultar em um erro de ativação se o mapeamento do conjunto de usuários para partições for o mecanismo usado para ativar um componente.</span><span class="sxs-lookup"><span data-stu-id="3cf31-118">This could result in an activation error if user-to-partition set mapping is the mechanism used to activate a component.</span></span>

 

<span data-ttu-id="3cf31-119">Os eventos COM+ são totalmente integrados às partições.</span><span class="sxs-lookup"><span data-stu-id="3cf31-119">COM+ events are fully integrated into partitions.</span></span> <span data-ttu-id="3cf31-120">Isso significa que um assinante pode assinar um Publicador cujo aplicativo reside em uma partição.</span><span class="sxs-lookup"><span data-stu-id="3cf31-120">This means that a subscriber can subscribe to a publisher whose application resides within a partition.</span></span> <span data-ttu-id="3cf31-121">Para permitir essa assinatura, a coleção de classes de assinante inclui duas propriedades relacionadas à partição — uma ID de partição de classe de evento e uma ID de aplicativo de classe de evento.</span><span class="sxs-lookup"><span data-stu-id="3cf31-121">To allow this subscription, the subscriber class collection includes two partition-related properties—an event class partition ID and an event class application ID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cf31-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3cf31-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cf31-123">Restrições de design de aplicativo</span><span class="sxs-lookup"><span data-stu-id="3cf31-123">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="3cf31-124">Implementação de partição</span><span class="sxs-lookup"><span data-stu-id="3cf31-124">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="3cf31-125">Registrando e ativando componentes em partições</span><span class="sxs-lookup"><span data-stu-id="3cf31-125">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="3cf31-126">O que são partições COM+?</span><span class="sxs-lookup"><span data-stu-id="3cf31-126">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



