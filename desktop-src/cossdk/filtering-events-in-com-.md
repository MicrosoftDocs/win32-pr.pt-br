---
description: 'Os eventos COM+ fornecem duas maneiras de controlar quais eventos atingem quais assinantes: filtragem de Publicador e filtragem de parâmetros.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Filtrando eventos no COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646490"
---
# <a name="filtering-events-in-com"></a><span data-ttu-id="000bd-103">Filtrando eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="000bd-103">Filtering Events in COM+</span></span>

<span data-ttu-id="000bd-104">Os eventos COM+ fornecem duas maneiras de controlar quais eventos atingem quais assinantes: *filtragem de Publicador* e *filtragem de parâmetros*.</span><span class="sxs-lookup"><span data-stu-id="000bd-104">COM+ Events provides two ways to control which events reach which subscribers: *publisher filtering* and *parameter filtering*.</span></span>

## <a name="publisher-filtering"></a><span data-ttu-id="000bd-105">Filtragem de Publicador</span><span class="sxs-lookup"><span data-stu-id="000bd-105">Publisher Filtering</span></span>

<span data-ttu-id="000bd-106">A filtragem de Publicador controla a ordem e o acionamento de um método de evento por um objeto de [classe de evento](the-com--event-class-object.md) .</span><span class="sxs-lookup"><span data-stu-id="000bd-106">Publisher filtering controls the order and firing of an event method by an [event class](the-com--event-class-object.md) object.</span></span> <span data-ttu-id="000bd-107">A filtragem de Publicador permite que o Publicador determine quais assinantes recebem um evento específico.</span><span class="sxs-lookup"><span data-stu-id="000bd-107">Publisher filtering allows the publisher to determine which subscribers receive a particular event.</span></span>

<span data-ttu-id="000bd-108">Um exemplo de uso efetivo da filtragem de Publicador é o de uma troca de estoque.</span><span class="sxs-lookup"><span data-stu-id="000bd-108">An example of effective use of publisher filtering is that of a stock exchange.</span></span> <span data-ttu-id="000bd-109">A maioria dos assinantes deseja saber quando uma nova ação é adicionada.</span><span class="sxs-lookup"><span data-stu-id="000bd-109">Most subscribers want to know when a new stock is added.</span></span> <span data-ttu-id="000bd-110">No entanto, muitos desses mesmos assinantes talvez não queiram saber sempre que cada preço de estoque é alterado.</span><span class="sxs-lookup"><span data-stu-id="000bd-110">However, many of these same subscribers may not want to know whenever each stock price changes.</span></span> <span data-ttu-id="000bd-111">A filtragem de Publicador fornece a granularidade necessária para entregar com eficiência os eventos apenas aos assinantes que desejam essas informações.</span><span class="sxs-lookup"><span data-stu-id="000bd-111">Publisher filtering provides the granularity required to effectively deliver events to only the subscribers who want this information.</span></span>

<span data-ttu-id="000bd-112">Quando um método é invocado no objeto da classe de evento instanciado, ele coleta todos os filtros do editor nesse método.</span><span class="sxs-lookup"><span data-stu-id="000bd-112">When a method is invoked on the instantiated event class object, it collects any publisher filters on that method.</span></span> <span data-ttu-id="000bd-113">O filtro força o objeto de evento a acionar o método de evento para um Assinante específico.</span><span class="sxs-lookup"><span data-stu-id="000bd-113">The filter forces the event object to fire the event method to a specific subscriber.</span></span> <span data-ttu-id="000bd-114">O filtro determina quais assinaturas são acionadas e em qual ordem para disfire-las.</span><span class="sxs-lookup"><span data-stu-id="000bd-114">The filter determines which subscriptions to fire and in which order to fire them.</span></span> <span data-ttu-id="000bd-115">Por exemplo, o filtro pode ler a lista de assinaturas e criar a ordem com base em alguns critérios de aplicativo e, em seguida, chamar os assinantes nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="000bd-115">For example, the filter could read the subscription list and create the order based on some application criteria and then call the subscribers in that order.</span></span>

