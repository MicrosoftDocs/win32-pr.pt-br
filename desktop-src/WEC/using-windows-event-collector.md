---
title: Usando o coletor de eventos do Windows
description: Esta seção lista os tópicos que explicam as tarefas que podem ser realizadas usando o SDK do coletor de eventos do Windows. Exemplos de código e explicações para todas as tarefas são incluídos em cada um dos tópicos a seguir.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc618ced4cefc7f17fb63b27bb1e097e65b3adac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788824"
---
# <a name="using-windows-event-collector"></a><span data-ttu-id="70a1f-104">Usando o coletor de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="70a1f-104">Using Windows Event Collector</span></span>

<span data-ttu-id="70a1f-105">Esta seção lista os tópicos que explicam as tarefas que podem ser realizadas usando o SDK do coletor de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="70a1f-105">This section lists the topics that explain the tasks that can be accomplished using the Windows Event Collector SDK.</span></span> <span data-ttu-id="70a1f-106">Exemplos de código e explicações para todas as tarefas são incluídos em cada um dos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="70a1f-106">Code examples and explanations for all the tasks are included in each of the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="70a1f-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="70a1f-107">In This Section</span></span>

-   [<span data-ttu-id="70a1f-108">Criando uma assinatura iniciada pelo coletor</span><span class="sxs-lookup"><span data-stu-id="70a1f-108">Creating a Collector Initiated Subscription</span></span>](creating-an-event-collector-subscription.md)

    <span data-ttu-id="70a1f-109">Fornece informações e um exemplo de código C++ para criar uma assinatura iniciada pelo coletor.</span><span class="sxs-lookup"><span data-stu-id="70a1f-109">Provides information and a C++ code example for creating a collector-initiated subscription.</span></span> <span data-ttu-id="70a1f-110">Uma assinatura iniciada pelo coletor permite que você receba eventos em um computador local (o coletor de eventos) que são encaminhados de um computador remoto (uma origem do evento).</span><span class="sxs-lookup"><span data-stu-id="70a1f-110">A collector-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source).</span></span>

-   [<span data-ttu-id="70a1f-111">Configurando uma assinatura iniciada pela origem</span><span class="sxs-lookup"><span data-stu-id="70a1f-111">Setting up a Source Initiated Subscription</span></span>](setting-up-a-source-initiated-subscription.md)

    <span data-ttu-id="70a1f-112">Fornece informações e um exemplo de código C++ para criar uma assinatura iniciada pela fonte.</span><span class="sxs-lookup"><span data-stu-id="70a1f-112">Provides information and a C++ code example for creating a source-initiated subscription.</span></span> <span data-ttu-id="70a1f-113">Uma assinatura iniciada pela origem permite que você receba eventos em um computador local (o coletor de eventos) que são encaminhados de um computador remoto (uma origem do evento) sem especificar as origens do evento na assinatura.</span><span class="sxs-lookup"><span data-stu-id="70a1f-113">A source-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source) without specifying the event sources in the subscription.</span></span>

-   [<span data-ttu-id="70a1f-114">Adicionando uma origem do evento a uma assinatura iniciada pelo coletor</span><span class="sxs-lookup"><span data-stu-id="70a1f-114">Adding an Event Source to a Collector Initiated Subscription</span></span>](adding-an-event-source-to-an-event-collector-subscription.md)

    <span data-ttu-id="70a1f-115">Fornece informações e um exemplo de código C++ para adicionar uma origem de evento (computador local ou computador remoto) a uma assinatura iniciada pelo coletor.</span><span class="sxs-lookup"><span data-stu-id="70a1f-115">Provides information and a C++ code example for adding an event source (local computer or remote computer) to a collector-initiated subscription.</span></span> <span data-ttu-id="70a1f-116">Uma assinatura iniciada pelo coletor não pode iniciar a coleta de eventos até que uma origem do evento seja adicionada à assinatura.</span><span class="sxs-lookup"><span data-stu-id="70a1f-116">A collector initiated subscription cannot start collecting events until an event source is added to the subscription.</span></span>

-   [<span data-ttu-id="70a1f-117">Criando assinaturas de evento de hardware</span><span class="sxs-lookup"><span data-stu-id="70a1f-117">Creating Hardware Event Subscriptions</span></span>](creating-hardware-event-subscriptions.md)

    <span data-ttu-id="70a1f-118">Fornece informações sobre como criar uma assinatura de evento para receber eventos de hardware de um computador que tenha um controlador BMC (Baseboard Management Controller) instalado.</span><span class="sxs-lookup"><span data-stu-id="70a1f-118">Provides information about how to create an event subscription in order to receive hardware events from a computer that has a Baseboard Management Controller (BMC) installed.</span></span>

