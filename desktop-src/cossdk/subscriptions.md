---
description: 'Os dados de assinatura residem no catálogo COM+ da assinatura. Uma assinatura pode ser criada usando a ferramenta administrativa serviços de componentes ou programaticamente usando a interface ICOMAdminCatalog:: InstallComponent.'
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: Assinaturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9973eb76fc22354f1a2fc8e381c90cf5be1efee3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164015"
---
# <a name="subscriptions"></a><span data-ttu-id="7f37d-104">Assinaturas</span><span class="sxs-lookup"><span data-stu-id="7f37d-104">Subscriptions</span></span>

<span data-ttu-id="7f37d-105">Os dados de assinatura residem no catálogo COM+ da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7f37d-105">Subscription data resides in the subscription COM+ catalog.</span></span> <span data-ttu-id="7f37d-106">Uma assinatura pode ser criada usando a ferramenta administrativa serviços de componentes ou programaticamente usando a interface [**ICOMAdminCatalog:: InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) .</span><span class="sxs-lookup"><span data-stu-id="7f37d-106">A subscription can be created either by using the Component Services administrative tool or programmatically by using the [**ICOMAdminCatalog::InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) interface.</span></span>

<span data-ttu-id="7f37d-107">A coleção [**SubscriptionsForComponent**](subscriptionsforcomponent.md) é usada para adicionar, excluir ou alterar informações pertencentes a assinaturas.</span><span class="sxs-lookup"><span data-stu-id="7f37d-107">The [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection is used to add, delete, or change information pertaining to subscriptions.</span></span> <span data-ttu-id="7f37d-108">A coleção **SubscriptionsForComponent** é uma coleção filho de um componente.</span><span class="sxs-lookup"><span data-stu-id="7f37d-108">The **SubscriptionsForComponent** collection is a child collection to a component.</span></span> <span data-ttu-id="7f37d-109">Para adicionar uma assinatura, obtenha a coleção **SubscriptionsForComponent** do componente e use o método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) para adicionar uma entrada à coleção.</span><span class="sxs-lookup"><span data-stu-id="7f37d-109">To add a subscription, get the component's **SubscriptionsForComponent** collection and use the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method to add an entry to the collection.</span></span> <span data-ttu-id="7f37d-110">Para configurar as várias propriedades do objeto de assinatura, use a propriedade [**Value**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) .</span><span class="sxs-lookup"><span data-stu-id="7f37d-110">To set up the various properties of the subscription object, use the [**Value**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) property.</span></span> <span data-ttu-id="7f37d-111">Para salvar as alterações, use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) no objeto da coleção **SubscriptionsForComponent** .</span><span class="sxs-lookup"><span data-stu-id="7f37d-111">To save the changes, use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the **SubscriptionsForComponent** collection object.</span></span>

<span data-ttu-id="7f37d-112">Você também pode usar a ferramenta de administração de serviços de componentes para modificar algumas, mas não todas, as propriedades da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7f37d-112">You can also use the Component Services administration tool to modify some, but not all, of the subscription properties.</span></span> <span data-ttu-id="7f37d-113">As assinaturas especificam as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="7f37d-113">Subscriptions specify the following information:</span></span>

-   <span data-ttu-id="7f37d-114">Identidade e local do assinante</span><span class="sxs-lookup"><span data-stu-id="7f37d-114">Identity and location of the subscriber</span></span>
-   <span data-ttu-id="7f37d-115">Método de entrega</span><span class="sxs-lookup"><span data-stu-id="7f37d-115">Delivery method</span></span>
-   <span data-ttu-id="7f37d-116">Métodos de evento a serem entregues</span><span class="sxs-lookup"><span data-stu-id="7f37d-116">Event methods to deliver</span></span>
-   <span data-ttu-id="7f37d-117">Objeto de classe de evento e a propriedade PublisherID de um componente de classe de evento do qual o assinante deseja receber eventos</span><span class="sxs-lookup"><span data-stu-id="7f37d-117">Event class object and PublisherID property of an event class component from which the subscriber wants to receive events</span></span>