<span data-ttu-id="000bd-116">Para obter instruções detalhadas sobre como criar um filtro de Publicador, consulte [criando um filtro de Publicador](creating-a-publisher-filter.md).</span><span class="sxs-lookup"><span data-stu-id="000bd-116">For detailed instructions on creating a publisher filter, see [Creating a Publisher Filter](creating-a-publisher-filter.md).</span></span>

## <a name="parameter-filtering"></a><span data-ttu-id="000bd-117">Filtragem de parâmetro</span><span class="sxs-lookup"><span data-stu-id="000bd-117">Parameter Filtering</span></span>

<span data-ttu-id="000bd-118">Ao contrário da filtragem de Publicador, o serviço de eventos COM+ fornece uma filtragem de parâmetro de assinante opcional para cada assinatura e cada invocação de método de evento.</span><span class="sxs-lookup"><span data-stu-id="000bd-118">In contrast to publisher filtering, the COM+ Events service provides an optional subscriber parameter filtering for each subscription and each event method invocation.</span></span> <span data-ttu-id="000bd-119">A filtragem de parâmetro avalia a propriedade FilterCriteria da assinatura em relação aos parâmetros do método de evento.</span><span class="sxs-lookup"><span data-stu-id="000bd-119">Parameter filtering evaluates the subscription FilterCriteria property against the parameters of the event method.</span></span> <span data-ttu-id="000bd-120">Esse tipo de filtragem é usado em uma base por cada assinatura e fornece um nível de filtragem de Assinante na origem do evento.</span><span class="sxs-lookup"><span data-stu-id="000bd-120">This type of filtering is used on a per-method, per-subscription basis and provides a level of subscriber filtering at the event source.</span></span> <span data-ttu-id="000bd-121">A cadeia de caracteres de critérios de filtro reconhece os operadores relacionais para verificar a igualdade (=, = =,!,! =, ~, ~ =,  <>), parênteses aninhados e palavras-chave lógicas **e**, **ou**, ou **não**.</span><span class="sxs-lookup"><span data-stu-id="000bd-121">The filter criteria string recognizes relational operators for checking equality (=, ==, !, !=, ~, ~=, <>), nested parentheses, and logical keywords **AND**, **OR**, or **NOT**.</span></span>

<span data-ttu-id="000bd-122">A filtragem de parâmetro ocorre depois de qualquer filtragem de Publicador e quando o objeto de evento padrão é acionado para uma determinada assinatura.</span><span class="sxs-lookup"><span data-stu-id="000bd-122">Parameter filtering occurs after any publisher filtering and when the standard event object is fired for a given subscription.</span></span> <span data-ttu-id="000bd-123">Se a filtragem de Publicador for usada, a filtragem de parâmetros ocorrerá somente quando o filtro de editor invocar [**IFiringControl:: FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span><span class="sxs-lookup"><span data-stu-id="000bd-123">If publisher filtering is used, parameter filtering occurs only when the publisher filter invokes [**IFiringControl::FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span></span> <span data-ttu-id="000bd-124">Por isso, a filtragem de editores e a filtragem de parâmetros podem compor juntas, mas a filtragem de Publicador tem precedência.</span><span class="sxs-lookup"><span data-stu-id="000bd-124">Because of this, publisher filtering and parameter filtering can compose together but publisher filtering takes precedence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="000bd-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="000bd-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="000bd-126">Publicando e fornecendo eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="000bd-126">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="000bd-127">Assinaturas</span><span class="sxs-lookup"><span data-stu-id="000bd-127">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="000bd-128">O objeto de classe de evento COM+</span><span class="sxs-lookup"><span data-stu-id="000bd-128">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="000bd-129">Usando eventos COM+ com componentes em fila COM+</span><span class="sxs-lookup"><span data-stu-id="000bd-129">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