-   [<span data-ttu-id="70a1f-119">Excluindo uma assinatura do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="70a1f-119">Deleting an Event Collector Subscription</span></span>](deleting-an-event-collector-subscription.md)

    <span data-ttu-id="70a1f-120">Fornece informações e um exemplo de código C++ para excluir uma assinatura do coletor de eventos de um computador local.</span><span class="sxs-lookup"><span data-stu-id="70a1f-120">Provides information and a C++ code example for deleting an Event Collector subscription from a local computer.</span></span>

-   [<span data-ttu-id="70a1f-121">Exibindo as propriedades de uma assinatura do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="70a1f-121">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)

    <span data-ttu-id="70a1f-122">Fornece informações e um exemplo de código C++ para exibir os valores de propriedade de uma assinatura do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="70a1f-122">Provides information and a C++ code example for displaying the property values of an Event Collector subscription.</span></span> <span data-ttu-id="70a1f-123">Os valores de propriedade podem fornecer informações úteis, como os endereços de origens do evento, o status da assinatura e as origens do evento e informações sobre como os eventos são entregues.</span><span class="sxs-lookup"><span data-stu-id="70a1f-123">Property values can provide useful information, such as the addresses of event sources, the status of the subscription and event sources, and information about how events are delivered.</span></span>

-   [<span data-ttu-id="70a1f-124">Exibindo o status de uma assinatura do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="70a1f-124">Displaying the Status of an Event Collector Subscription</span></span>](displaying-the-status-of-an-event-collector-subscription.md)

    <span data-ttu-id="70a1f-125">Fornece informações e um exemplo de código C++ para exibir o status de tempo de execução de fontes de eventos que estão associadas a uma assinatura do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="70a1f-125">Provides information and a C++ code example for displaying the run time status of events sources that are associated to an Event Collector subscription.</span></span> <span data-ttu-id="70a1f-126">Isso permite que você exiba mensagens de erro que podem ajudar a resolver problemas, o que impede que uma fonte de eventos encaminhe eventos.</span><span class="sxs-lookup"><span data-stu-id="70a1f-126">This enables you to view error messages that can help solve problems, which prevent an event source from forwarding events.</span></span>

-   [<span data-ttu-id="70a1f-127">Listando assinaturas do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="70a1f-127">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)

    <span data-ttu-id="70a1f-128">Fornece informações e um exemplo de código C++ para listar as assinaturas que existem em um computador local.</span><span class="sxs-lookup"><span data-stu-id="70a1f-128">Provides information and a C++ code example for listing the subscriptions that exist on a local computer.</span></span> <span data-ttu-id="70a1f-129">Você pode usar os nomes de assinatura que são obtidos com este exemplo para excluir uma assinatura, adicionar uma origem de evento a uma assinatura, recuperar as propriedades de uma assinatura ou exibir o status de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="70a1f-129">You can use the subscription names that are obtained with this example to delete a subscription, add an event source to a subscription, retrieve the properties of a subscription, or view the status of a subscription.</span></span>

-   [<span data-ttu-id="70a1f-130">Removendo uma origem do evento de uma assinatura iniciada pelo coletor</span><span class="sxs-lookup"><span data-stu-id="70a1f-130">Removing an Event Source from a Collector Initiated Subscription</span></span>](removing-an-event-source-from-an-event-collector-subscription.md)

    <span data-ttu-id="70a1f-131">Fornece informações e um exemplo de código C++ para remover uma origem de evento de uma assinatura iniciada pelo coletor.</span><span class="sxs-lookup"><span data-stu-id="70a1f-131">Provides information and a C++ code example for removing an event source from a collector-initiated subscription.</span></span> <span data-ttu-id="70a1f-132">Você pode remover uma fonte de eventos de uma assinatura iniciada pelo coletor sem desabilitar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="70a1f-132">You can remove an event source from a collector-initiated subscription without disabling the subscription.</span></span>

-   [<span data-ttu-id="70a1f-133">Repetindo uma assinatura do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="70a1f-133">Retrying an Event Collector Subscription</span></span>](retrying-an-event-collector-subscription.md)

    <span data-ttu-id="70a1f-134">Fornece informações e um exemplo de código C++ para repetir uma assinatura do coletor de eventos quando uma ou mais origens de evento falharam.</span><span class="sxs-lookup"><span data-stu-id="70a1f-134">Provides information and a C++ code example for retrying an Event Collector subscription when one or more event sources have failed.</span></span> <span data-ttu-id="70a1f-135">Você pode repetir uma única origem de evento ou pode repetir a assinatura inteira.</span><span class="sxs-lookup"><span data-stu-id="70a1f-135">You can retry a single event source or you can retry the entire subscription.</span></span>

 

 




