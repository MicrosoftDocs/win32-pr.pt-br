---
description: A cláusula GROUP faz com que o WMI gere uma única notificação para representar um grupo de eventos.
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: Cláusula GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032a8e86c84c0b317b3739c0e203a249b432b0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765193"
---
# <a name="group-clause"></a><span data-ttu-id="9311f-103">Cláusula GROUP</span><span class="sxs-lookup"><span data-stu-id="9311f-103">GROUP Clause</span></span>

<span data-ttu-id="9311f-104">A cláusula GROUP faz com que o WMI gere uma única notificação para representar um grupo de eventos.</span><span class="sxs-lookup"><span data-stu-id="9311f-104">The GROUP clause causes WMI to generate a single notification to represent a group of events.</span></span> <span data-ttu-id="9311f-105">A notificação representativa é uma instância da classe de sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) .</span><span class="sxs-lookup"><span data-stu-id="9311f-105">The representative notification is an instance of the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span> <span data-ttu-id="9311f-106">A classe de sistema **\_ \_ AggregateEvent** contém duas propriedades: **Representation** e **NumberOfEvents**.</span><span class="sxs-lookup"><span data-stu-id="9311f-106">The **\_\_AggregateEvent** system class contains two properties: **Representative** and **NumberOfEvents**.</span></span> <span data-ttu-id="9311f-107">A propriedade **Representation** é um objeto inserido que contém uma das instâncias recebidas durante o intervalo de Agrupamento especificado na [cláusula Within](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="9311f-107">The **Representative** property is an embedded object that contains one of the instances received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="9311f-108">Por exemplo, se um evento de agregação for gerado para notificar sobre eventos de modificação de instância, **representará** uma instância da classe [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) .</span><span class="sxs-lookup"><span data-stu-id="9311f-108">For example, if an aggregate event is generated to notify of instance modification events, **Representative** contains one instance of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) class.</span></span> <span data-ttu-id="9311f-109">A propriedade **NumberOfEvents** contém o número de eventos recebidos durante o intervalo de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="9311f-109">The **NumberOfEvents** property contains the number of events received during the grouping interval.</span></span> <span data-ttu-id="9311f-110">O intervalo de agrupamento especifica o período de tempo, após o recebimento de um evento inicial, durante o qual o WMI deve coletar eventos semelhantes.</span><span class="sxs-lookup"><span data-stu-id="9311f-110">The grouping interval specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span>

<span data-ttu-id="9311f-111">A cláusula GROUP deve conter uma cláusula WITHIN para especificar o intervalo de agrupamento e pode conter a palavra-chave BY ou HAVING, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="9311f-111">The GROUP clause must contain a WITHIN clause to specify the grouping interval and can contain the BY or HAVING keyword, or both.</span></span> <span data-ttu-id="9311f-112">A cláusula GROUP é colocada após a cláusula WHERE, conforme mostrado a seguir:</span><span class="sxs-lookup"><span data-stu-id="9311f-112">The GROUP clause is placed after the WHERE clause, as shown following:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

<span data-ttu-id="9311f-113">O valor *EventClass* é a classe de evento da qual o evento é um membro e *Value* é o valor para a propriedade na qual a notificação é necessária.</span><span class="sxs-lookup"><span data-stu-id="9311f-113">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="9311f-114">O intervalo é um inteiro sem sinal que representa o intervalo de agrupamento após o recebimento do primeiro evento.</span><span class="sxs-lookup"><span data-stu-id="9311f-114">The interval is an unsigned integer that represents the grouping interval after receiving the first event.</span></span> <span data-ttu-id="9311f-115">O inteiro sem sinal é um número de segundos.</span><span class="sxs-lookup"><span data-stu-id="9311f-115">The unsigned integer is a number of seconds.</span></span> <span data-ttu-id="9311f-116">A lista de propriedades é uma lista delimitada por vírgula de uma ou mais propriedades que são incluídas na classe de evento; o *operador* é qualquer operador relacional; e *Integer* é um inteiro de 32 bits sem sinal indicando um número de eventos.</span><span class="sxs-lookup"><span data-stu-id="9311f-116">The property list is a comma-delimited list of one or more properties that are included in the event class; *operator* is any relational operator; and *integer* is an unsigned 32-bit integer indicating a number of events.</span></span>

<span data-ttu-id="9311f-117">Ao usar a cláusula GROUP, as cláusulas WHERE, BY e HAVING são opcionais.</span><span class="sxs-lookup"><span data-stu-id="9311f-117">When using the GROUP clause, the WHERE, BY, and HAVING clauses are optional.</span></span>

<span data-ttu-id="9311f-118">Um uso básico da cláusula GROUP pode solicitar um agrupamento de eventos dentro de um intervalo de tempo que é iniciado quando o primeiro evento é recebido.</span><span class="sxs-lookup"><span data-stu-id="9311f-118">A basic use of the GROUP clause might request a grouping of events within a time interval that starts when the first event is received.</span></span> <span data-ttu-id="9311f-119">Por exemplo, a consulta a seguir agrupa todos os eventos de email enviados em 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="9311f-119">For example, the following query groups all of the email events sent within 5 minutes.</span></span> <span data-ttu-id="9311f-120">Em vez de paginar um usuário sempre que um novo email for recebido, o consumidor permanente poderá usar essa consulta para informar o usuário somente se um novo email tiver sido recebido nos últimos 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="9311f-120">Instead of paging a user every time a piece of new email is received, the permanent consumer might use this query to inform the user only if new email has been received within the last 5 minutes.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



<span data-ttu-id="9311f-121">Se forem necessárias informações mais detalhadas, os eventos poderão ser agrupados por uma ou mais propriedades da classe de evento.</span><span class="sxs-lookup"><span data-stu-id="9311f-121">If more detailed information is required, events can be grouped by one or more properties of the event class.</span></span> <span data-ttu-id="9311f-122">A consulta a seguir solicita que os eventos de email sejam combinados com outros eventos que têm o mesmo valor na propriedade **Sender** :</span><span class="sxs-lookup"><span data-stu-id="9311f-122">The following query requests that email events be combined with other events that have the same value in the **Sender** property:</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



<span data-ttu-id="9311f-123">Um nível ainda maior de detalhes pode ser obtido com a adição de uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="9311f-123">A still greater level of detail can be achieved by adding a WHERE clause.</span></span> <span data-ttu-id="9311f-124">Por exemplo, a consulta a seguir notifica um usuário sobre o novo email de um remetente específico que chegou nos últimos 10 minutos, combinado com outros eventos que têm o mesmo valor na propriedade de **importância** :</span><span class="sxs-lookup"><span data-stu-id="9311f-124">For example, the following query notifies a user of new email from a particular sender that has arrived within the last 10 minutes, combined with other events that have the same value in the **Importance** property:</span></span>


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



