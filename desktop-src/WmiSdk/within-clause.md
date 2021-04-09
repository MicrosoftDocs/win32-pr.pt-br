---
description: Use a cláusula WITHIN em consultas de evento para especificar um intervalo de sondagem ou um intervalo de agrupamento.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: Cláusula WITHIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d863e2e71d52fe60aeed7697feeb1231164c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091372"
---
# <a name="within-clause"></a><span data-ttu-id="6ddc8-103">Cláusula WITHIN</span><span class="sxs-lookup"><span data-stu-id="6ddc8-103">WITHIN Clause</span></span>

<span data-ttu-id="6ddc8-104">Os consumidores de eventos usam a cláusula WITHIN em consultas de evento para especificar um *intervalo de sondagem* ou um *intervalo de agrupamento*.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-104">Event consumers use the WITHIN clause in event queries to specify a *polling interval* or a *grouping interval*.</span></span>

<span data-ttu-id="6ddc8-105">Um intervalo de sondagem é o intervalo que Instrumentação de Gerenciamento do Windows (WMI) usa para sondar o provedor de dados responsável pela classe para [eventos intrínsecos](determining-the-type-of-event-to-receive.md), dos quais o evento consultado é um membro.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-105">A polling interval is the interval that Windows Management Instrumentation (WMI) uses to poll the data provider responsible for the class for [intrinsic events](determining-the-type-of-event-to-receive.md), of which the event queried is a member.</span></span> <span data-ttu-id="6ddc8-106">Este intervalo é o período máximo de tempo que pode ser decorrido antes que um evento de notificação precise ser entregue.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-106">This interval is the maximum amount of time that can pass before notification of an event must be delivered.</span></span> <span data-ttu-id="6ddc8-107">Um consumidor usa um intervalo de sondagem em uma cláusula WITHIN quando o consumidor requer notificação de alterações em uma classe e um provedor de eventos não está disponível.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-107">A consumer uses a polling interval in a WITHIN clause when the consumer requires notification of changes to a class, and an event provider is unavailable.</span></span> <span data-ttu-id="6ddc8-108">O consumidor registra um evento intrínseco e inclui o intervalo de sondagem.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-108">The consumer registers for an intrinsic event and includes the polling interval.</span></span>

<span data-ttu-id="6ddc8-109">Para especificar um intervalo de sondagem, coloque a cláusula WITHIN imediatamente antes da cláusula WHERE, conforme mostrado a seguir:</span><span class="sxs-lookup"><span data-stu-id="6ddc8-109">To specify a polling interval, place the WITHIN clause immediately before the WHERE clause, as shown following:</span></span>


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



<span data-ttu-id="6ddc8-110">IntrinsicEventClass é a classe de evento intrínseca da qual o evento é um membro, Interval é o intervalo de sondagem e Value é o valor para a propriedade na qual o consumidor requer notificação.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-110">IntrinsicEventClass is the intrinsic event class of which the event is a member, interval is the polling interval, and value is the value for the property on which the consumer requires notification.</span></span>

<span data-ttu-id="6ddc8-111">O intervalo de sondagem é um número de ponto flutuante e pode ser fracionário para aceitar valores menores que 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-111">The polling interval is a floating-point number, and can be fractional to accept values smaller than 1 second.</span></span> <span data-ttu-id="6ddc8-112">No entanto, o intervalo deve representar um número de segundos em vez de um valor extremamente pequeno, como 0, 1, porque a especificação de um valor muito pequeno pode fazer com que o WMI rejeite a instrução como inválida — devido à natureza de sondagem intensiva de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-112">However, the interval should represent a number of seconds rather than an extremely small value such as 0.001, because specifying a value that is too small can cause WMI to reject the statement as not valid—due to the resource-intensive nature of polling.</span></span> <span data-ttu-id="6ddc8-113">Como a maioria dos consumidores de eventos não requer notificação imediata, é recomendável que eles usem um intervalo maior do que 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-113">Because most event consumers do not require immediate notification, it is recommended that they use an interval that is greater than 5 minutes.</span></span>

