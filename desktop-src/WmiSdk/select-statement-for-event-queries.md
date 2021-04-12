---
description: Descreve a sintaxe básica de uma instrução SELECT para consultas de evento.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: Instrução SELECT para consultas de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab840072269d04987bf42939f1f566ee6b99afab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171444"
---
# <a name="select-statement-for-event-queries"></a><span data-ttu-id="ab9a4-103">Instrução SELECT para consultas de evento</span><span class="sxs-lookup"><span data-stu-id="ab9a4-103">SELECT Statement for Event Queries</span></span>

<span data-ttu-id="ab9a4-104">Você pode usar uma variedade de instruções SELECT para consultar informações de eventos.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-104">You can use a variety of SELECT statements to query for event information.</span></span> <span data-ttu-id="ab9a4-105">As instruções podem ser instruções básicas ou podem ser mais restritivas para restringir o conjunto de resultados retornado pela consulta.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="ab9a4-106">O exemplo a seguir é uma instrução SELECT básica que é usada para consultar informações de evento.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-106">The following example is a basic SELECT statement that is used to query for event information.</span></span>


```sql
SELECT * FROM EventClass
```



<span data-ttu-id="ab9a4-107">Quando um consumidor envia uma consulta, é uma solicitação para ser notificado de todas as ocorrências do evento representado por **EventClass**.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-107">When a consumer submits a query, it is a request to be notified of all occurrences of the event represented by **EventClass**.</span></span> <span data-ttu-id="ab9a4-108">Essa solicitação inclui uma solicitação de notificação sobre todas as propriedades do sistema de eventos e não do sistema.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-108">This request includes a request for notification about all of the event system and nonsystem properties.</span></span> <span data-ttu-id="ab9a4-109">Quando um provedor de eventos envia uma consulta, ele registra o suporte para gerar notificações quando um evento representado por **EventClass** ocorre.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-109">When an event provider submits a query, it registers support for generating notifications when an event represented by **EventClass** occurs.</span></span>

<span data-ttu-id="ab9a4-110">Os consumidores podem especificar propriedades individuais em vez do asterisco ( \* ) na instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-110">Consumers can specify individual properties instead of the asterisk (\*) in the SELECT statement.</span></span>

<span data-ttu-id="ab9a4-111">O exemplo a seguir mostra como consultar propriedades específicas.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-111">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



<span data-ttu-id="ab9a4-112">No entanto, todas as propriedades de um objeto inserido são retornadas, mesmo que a consulta especifique as propriedades do objeto inserido.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-112">However, all of the properties of an embedded object are returned, even if the query specifies embedded object properties.</span></span>

<span data-ttu-id="ab9a4-113">O exemplo a seguir mostra duas consultas que retornam os mesmos dados.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-113">The following example shows two queries that return the same data.</span></span>


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



<span data-ttu-id="ab9a4-114">Se uma propriedade do sistema não for relevante para uma consulta específica, ela conterá **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-114">If a system property is not relevant for a specific query, it contains **NULL**.</span></span> <span data-ttu-id="ab9a4-115">Por exemplo, o valor da Propriedade do sistema **\_ \_ RelPath** é **nulo** para todas as consultas de evento.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-115">For example, the value of the **\_\_RELPATH** system property is **NULL** for all event queries.</span></span>

<span data-ttu-id="ab9a4-116">As propriedades do sistema a seguir contêm **NULL** para consultas de evento:</span><span class="sxs-lookup"><span data-stu-id="ab9a4-116">The following system properties contain **NULL** for event queries:</span></span>

<dl> <span data-ttu-id="ab9a4-117">\_\_Namespace</span><span class="sxs-lookup"><span data-stu-id="ab9a4-117">\_\_Namespace</span></span>  
<span data-ttu-id="ab9a4-118">\_\_Multi-Path</span><span class="sxs-lookup"><span data-stu-id="ab9a4-118">\_\_Path</span></span>  
<span data-ttu-id="ab9a4-119">\_\_RelPath</span><span class="sxs-lookup"><span data-stu-id="ab9a4-119">\_\_RelPath</span></span>  
<span data-ttu-id="ab9a4-120">\_\_Servidor</span><span class="sxs-lookup"><span data-stu-id="ab9a4-120">\_\_Server</span></span>  
</dl>

