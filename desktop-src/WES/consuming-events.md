---
title: Consumindo eventos (log de eventos do Windows)
description: Você pode consumir eventos de canais ou de arquivos de log.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb3fb1b36a0cd4ecf836a8893bc1abc14e46451
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105796462"
---
# <a name="consuming-events-windows-event-log"></a><span data-ttu-id="0c033-103">Consumindo eventos (log de eventos do Windows)</span><span class="sxs-lookup"><span data-stu-id="0c033-103">Consuming Events (Windows Event Log)</span></span>

<span data-ttu-id="0c033-104">Você pode consumir eventos de canais ou de arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="0c033-104">You can consume events from channels or from log files.</span></span> <span data-ttu-id="0c033-105">Para consumir eventos, você pode consumir todos os eventos ou pode especificar uma expressão XPath que identifique os eventos que você deseja consumir.</span><span class="sxs-lookup"><span data-stu-id="0c033-105">To consume events, you can consume all events or you can specify an XPath expression that identifies the events that you want to consume.</span></span> <span data-ttu-id="0c033-106">Para determinar os elementos e atributos de um evento que você pode usar em sua expressão XPath, consulte [esquema de evento](eventschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="0c033-106">To determine the elements and attributes of an event that you can use in your XPath expression, see [Event Schema](eventschema-schema.md).</span></span>

<span data-ttu-id="0c033-107">O log de eventos do Windows dá suporte a um subconjunto do XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="0c033-107">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="0c033-108">Para obter detalhes sobre as limitações, consulte [limitações do XPath 1,0](#xpath-10-limitations).</span><span class="sxs-lookup"><span data-stu-id="0c033-108">For details on the limitations, see [XPath 1.0 limitations](#xpath-10-limitations).</span></span>

<span data-ttu-id="0c033-109">Os exemplos a seguir mostram expressões XPath simples.</span><span class="sxs-lookup"><span data-stu-id="0c033-109">The following examples show simple XPath expressions.</span></span>


```XML
// The following query selects all events from the channel or log file
XPath Query: *

// The following query selects all the LowOnMemory events from the channel or log file
XPath Query: *[UserData/LowOnMemory]

// The following query selects all events with a severity level of 1 (Critical) from the channel or log file
XPath Query: *[System/Level=1]

// The following query shows a compound expression that selects all events from the channel or log file
// where the printer's name is MyPrinter and severity level is 1.
XPath Query: *[UserData/*/PrinterName="MyPrinter" and System/Level=1]

// The following query selects all events from the channel or log file where the severity level is
// less than or equal to 3 and the event occurred in the last 24 hour period.
XPath Query: *[System[(Level <= 3) and TimeCreated[timediff(@SystemTime) <= 86400000]]]
```



<span data-ttu-id="0c033-110">Você pode usar as expressões XPath diretamente ao chamar as funções [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ou pode usar uma consulta XML estruturada que contém a expressão XPath.</span><span class="sxs-lookup"><span data-stu-id="0c033-110">You can use the XPath expressions directly when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions or you can use a structured XML query that contains the XPath expression.</span></span> <span data-ttu-id="0c033-111">Para consultas simples que consultam eventos de uma única fonte, o uso de uma expressão XPath é bom.</span><span class="sxs-lookup"><span data-stu-id="0c033-111">For simple queries that query events from a single source, using an XPath expression is fine.</span></span> <span data-ttu-id="0c033-112">Se a expressão XPath for uma expressão composta que contenha mais de 20 expressões ou se você estiver consultando eventos de várias fontes, deverá usar uma consulta XML estruturada.</span><span class="sxs-lookup"><span data-stu-id="0c033-112">If the XPath expression is a compound expression that contains more than 20 expressions or you are querying for events from multiple sources, then you must use a structured XML query.</span></span> <span data-ttu-id="0c033-113">Para obter detalhes sobre os elementos de uma consulta XML estruturada, consulte [esquema de consulta](queryschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="0c033-113">For details on the elements of a structured XML query, see [Query Schema](queryschema-schema.md).</span></span>

<span data-ttu-id="0c033-114">Uma consulta estruturada identifica a origem dos eventos e um ou mais seletores ou supressers.</span><span class="sxs-lookup"><span data-stu-id="0c033-114">A structured query identifies the source of the events and one or more selectors or suppressors.</span></span> <span data-ttu-id="0c033-115">Um seletor contém expressões XPath que selecionam eventos da origem e um supressor contém uma expressão XPath que impede a seleção de eventos.</span><span class="sxs-lookup"><span data-stu-id="0c033-115">A selector contains an XPath expressions that selects events from the source and a suppressor contains an XPath expression that prevents events from being selected.</span></span> <span data-ttu-id="0c033-116">Você pode selecionar eventos de mais de uma fonte.</span><span class="sxs-lookup"><span data-stu-id="0c033-116">You can select events from more than one source.</span></span> <span data-ttu-id="0c033-117">Se um seletor e o supressor identificarem o mesmo evento, o evento não será incluído no resultado.</span><span class="sxs-lookup"><span data-stu-id="0c033-117">If a selector and suppressor identify the same event, the event is not included in the result.</span></span>

<span data-ttu-id="0c033-118">O seguinte mostra uma consulta XML estruturada que especifica um conjunto de seletores e supressers.</span><span class="sxs-lookup"><span data-stu-id="0c033-118">The following shows a structured XML query that specifies a set of selectors and suppressors.</span></span>


```XML
<QueryList>
  <Query Id="0">
    <Select Path="Application">
        *[System[(Level <= 3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
  </Query>
</QueryList>
```



<span data-ttu-id="0c033-119">O conjunto de resultados da consulta não contém um instantâneo dos eventos no momento da consulta.</span><span class="sxs-lookup"><span data-stu-id="0c033-119">The result set from the query does not contain a snapshot of the events at the time of the query.</span></span> <span data-ttu-id="0c033-120">Em vez disso, o conjunto de resultados inclui os eventos no momento da consulta e também conterá todos os novos eventos que são gerados que correspondam aos critérios de consulta enquanto você está enumerando os resultados.</span><span class="sxs-lookup"><span data-stu-id="0c033-120">Instead, the result set includes the events at the time of the query and will also contain all new events that are raised that match the query criteria while you are enumerating the results.</span></span>

> [!Note]  
> <span data-ttu-id="0c033-121">A ordem dos eventos é preservada para eventos que são gravados pelo mesmo thread.</span><span class="sxs-lookup"><span data-stu-id="0c033-121">The order of the events is preserved for events that are written by the same thread.</span></span> <span data-ttu-id="0c033-122">No entanto, é possível que os eventos escritos por threads separados em diferentes processadores de um computador com vários processadores apareçam fora de ordem.</span><span class="sxs-lookup"><span data-stu-id="0c033-122">However, it is possible for events written by separate threads on different processors of a multiple processor computer to appear out of order.</span></span>

 

<span data-ttu-id="0c033-123">Para obter detalhes sobre como consumir eventos, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="0c033-123">For details on consuming events, see the following topics:</span></span>

-   [<span data-ttu-id="0c033-124">Consultando eventos</span><span class="sxs-lookup"><span data-stu-id="0c033-124">Querying for Events</span></span>](querying-for-events.md)
-   [<span data-ttu-id="0c033-125">Inscrevendo-se em eventos</span><span class="sxs-lookup"><span data-stu-id="0c033-125">Subscribing to Events</span></span>](subscribing-to-events.md)
-   [<span data-ttu-id="0c033-126">Renderizando eventos</span><span class="sxs-lookup"><span data-stu-id="0c033-126">Rendering Events</span></span>](rendering-events.md)
-   [<span data-ttu-id="0c033-127">Formatando mensagens de evento</span><span class="sxs-lookup"><span data-stu-id="0c033-127">Formatting Event Messages</span></span>](formatting-event-messages.md)
-   [<span data-ttu-id="0c033-128">Eventos de indicador</span><span class="sxs-lookup"><span data-stu-id="0c033-128">Bookmarking Events</span></span>](bookmarking-events.md)

<span data-ttu-id="0c033-129">As ferramentas de usuário final padrão para o evento de consumo são:</span><span class="sxs-lookup"><span data-stu-id="0c033-129">The standard end user tools for consuming event are:</span></span>

-   <span data-ttu-id="0c033-130">[Visualizador de Eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="0c033-130">[Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span></span>
-   <span data-ttu-id="0c033-131">O cmdlet [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0c033-131">The Windows PowerShell [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) cmdlet</span></span>
-   [<span data-ttu-id="0c033-132">**WevtUtil**</span><span class="sxs-lookup"><span data-stu-id="0c033-132">**WevtUtil**</span></span>](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a><span data-ttu-id="0c033-133">Limitações do XPath 1,0</span><span class="sxs-lookup"><span data-stu-id="0c033-133">XPath 1.0 limitations</span></span>

<span data-ttu-id="0c033-134">O log de eventos do Windows dá suporte a um subconjunto do XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="0c033-134">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="0c033-135">A principal restrição é que apenas elementos XML que representam eventos podem ser selecionados por um seletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="0c033-135">The primary restriction is that only XML elements that represent events can be selected by an event selector.</span></span> <span data-ttu-id="0c033-136">Uma consulta XPath que não seleciona um evento não é válida.</span><span class="sxs-lookup"><span data-stu-id="0c033-136">An XPath query that does not select an event is not valid.</span></span> <span data-ttu-id="0c033-137">Todos os caminhos de seletor válidos começam com \* ou "Event".</span><span class="sxs-lookup"><span data-stu-id="0c033-137">All valid selector paths start with \* or "Event".</span></span> <span data-ttu-id="0c033-138">Todos os caminhos de localização operam nos nós de evento e são compostos por uma série de etapas.</span><span class="sxs-lookup"><span data-stu-id="0c033-138">All location paths operate on the event nodes and are composed of a series of steps.</span></span> <span data-ttu-id="0c033-139">Cada etapa é uma estrutura de três partes: o eixo, o teste de nó e o predicado.</span><span class="sxs-lookup"><span data-stu-id="0c033-139">Each step is a structure of three parts: the axis, node test, and predicate.</span></span> <span data-ttu-id="0c033-140">Para obter mais informações sobre essas partes e sobre o XPath 1,0, consulte [linguagem de caminho XML (XPath)](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="0c033-140">For more information about these parts and about XPath 1.0, see [XML Path Language (XPath)](https://www.w3.org/TR/xpath).</span></span> <span data-ttu-id="0c033-141">O log de eventos do Windows coloca as seguintes restrições na expressão:</span><span class="sxs-lookup"><span data-stu-id="0c033-141">Windows Event Log places the following restrictions on the expression:</span></span>

-   <span data-ttu-id="0c033-142">Axis: há suporte apenas para o eixo filho (padrão) e o atributo (e seu "@") de atalho.</span><span class="sxs-lookup"><span data-stu-id="0c033-142">Axis: Only the Child (default) and Attribute (and its shorthand "@") axis are supported.</span></span>
-   <span data-ttu-id="0c033-143">Testes de nó: há suporte apenas para os nomes de nó e os testes de NCName.</span><span class="sxs-lookup"><span data-stu-id="0c033-143">Node Tests: Only node names and NCName tests are supported.</span></span> <span data-ttu-id="0c033-144">O \* caractere "", que seleciona qualquer caractere, tem suporte.</span><span class="sxs-lookup"><span data-stu-id="0c033-144">The "\*" character, which selects any character, is supported.</span></span>
-   <span data-ttu-id="0c033-145">Predicados: qualquer expressão XPath válida será aceitável se os caminhos de localização estiverem em conformidade com as seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="0c033-145">Predicates: Any valid XPath expression is acceptable if the location paths conform to the following restrictions:</span></span>
    -   <span data-ttu-id="0c033-146">Há suporte para operadores padrão **ou**, **e**, =,! =, <=, <, >=, > e parênteses.</span><span class="sxs-lookup"><span data-stu-id="0c033-146">Standard operators **OR**, **AND**, =, !=, <=, <, >=, >, and parentheses are supported.</span></span>
    -   <span data-ttu-id="0c033-147">Não há suporte para a geração de um valor de cadeia de caracteres para um nome de nó.</span><span class="sxs-lookup"><span data-stu-id="0c033-147">Generating a string value for a node name is not supported.</span></span>
    -   <span data-ttu-id="0c033-148">Não há suporte para a avaliação na ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="0c033-148">Evaluation in reverse order is not supported.</span></span>
    -   <span data-ttu-id="0c033-149">Não há suporte para conjuntos de nós.</span><span class="sxs-lookup"><span data-stu-id="0c033-149">Node sets are not supported.</span></span>
    -   <span data-ttu-id="0c033-150">Não há suporte para o escopo do namespace.</span><span class="sxs-lookup"><span data-stu-id="0c033-150">Namespace scoping is not supported.</span></span>
    -   <span data-ttu-id="0c033-151">Não há suporte para namespace, processamento e nós de comentário.</span><span class="sxs-lookup"><span data-stu-id="0c033-151">Namespace, processing, and comment nodes are not supported.</span></span>
    -   <span data-ttu-id="0c033-152">Não há suporte para o tamanho do contexto.</span><span class="sxs-lookup"><span data-stu-id="0c033-152">Context size is not supported.</span></span>
    -   <span data-ttu-id="0c033-153">Não há suporte para associações de variáveis.</span><span class="sxs-lookup"><span data-stu-id="0c033-153">Variable bindings are not supported.</span></span>
    -   <span data-ttu-id="0c033-154">A função position e sua referência de matriz abreviada têm suporte (somente em nós folha).</span><span class="sxs-lookup"><span data-stu-id="0c033-154">The position function, and its shorthand array reference, is supported (on leaf nodes only).</span></span>
    -   <span data-ttu-id="0c033-155">Há suporte para a função Band.</span><span class="sxs-lookup"><span data-stu-id="0c033-155">The Band function is supported.</span></span> <span data-ttu-id="0c033-156">A função executa um e bit e para dois argumentos de número inteiro.</span><span class="sxs-lookup"><span data-stu-id="0c033-156">The function performs a bitwise AND for two integer number arguments.</span></span> <span data-ttu-id="0c033-157">Se o resultado do bit e for diferente de zero, a função será avaliada como true; caso contrário, a função será avaliada como false.</span><span class="sxs-lookup"><span data-stu-id="0c033-157">If the result of the bitwise AND is nonzero, the function evaluates to true; otherwise, the function evaluates to false.</span></span>
    -   <span data-ttu-id="0c033-158">Há suporte para a função TIMEDIFF.</span><span class="sxs-lookup"><span data-stu-id="0c033-158">The timediff function is supported.</span></span> <span data-ttu-id="0c033-159">A função computa a diferença entre o segundo argumento e o primeiro argumento.</span><span class="sxs-lookup"><span data-stu-id="0c033-159">The function computes the difference between the second argument and the first argument.</span></span> <span data-ttu-id="0c033-160">Um dos argumentos deve ser um número literal.</span><span class="sxs-lookup"><span data-stu-id="0c033-160">One of the arguments must be a literal number.</span></span> <span data-ttu-id="0c033-161">Os argumentos devem usar a representação FILETIME.</span><span class="sxs-lookup"><span data-stu-id="0c033-161">The arguments must use FILETIME representation.</span></span> <span data-ttu-id="0c033-162">O resultado é o número de milissegundos entre as duas vezes.</span><span class="sxs-lookup"><span data-stu-id="0c033-162">The result is the number of milliseconds between the two times.</span></span> <span data-ttu-id="0c033-163">O resultado será positivo se o segundo argumento representar uma hora posterior; caso contrário, será negativo.</span><span class="sxs-lookup"><span data-stu-id="0c033-163">The result is positive if the second argument represents a later time; otherwise, it is negative.</span></span> <span data-ttu-id="0c033-164">Quando o segundo argumento não é fornecido, a hora atual do sistema é usada.</span><span class="sxs-lookup"><span data-stu-id="0c033-164">When the second argument is not provided, the current system time is used.</span></span>

 

 
