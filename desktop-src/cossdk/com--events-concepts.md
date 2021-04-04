---
description: Conceitos de eventos COM+
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Conceitos de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646546"
---
# <a name="com-events-concepts"></a><span data-ttu-id="adba0-103">Conceitos de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="adba0-103">COM+ Events Concepts</span></span>

<span data-ttu-id="adba0-104">O serviço de eventos COM+ é um sistema de eventos automatizado e *menos* rígido que armazena informações de eventos de editores diferentes no catálogo com+.</span><span class="sxs-lookup"><span data-stu-id="adba0-104">The COM+ events service is an automated, *loosely coupled event* system that stores event information from different publishers in the COM+ catalog.</span></span> <span data-ttu-id="adba0-105">Os assinantes podem consultar esse repositório de eventos e selecionar os eventos sobre os quais desejam saber.</span><span class="sxs-lookup"><span data-stu-id="adba0-105">Subscribers can query this event store and select the events that they want to hear about.</span></span>

> [!Note]  
> <span data-ttu-id="adba0-106">Um *evento* é identificado por um método em uma interface com+, conhecido como um *método de evento*, e é originado por um Publicador e despachado para o assinante ou assinantes corretos por meio do serviço de eventos com+.</span><span class="sxs-lookup"><span data-stu-id="adba0-106">An *event* is identified by a method in a COM+ interface, known as an *event method*, and is originated by a publisher and dispatched to the correct subscriber or subscribers through the COM+ events service.</span></span> <span data-ttu-id="adba0-107">Os métodos de evento devem ser nomeados exclusivamente e podem conter apenas parâmetros de entrada (sem parâmetros de saída ou de entrada/saída).</span><span class="sxs-lookup"><span data-stu-id="adba0-107">Event methods must be uniquely named and can contain only input parameters (no output or input/output parameters).</span></span> <span data-ttu-id="adba0-108">O valor de retorno deve ser um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="adba0-108">The return value must be an **HRESULT**.</span></span>

 

<span data-ttu-id="adba0-109">O serviço de eventos COM+ lida com a maioria das semânticas de evento para o Publicador e o Assinante.</span><span class="sxs-lookup"><span data-stu-id="adba0-109">The COM+ events service handles most of the event semantics for the publisher and subscriber.</span></span> <span data-ttu-id="adba0-110">Os editores oferecem para publicar tipos de evento e os assinantes solicitam tipos de evento de Publicadores.</span><span class="sxs-lookup"><span data-stu-id="adba0-110">Publishers offer to publish event types, and subscribers request event types from publishers.</span></span> <span data-ttu-id="adba0-111">Ao contrário de um sistema de *eventos rigidamente acoplado* , em que os editores devem lidar com a sobrecarga dos assinantes de chamada diretamente, o serviço de eventos com+ mantém os dados de assinatura no catálogo com+, independentemente do Publicador e do Assinante.</span><span class="sxs-lookup"><span data-stu-id="adba0-111">Unlike a *tightly coupled event* system, where publishers must handle the overhead of calling subscribers directly, the COM+ events service maintains subscription data in the COM+ catalog, independent of the publisher and subscriber.</span></span> <span data-ttu-id="adba0-112">Isso simplifica o modelo de programação para o Publicador e o assinante porque o componente de assinante do COM+ não precisa conter a lógica para a criação de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="adba0-112">This simplifies the programming model for the publisher and subscriber because the COM+ subscriber component does not need to contain the logic for building subscriptions.</span></span>

<span data-ttu-id="adba0-113">Como o ciclo de vida dos dados de assinatura de eventos COM+ é separado do Publicador ou do Assinante, as assinaturas podem ser criadas antes que o assinante ou os aplicativos do Publicador estejam ativos.</span><span class="sxs-lookup"><span data-stu-id="adba0-113">Because the life cycle of the COM+ events subscription data is separate from that of either the publisher or the subscriber, subscriptions can be built prior to either the subscriber or the publisher applications being active.</span></span> <span data-ttu-id="adba0-114">Isso também significa que os editores e assinantes podem ser desenvolvidos e implantados separadamente.</span><span class="sxs-lookup"><span data-stu-id="adba0-114">This also means that publishers and subscribers can be developed and deployed separately.</span></span> <span data-ttu-id="adba0-115">O Publicador pode ser escrito sem o conhecimento do número e do local dos assinantes.</span><span class="sxs-lookup"><span data-stu-id="adba0-115">The publisher can be written without knowledge of the number and location of the subscribers.</span></span> <span data-ttu-id="adba0-116">Os assinantes usam o serviço de eventos COM+ para localizar o Publicador e gerenciar suas assinaturas.</span><span class="sxs-lookup"><span data-stu-id="adba0-116">The subscribers use the COM+ Events service to find the publisher and manage their subscriptions.</span></span>

<span data-ttu-id="adba0-117">Os tópicos a seguir nesta seção fornecem informações detalhadas sobre os principais elementos do serviço de eventos COM+ e como usá-los.</span><span class="sxs-lookup"><span data-stu-id="adba0-117">The following topics in this section provide detailed information about the core elements of the COM+ events service and how to use them.</span></span>

-   [<span data-ttu-id="adba0-118">O objeto de classe de evento COM+</span><span class="sxs-lookup"><span data-stu-id="adba0-118">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
-   [<span data-ttu-id="adba0-119">Assinaturas</span><span class="sxs-lookup"><span data-stu-id="adba0-119">Subscriptions</span></span>](subscriptions.md)
-   [<span data-ttu-id="adba0-120">Publicando e fornecendo eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="adba0-120">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
-   [<span data-ttu-id="adba0-121">Filtrando eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="adba0-121">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
-   [<span data-ttu-id="adba0-122">Usando eventos COM+ com componentes em fila COM+</span><span class="sxs-lookup"><span data-stu-id="adba0-122">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a><span data-ttu-id="adba0-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="adba0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adba0-124">Considerações de segurança de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="adba0-124">COM+ Events Security Considerations</span></span>](com--events-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="adba0-125">Tarefas de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="adba0-125">COM+ Events Tasks</span></span>](com--events-tasks.md)
</dt> </dl>

 

 



