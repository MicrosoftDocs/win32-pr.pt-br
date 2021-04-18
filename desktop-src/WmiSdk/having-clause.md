---
description: A cláusula HAVING é usada para filtrar os eventos que são recebidos durante o intervalo de Agrupamento especificado na cláusula WITHIN.
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: Cláusula HAVING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f93fbe082fb2f655dfad59d7642e1d0ff9a33e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807786"
---
# <a name="having-clause"></a><span data-ttu-id="aa31a-103">Cláusula HAVING</span><span class="sxs-lookup"><span data-stu-id="aa31a-103">HAVING Clause</span></span>

<span data-ttu-id="aa31a-104">A cláusula HAVING é usada para filtrar os eventos que são recebidos durante o intervalo de Agrupamento especificado na [cláusula Within](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="aa31a-104">The HAVING clause is used to filter the events that are received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="aa31a-105">Por exemplo, uma instrução SELECT poderia ser construída para que não retorne nada, a menos que haja pelo menos 5 eventos dentro do intervalo de 30 segundos anteriores.</span><span class="sxs-lookup"><span data-stu-id="aa31a-105">For example, a SELECT statement could be constructed so that it returns nothing unless there HAVE been at least 5 events within the past 30 second INTERVAL.</span></span>

<span data-ttu-id="aa31a-106">A cláusula WITHIN segue imediatamente na [instrução SELECT](select-statement-for-event-queries.md) após a cláusula [Group](group-clause.md) .</span><span class="sxs-lookup"><span data-stu-id="aa31a-106">The WITHIN clause follows immediately in the [SELECT statement](select-statement-for-event-queries.md) after the [GROUP](group-clause.md) clause.</span></span> <span data-ttu-id="aa31a-107">A cláusula HAVING opera na propriedade **NumberOfEvents** da classe de sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) , da qual o grupo criado pela cláusula Group é um membro.</span><span class="sxs-lookup"><span data-stu-id="aa31a-107">The HAVING clause operates on the **NumberOfEvents** property of the [**\_\_AggregateEvent**](--aggregateevent.md) system class, of which the group created by the GROUP clause is a member.</span></span> <span data-ttu-id="aa31a-108">A cláusula HAVING pode usar todos os operadores relacionais padrão.</span><span class="sxs-lookup"><span data-stu-id="aa31a-108">The HAVING clause can use all of the standard relational operators.</span></span>

<span data-ttu-id="aa31a-109">A sintaxe dela é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="aa31a-109">The syntax is as follows:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

<span data-ttu-id="aa31a-110">O valor *EventClass* é a classe de evento da qual o evento é um membro e *Value* é o valor para a propriedade na qual a notificação é necessária.</span><span class="sxs-lookup"><span data-stu-id="aa31a-110">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="aa31a-111">O intervalo é um inteiro sem sinal que representa o intervalo de agrupamento (em segundos) após o recebimento do primeiro evento.</span><span class="sxs-lookup"><span data-stu-id="aa31a-111">The interval is an unsigned integer that represents the grouping interval (in seconds) after receiving the first event.</span></span> <span data-ttu-id="aa31a-112">A lista de propriedades é uma lista delimitada por vírgula de uma ou mais propriedades que são incluídas na classe de evento.</span><span class="sxs-lookup"><span data-stu-id="aa31a-112">The property list is a comma-delimited list of one or more properties that are included in the event class.</span></span> <span data-ttu-id="aa31a-113">O operador é qualquer operador relacional.</span><span class="sxs-lookup"><span data-stu-id="aa31a-113">The operator is any relational operator.</span></span> <span data-ttu-id="aa31a-114">O valor constante é qualquer inteiro de 32 bits sem sinal que indique o número de eventos usados para filtragem.</span><span class="sxs-lookup"><span data-stu-id="aa31a-114">The constant value is any unsigned 32-bit integer indicating the number of events used for filtering.</span></span>

<span data-ttu-id="aa31a-115">Ao usar a cláusula HAVING, as cláusulas WHERE e BY são opcionais.</span><span class="sxs-lookup"><span data-stu-id="aa31a-115">When using the HAVING clause, the WHERE and BY clauses are optional.</span></span>

<span data-ttu-id="aa31a-116">A consulta de evento a seguir solicita que as notificações da classe **EmailEvent** sejam agrupadas em um evento 300 segundos após o primeiro evento que o WMI recebe.</span><span class="sxs-lookup"><span data-stu-id="aa31a-116">The following event query requests that notifications of the **EmailEvent** class be grouped into one event 300 seconds after the first event that WMI receives.</span></span> <span data-ttu-id="aa31a-117">Além disso, a consulta solicitará que a instância [**\_ \_ AggregateEvent**](--aggregateevent.md) seja entregue somente se o WMI receber mais de cinco eventos de email em 300 segundos.</span><span class="sxs-lookup"><span data-stu-id="aa31a-117">Also, the query requests the [**\_\_AggregateEvent**](--aggregateevent.md) instance should be delivered only if WMI receives more than five email events in that 300 seconds.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



<span data-ttu-id="aa31a-118">O exemplo a seguir agrupa todos os eventos recebidos em 600 segundos (ou seja, 10 minutos) pelo **TargetInstance**. Propriedade **SourceName** .</span><span class="sxs-lookup"><span data-stu-id="aa31a-118">The following example groups all events received in 600 seconds (that is, 10 minutes) by the **TargetInstance**.**SourceName** property.</span></span> <span data-ttu-id="aa31a-119">Neste exemplo, os eventos de agregação serão entregues somente se o número de eventos [**\_ NTLogEvent do Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) recebidos da mesma origem exceder 25.</span><span class="sxs-lookup"><span data-stu-id="aa31a-119">In this example, aggregate events are delivered only if the number of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) events received from the same source exceeds 25.</span></span> <span data-ttu-id="aa31a-120">Tenha em mente que o operador ISA faz com que a propriedade **TargetInstance** da classe de sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) represente uma instância da classe **Win32 \_ NTLogEvent** .</span><span class="sxs-lookup"><span data-stu-id="aa31a-120">Keep in mind that the ISA operator causes the **TargetInstance** property of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) system class to represent an instance of the **Win32\_NTLogEvent** class.</span></span>


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