<span data-ttu-id="7f37d-118">As assinaturas existem independentemente dos objetos da classe de evento.</span><span class="sxs-lookup"><span data-stu-id="7f37d-118">Subscriptions exist independently from event class objects.</span></span> <span data-ttu-id="7f37d-119">Você pode desabilitar uma assinatura definindo a propriedade Enabled como false.</span><span class="sxs-lookup"><span data-stu-id="7f37d-119">You can disable a subscription by setting the Enabled property to False.</span></span> <span data-ttu-id="7f37d-120">Uma assinatura desabilitada não é chamada por eventos COM+.</span><span class="sxs-lookup"><span data-stu-id="7f37d-120">A disabled subscription is not called by COM+ Events.</span></span>

<span data-ttu-id="7f37d-121">Os três tipos de assinaturas são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7f37d-121">The three types of subscriptions are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="7f37d-122"><span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Persistente</span><span class="sxs-lookup"><span data-stu-id="7f37d-122"><span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Persistent</span></span>
</dt> <dd>

<span data-ttu-id="7f37d-123">As assinaturas persistentes residem no catálogo COM+ e são independentes do tempo de vida do Assinante.</span><span class="sxs-lookup"><span data-stu-id="7f37d-123">Persistent subscriptions reside in the COM+ catalog and are independent from the subscriber's lifetime.</span></span> <span data-ttu-id="7f37d-124">As assinaturas persistentes sobrevivem a uma reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="7f37d-124">Persistent subscriptions survive a system restart.</span></span> <span data-ttu-id="7f37d-125">Geralmente, uma assinatura persistente é criada quando um aplicativo é instalado no computador de um assinante e removido quando o aplicativo é removido.</span><span class="sxs-lookup"><span data-stu-id="7f37d-125">Generally, a persistent subscription is created when an application is installed on a subscriber's computer and removed when the application is removed.</span></span> <span data-ttu-id="7f37d-126">Depois que uma assinatura persistente é criada, os eventos COM+ ativam o assinante sempre que um evento deve ser entregue a ele.</span><span class="sxs-lookup"><span data-stu-id="7f37d-126">After a persistent subscription is created, COM+ Events activates the subscriber each time an event should be delivered to it.</span></span>

<span data-ttu-id="7f37d-127">Quando um Publicador instancia e faz uma chamada em um objeto de [classe de evento](the-com--event-class-object.md) , o objeto procura todas as assinaturas persistentes no catálogo com+ e cria uma nova instância de cada objeto.</span><span class="sxs-lookup"><span data-stu-id="7f37d-127">When a publisher instantiates and makes a call on an [event class](the-com--event-class-object.md) object, the object looks for all the persistent subscriptions in the COM+ catalog and creates a new instance of each object.</span></span> <span data-ttu-id="7f37d-128">O processo de criação pode ser direto ou por meio de um moniker para componentes em fila.</span><span class="sxs-lookup"><span data-stu-id="7f37d-128">The creation process can be either direct or through a moniker for queued components.</span></span> <span data-ttu-id="7f37d-129">Especifique o objeto de assinante pela propriedade [**SubscriberMoniker**](subscriptionsforcomponent.md) da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7f37d-129">Specify the subscriber object by the [**SubscriberMoniker**](subscriptionsforcomponent.md) property of the subscription.</span></span> <span data-ttu-id="7f37d-130">Os objetos de assinante criados por uma assinatura persistente são sempre liberados após cada chamada de evento.</span><span class="sxs-lookup"><span data-stu-id="7f37d-130">Subscriber objects created by a persistent subscription are always released after each event call.</span></span>

</dd> <dt>

<span data-ttu-id="7f37d-131"><span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Transitório</span><span class="sxs-lookup"><span data-stu-id="7f37d-131"><span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Transient</span></span>
</dt> <dd>

