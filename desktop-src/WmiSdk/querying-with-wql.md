---
description: O linguagem WQL (WQL) é um subconjunto de linguagem SQL padrão de American National Standards Institute (ANSI SQL) com pequenas alterações semânticas para dar suporte ao WMI.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Consultando com WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8e2d3f68f4d7384781110958070b33b67a78405f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783792"
---
# <a name="querying-with-wql"></a><span data-ttu-id="f608d-103">Consultando com WQL</span><span class="sxs-lookup"><span data-stu-id="f608d-103">Querying with WQL</span></span>

<span data-ttu-id="f608d-104">O linguagem WQL (WQL) é um subconjunto de linguagem SQL padrão de American National Standards Institute (ANSI SQL) com pequenas alterações semânticas para dar suporte ao WMI.</span><span class="sxs-lookup"><span data-stu-id="f608d-104">The WMI Query Language (WQL) is a subset of standard American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes to support WMI.</span></span>

<span data-ttu-id="f608d-105">Para obter uma lista completa de palavras-chave WQL com suporte, consulte [WQL (SQL para WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f608d-105">For a complete list of supported WQL keywords, see [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span> <span data-ttu-id="f608d-106">Usar palavras-chave SQL para nomes de objeto ou propriedade pode restringir a análise de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="f608d-106">Using SQL keywords for object or property names may restrict a query from being parsed.</span></span> <span data-ttu-id="f608d-107">As seguintes palavras-chave SQL são restritas: **NULL**, **true** e **false**.</span><span class="sxs-lookup"><span data-stu-id="f608d-107">The following SQL keywords are restricted: **NULL**, **TRUE**, and **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="f608d-108">Há limites para o número de palavras-chave AND e OR que podem ser usadas em consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="f608d-108">There are limits to the number of AND and OR keywords that can be used in WQL queries.</span></span> <span data-ttu-id="f608d-109">Grandes números de palavras-chave WQL usadas em uma consulta complexa podem fazer com que o WMI retorne o código de erro de **\_ \_ \_ violação E de cota de WBEM** como um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f608d-109">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="f608d-110">O limite de palavras-chave WQL depende da complexidade da consulta.</span><span class="sxs-lookup"><span data-stu-id="f608d-110">The limit of WQL keywords depends on how complex the query is.</span></span>

 

<span data-ttu-id="f608d-111">As consultas podem usar a cláusula **Where** para extensão e personalização, embora não seja necessário.</span><span class="sxs-lookup"><span data-stu-id="f608d-111">Queries can use the **WHERE** clause for extension and customization, although it is not required.</span></span> <span data-ttu-id="f608d-112">A cláusula **Where** é composta de uma propriedade ou palavra-chave, um operador e uma constante.</span><span class="sxs-lookup"><span data-stu-id="f608d-112">The **WHERE** clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="f608d-113">Todas as cláusulas **Where** devem especificar um dos operadores predefinidos que são incluídos na WQL.</span><span class="sxs-lookup"><span data-stu-id="f608d-113">All **WHERE** clauses must specify one of the predefined operators that are included in WQL.</span></span> <span data-ttu-id="f608d-114">Para obter mais informações sobre a sintaxe, consulte a [cláusula WHERE](where-clause.md).</span><span class="sxs-lookup"><span data-stu-id="f608d-114">For more information about syntax, see [WHERE Clause](where-clause.md).</span></span> <span data-ttu-id="f608d-115">Para obter mais informações sobre operadores WQL válidos, consulte [operadores WQL](wql-operators.md).</span><span class="sxs-lookup"><span data-stu-id="f608d-115">For more information about valid WQL operators, see [WQL Operators](wql-operators.md).</span></span>

<span data-ttu-id="f608d-116">Assim como acontece com outras cadeias de caracteres de consulta SQL, você pode escapar suas consultas.</span><span class="sxs-lookup"><span data-stu-id="f608d-116">As with other SQL query strings, you can escape your queries.</span></span>

> [!Note]  
> <span data-ttu-id="f608d-117">O WQL não dá suporte a consultas ou associações de namespace cruzado.</span><span class="sxs-lookup"><span data-stu-id="f608d-117">WQL does not support cross-namespace queries or associations.</span></span> <span data-ttu-id="f608d-118">Você não pode consultar todas as instâncias de uma classe especificada que reside em todos os namespaces no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="f608d-118">You cannot query for all instances of a specified class residing in all of the namespaces on the target computer.</span></span>

 

<span data-ttu-id="f608d-119">O WQL dá suporte aos seguintes tipos de consultas:</span><span class="sxs-lookup"><span data-stu-id="f608d-119">WQL supports the following types of queries:</span></span>

-   <span data-ttu-id="f608d-120">Consultas de dados</span><span class="sxs-lookup"><span data-stu-id="f608d-120">Data queries</span></span>

    <span data-ttu-id="f608d-121">As consultas de dados são usadas para recuperar instâncias de classe e associações de dados.</span><span class="sxs-lookup"><span data-stu-id="f608d-121">Data queries are used to retrieve class instances and data associations.</span></span> <span data-ttu-id="f608d-122">Eles são o tipo de consulta mais comumente usado em aplicativos e scripts do WMI.</span><span class="sxs-lookup"><span data-stu-id="f608d-122">They are the most commonly used type of query in WMI scripts and applications.</span></span> <span data-ttu-id="f608d-123">Para obter mais informações sobre a sintaxe de consultas de dados, consulte [solicitando dados de instância de classe](requesting-class-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="f608d-123">For more information about the syntax of data queries, see [Requesting Class Instance Data](requesting-class-instance-data.md).</span></span> <span data-ttu-id="f608d-124">Para obter mais informações sobre associações, consulte [declarando uma classe de associação](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="f608d-124">For more information about associations, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="f608d-125">WQL não oferece suporte a consultas de tipos de dataArray.</span><span class="sxs-lookup"><span data-stu-id="f608d-125">WQL does not support queries of array datatypes.</span></span>

     

    <span data-ttu-id="f608d-126">O exemplo de consulta de dados a seguir solicita o arquivo de log de eventos chamado "Application" de todas as instâncias do [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="f608d-126">The following data query example requests the event log file named "Application" from all instances of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   <span data-ttu-id="f608d-127">Consultas de evento</span><span class="sxs-lookup"><span data-stu-id="f608d-127">Event queries</span></span>

    <span data-ttu-id="f608d-128">Os consumidores usam consultas de eventos para se registrar para receber notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="f608d-128">Consumers use event queries to register to receive notification of events.</span></span> <span data-ttu-id="f608d-129">Provedores de eventos usam consultas de eventos para se registrar para dar suporte a um ou mais eventos.</span><span class="sxs-lookup"><span data-stu-id="f608d-129">Event providers use event queries to register to support one or more events.</span></span> <span data-ttu-id="f608d-130">Para obter mais informações sobre consultas de eventos, consulte [recebendo notificações de eventos](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f608d-130">For more information about event queries, see [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

    <span data-ttu-id="f608d-131">O seguinte exemplo de consulta de evento por um consumidor de evento temporário solicita notificação quando uma nova instância de uma classe derivada do [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) é criada.</span><span class="sxs-lookup"><span data-stu-id="f608d-131">The following example event query by a temporary event consumer requests notification when a new instance of a class derived from [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) is created.</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   <span data-ttu-id="f608d-132">Consultas de esquema</span><span class="sxs-lookup"><span data-stu-id="f608d-132">Schema queries</span></span>

    <span data-ttu-id="f608d-133">As consultas de esquema são usadas para recuperar definições de classe (em vez de instâncias de classe) e associações de esquema.</span><span class="sxs-lookup"><span data-stu-id="f608d-133">Schema queries are used to retrieve class definitions (rather than class instances) and schema associations.</span></span> <span data-ttu-id="f608d-134">Provedores de classe usam consultas de esquema para especificar as classes que dão suporte ao se registrarem.</span><span class="sxs-lookup"><span data-stu-id="f608d-134">Class providers use schema queries to specify the classes that they support when they register.</span></span> <span data-ttu-id="f608d-135">Para obter mais informações sobre consultas de esquema, consulte [recuperando definições de classe](retrieving-class-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="f608d-135">For more information about schema queries, see [Retrieving Class Definitions](retrieving-class-definitions.md).</span></span>

    <span data-ttu-id="f608d-136">O exemplo de consulta de esquema a seguir mostra a sintaxe especial.</span><span class="sxs-lookup"><span data-stu-id="f608d-136">The following example schema query shows the special syntax.</span></span>

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="f608d-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f608d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f608d-138">Formato de data e hora do WMI</span><span class="sxs-lookup"><span data-stu-id="f608d-138">WMI Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 