<span data-ttu-id="6ddc8-114">O exemplo de consulta a seguir solicita que o WMI Verifique a cada 10 segundos se há alterações que ocorrem em instâncias da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="6ddc8-114">The following query example requests that WMI check every 10 seconds for changes that occur to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="6ddc8-115">Se uma instância da classe for modificada dentro do intervalo de sondagem especificado, um evento de notificação será enviado para cada modificação.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-115">If an instance of the class is modified within the specified polling interval, a notification event is sent for each modification.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="6ddc8-116">Dependendo da consulta, um provedor de eventos e o WMI podem compartilhar a tarefa de fornecer eventos.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-116">Depending on the query, an event provider and WMI can share the task of providing events.</span></span> <span data-ttu-id="6ddc8-117">Por exemplo, um provedor de eventos que dá suporte a eventos das classes de sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) e [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) , e não a eventos da classe de sistema [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) .</span><span class="sxs-lookup"><span data-stu-id="6ddc8-117">For example, an event provider that supports events of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) and [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system classes, and not events of the [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) system class.</span></span> <span data-ttu-id="6ddc8-118">A consulta a seguir permite que o provedor de eventos gere os eventos de criação e modificação à medida que eles ocorrem e os tenha entregue quando forem criados.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-118">The following query enables the event provider to generate the creation and modification events as they occur and have them delivered when they are created.</span></span> <span data-ttu-id="6ddc8-119">A consulta também permite que o WMI gere eventos **\_ \_ InstanceDeletionEvent** a cada 10 (dez) segundos usando o mecanismo de sondagem.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-119">The query also allows WMI to generate **\_\_InstanceDeletionEvent** events every 10 (ten) seconds using the polling mechanism.</span></span>


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



<span data-ttu-id="6ddc8-120">Você também pode usar a cláusula WITHIN para especificar um intervalo de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-120">You can also use the WITHIN clause to specify a grouping interval.</span></span> <span data-ttu-id="6ddc8-121">Um intervalo de agrupamento é um inteiro de 32 bits sem sinal que especifica o período de tempo, após o recebimento de um evento inicial, durante o qual o WMI deve coletar eventos semelhantes.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-121">A grouping interval is an unsigned 32-bit integer that specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span> <span data-ttu-id="6ddc8-122">Quando esse período de tempo expira, o WMI entrega o evento de agregação, composto de todos os eventos semelhantes.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-122">When this time period expires, WMI delivers the aggregate event, made up of all the similar events.</span></span> <span data-ttu-id="6ddc8-123">Para obter mais informações, consulte [Group Clause](group-clause.md).</span><span class="sxs-lookup"><span data-stu-id="6ddc8-123">For more information, see [GROUP Clause](group-clause.md).</span></span>

<span data-ttu-id="6ddc8-124">Os consumidores de eventos que se registram para eventos que ocorrem com frequência usam um intervalo de agrupamento com a cláusula WITHIN.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-124">Event consumers that register for frequently occurring events use a grouping interval with the WITHIN clause.</span></span> <span data-ttu-id="6ddc8-125">Adicionar o grupo dentro da cláusula WHERE em uma consulta de evento faz com que o WMI envie um evento de agregação em vez de muitos eventos.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-125">Adding GROUP WITHIN to the WHERE clause in an event query results in WMI sending one aggregate event rather than many events.</span></span> <span data-ttu-id="6ddc8-126">O evento de agregação é representado pela classe de sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) .</span><span class="sxs-lookup"><span data-stu-id="6ddc8-126">The aggregate event is represented by the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span>

<span data-ttu-id="6ddc8-127">Para especificar um intervalo de agrupamento, coloque a cláusula WITHIN imediatamente após a cláusula GROUP.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-127">To specify a grouping interval, place the WITHIN clause immediately after the GROUP clause.</span></span>


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



<span data-ttu-id="6ddc8-128">EventClass é a classe de evento da qual o evento é um membro, value é o valor para a propriedade na qual o consumidor requer notificação e Interval é o intervalo de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-128">EventClass is the event class of which the event is a member, value is the value for the property on which the consumer requires notification, and Interval is the grouping interval.</span></span>

<span data-ttu-id="6ddc8-129">Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="6ddc8-129">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="6ddc8-130">Os consumidores de eventos permanentes podem ser criados com consultas de sondagem somente se você tiver privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="6ddc8-130">Permanent event consumers can be created with polling queries only if you have administrator privileges.</span></span>

 

 