<span data-ttu-id="7f37d-132">Para assinaturas transitórias, você pode usar a coleção [**TransientSubscriptions**](transientsubscriptions.md) , cujo objeto pai é o objeto de catálogo raiz.</span><span class="sxs-lookup"><span data-stu-id="7f37d-132">For transient subscriptions, you can use the [**TransientSubscriptions**](transientsubscriptions.md) collection, whose parent object is the root catalog object.</span></span> <span data-ttu-id="7f37d-133">Assinaturas transitórias solicitam um evento para um objeto de Assinante específico que já existe.</span><span class="sxs-lookup"><span data-stu-id="7f37d-133">Transient subscriptions request an event for a specific subscriber object that already exists.</span></span> <span data-ttu-id="7f37d-134">As assinaturas transitórias são armazenadas no catálogo COM+, mas a assinatura é excluída se o sistema de eventos ou o sistema operacional for interrompido.</span><span class="sxs-lookup"><span data-stu-id="7f37d-134">Transient subscriptions are stored in the COM+ catalog, but the subscription is deleted if the event system or operating system is stopped.</span></span> <span data-ttu-id="7f37d-135">Ao contrário das assinaturas persistentes, as assinaturas transitórias são vinculadas a um objeto específico e são armazenadas apenas no sistema de eventos.</span><span class="sxs-lookup"><span data-stu-id="7f37d-135">Unlike persistent subscriptions, transient subscriptions are tied to a particular object and are stored only in the event system.</span></span> <span data-ttu-id="7f37d-136">Assinaturas transitórias podem ser mais eficientes do que assinaturas persistentes, mas você deve gerenciar seus ciclos de vida do objeto.</span><span class="sxs-lookup"><span data-stu-id="7f37d-136">Transient subscriptions can be more efficient than persistent subscriptions, but you must manage their object life cycles.</span></span> <span data-ttu-id="7f37d-137">Para obter informações sobre como registrar uma assinatura transitória, consulte [registrando uma assinatura transitória](registering-a-transient-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="7f37d-137">For information about registering a transient subscription, see [Registering a Transient Subscription](registering-a-transient-subscription.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f37d-138"><span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Por usuário</span><span class="sxs-lookup"><span data-stu-id="7f37d-138"><span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Per user</span></span>
</dt> <dd>

<span data-ttu-id="7f37d-139">As assinaturas por usuário podem entregar eventos somente quando o assinante está conectado ao computador do sistema de eventos.</span><span class="sxs-lookup"><span data-stu-id="7f37d-139">Per User subscriptions can deliver events only when the subscriber is logged on to the event system's computer.</span></span> <span data-ttu-id="7f37d-140">Quando o assinante faz logon, o sistema de eventos habilita todas as assinaturas nas quais o sinalizador de *Peruser* está definido como **true** e *username* é definido como o nome do usuário que está conectado.</span><span class="sxs-lookup"><span data-stu-id="7f37d-140">When the subscriber logs on, the event system enables all subscriptions on which the *PerUser* flag is set to **TRUE** and *UserName* is set to the name of the user who is logged on.</span></span> <span data-ttu-id="7f37d-141">Quando o assinante faz logoff, as assinaturas são desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="7f37d-141">When the subscriber logs off, the subscriptions are disabled.</span></span>

<span data-ttu-id="7f37d-142">As assinaturas por usuário entram em vigor somente quando o Publicador e o assinante estão no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="7f37d-142">Per User subscriptions are effective only when the publisher and subscriber are on the same computer.</span></span> <span data-ttu-id="7f37d-143">O logon e o logoff são detectados somente no computador do Publicador — e não no computador no qual o objeto do assinante reside.</span><span class="sxs-lookup"><span data-stu-id="7f37d-143">Logon and logoff are detected only at the publisher's computer—not the computer on which the subscriber object resides.</span></span>

</dd> </dl>

<span data-ttu-id="7f37d-144">O sistema de eventos usa meta-Events para notificar os assinantes interessados sempre que os objetos ou assinaturas da classe de evento forem criados, modificados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="7f37d-144">The event system uses meta-events to notify interested subscribers whenever event class objects or subscriptions are created, modified, or removed.</span></span> <span data-ttu-id="7f37d-145">Para receber meta-eventos do sistema de eventos, os aplicativos devem criar uma assinatura que resida no computador do sistema de eventos e que especifique a ID da interface de acionamento (IID \_ IEventObjectChange).</span><span class="sxs-lookup"><span data-stu-id="7f37d-145">To receive meta-events from the event system, applications must create a subscription that resides on the event system's computer and that specifies the firing interface ID (IID\_IEventObjectChange).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f37d-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f37d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f37d-147">Filtrando eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="7f37d-147">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="7f37d-148">Publicando e fornecendo eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="7f37d-148">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="7f37d-149">O objeto de classe de evento COM+</span><span class="sxs-lookup"><span data-stu-id="7f37d-149">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="7f37d-150">Usando eventos COM+ com componentes em fila COM+</span><span class="sxs-lookup"><span data-stu-id="7f37d-150">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