<span data-ttu-id="ab9a4-121">Para obter mais informações, consulte [referência de propriedades do sistema WMI](wmi-system-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ab9a4-121">For more information, see [WMI System Property Reference](wmi-system-properties.md).</span></span>

<span data-ttu-id="ab9a4-122">Todas as consultas de evento podem incluir uma [cláusula WHERE](where-clause.md)opcional, mas as cláusulas WHERE são usadas principalmente pelos consumidores para especificar filtragem adicional.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-122">All event queries can include an optional [WHERE clause](where-clause.md), but WHERE clauses are primarily used by consumers to specify additional filtering.</span></span> <span data-ttu-id="ab9a4-123">É altamente recomendável que os consumidores sempre especifiquem uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-123">It is strongly recommended that consumers always specify a WHERE clause.</span></span> <span data-ttu-id="ab9a4-124">O custo de uma consulta complexa é mínimo em comparação com o custo de entrega e processamento de notificações desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-124">The cost of a complex query is minimal compared to the cost of delivering and processing unneeded notifications.</span></span>

<span data-ttu-id="ab9a4-125">O exemplo a seguir mostra uma consulta que solicita notificações de todos os eventos de modificação de instância que afetam a classe hipotética **EmailEvent**.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-125">The following example shows a query that requests notifications of all instance modification events that affect the hypothetical class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent
```



<span data-ttu-id="ab9a4-126">Se os eventos associados a **EmailEvent** ocorrem com frequência, o consumidor é inundado com eventos.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-126">If events associated with **EmailEvent** occur frequently, the consumer is flooded with events.</span></span> <span data-ttu-id="ab9a4-127">Uma consulta melhor solicita eventos somente quando condições específicas usam propriedades da classe especificada, como quando o nível de importância é alto.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-127">A better query requests events only when specific conditions use properties of the class specified, such as when the importance level is high.</span></span>

<span data-ttu-id="ab9a4-128">O exemplo a seguir mostra a consulta que você pode usar se **EmailImportance** for uma propriedade da classe **EmailEvent**.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-128">The following example shows the query you can use if **EmailImportance** is a property of the class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



<span data-ttu-id="ab9a4-129">Observe que o WMI pode rejeitar uma consulta por vários motivos.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-129">Note that WMI can reject a query for a number of reasons.</span></span> <span data-ttu-id="ab9a4-130">Por exemplo, a consulta pode ser muito complexa ou de uso intensivo de recursos para avaliação.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-130">For example, the query can be too complex or resource-intensive for evaluation.</span></span> <span data-ttu-id="ab9a4-131">Quando isso ocorre, o WMI retorna códigos de erro específicos, como a **\_ \_ \_ consulta WBEM E inválida**.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-131">When this occurs, WMI returns specific error codes, such as **WBEM\_E\_INVALID\_QUERY**.</span></span>

<span data-ttu-id="ab9a4-132">As propriedades de objetos inseridos podem ser usadas na cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-132">Properties of embedded objects can be used in the WHERE clause.</span></span>

<span data-ttu-id="ab9a4-133">O exemplo a seguir mostra como consultar objetos em que a propriedade **TargetInstance** da classe System [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) é um objeto de [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) inserido e **FreeSpace** é uma propriedade do disco **\_ lógico do Win32**.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-133">The following example shows how to query for objects where the **TargetInstance** property of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system class is an embedded [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) object and **FreeSpace** is a property of **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a><span data-ttu-id="ab9a4-134">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ab9a4-134">Examples</span></span>

<span data-ttu-id="ab9a4-135">O exemplo de [Monitor de evento de criação de nome de processo específico](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) no TechNet usa a instrução SELECT para monitorar eventos de criação de instância do WMI para \_ o processo do Win32, filtrando um nome de processo específico.</span><span class="sxs-lookup"><span data-stu-id="ab9a4-135">The [Monitor creation event for specific process name](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) VBScript sample on TechNet uses the SELECT statement to monitor WMI instance creation events for Win32\_Process, filtering for a specific process name.</span></span>

 

 
