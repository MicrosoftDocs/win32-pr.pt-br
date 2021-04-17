---
title: Escrevendo um manifesto de instrumentação
description: Aplicativos e DLLs usam um manifesto de instrumentação para identificar seus provedores de instrumentação e os eventos que os provedores gravam.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366051"
---
# <a name="writing-an-instrumentation-manifest"></a><span data-ttu-id="2e63f-103">Escrevendo um manifesto de instrumentação</span><span class="sxs-lookup"><span data-stu-id="2e63f-103">Writing an Instrumentation Manifest</span></span>

<span data-ttu-id="2e63f-104">Aplicativos e DLLs usam um manifesto de instrumentação para identificar seus provedores de instrumentação e os eventos que os provedores gravam.</span><span class="sxs-lookup"><span data-stu-id="2e63f-104">Applications and DLLs use an instrumentation manifest to identify their instrumentation providers and the events that the providers write.</span></span> <span data-ttu-id="2e63f-105">Um manifesto é um arquivo XML que contém os elementos que identificam seu provedor.</span><span class="sxs-lookup"><span data-stu-id="2e63f-105">A manifest is an XML file that contains the elements that identify your provider.</span></span> <span data-ttu-id="2e63f-106">A Convenção é usar. Man como a extensão do seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="2e63f-106">The convention is to use .man as the extension for your manifest.</span></span> <span data-ttu-id="2e63f-107">O manifesto deve estar em conformidade com o XSD do manifesto do evento.</span><span class="sxs-lookup"><span data-stu-id="2e63f-107">The manifest must conform to the event manifest XSD.</span></span> <span data-ttu-id="2e63f-108">Para obter detalhes sobre o esquema, consulte [esquema EventManifest](eventmanifestschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="2e63f-108">For details on the schema, see [EventManifest Schema](eventmanifestschema-schema.md).</span></span>

<span data-ttu-id="2e63f-109">Um provedor de instrumentação é qualquer aplicativo ou DLL que chama as funções [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)ou [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) para gravar eventos em uma sessão de rastreamento de ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) ) ou em um canal de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="2e63f-109">An instrumentation provider is any application or DLL that calls the [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring), or [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) functions to write events to an [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) tracing session or an Event Log channel.</span></span> <span data-ttu-id="2e63f-110">Um aplicativo pode definir um único provedor de instrumentação que cubra todos os eventos que ele grava ou pode definir um provedor para o aplicativo e um provedor para cada uma de suas DLLs.</span><span class="sxs-lookup"><span data-stu-id="2e63f-110">An application can define a single instrumentation provider that covers all events that it writes or it can define a provider for the application and a provider for each of its DLLs.</span></span> <span data-ttu-id="2e63f-111">O número de provedores que o aplicativo define no manifesto depende exclusivamente de como o aplicativo deseja organizar os eventos que ele grava.</span><span class="sxs-lookup"><span data-stu-id="2e63f-111">The number of providers that the application defines in the manifest depends solely on how the application wants to organize the events that it writes.</span></span>

<span data-ttu-id="2e63f-112">A vantagem de especificar um provedor para cada DLL é que você pode habilitar e desabilitar os provedores individuais e, portanto, os eventos que eles geram.</span><span class="sxs-lookup"><span data-stu-id="2e63f-112">The advantage of specifying a provider for each DLL is that you can then enable and disable the individual providers and thus the events that they generate.</span></span> <span data-ttu-id="2e63f-113">Essa vantagem se aplica somente se o provedor estiver habilitado por uma sessão de rastreamento ETW.</span><span class="sxs-lookup"><span data-stu-id="2e63f-113">This advantage applies only if the provider is enabled by an ETW tracing session.</span></span> <span data-ttu-id="2e63f-114">Todos os eventos que especificam um canal de log de eventos são sempre gravados nesse canal.</span><span class="sxs-lookup"><span data-stu-id="2e63f-114">Any events that specify an event log channel are always written to that channel.</span></span>

<span data-ttu-id="2e63f-115">O manifesto deve identificar o provedor e os eventos que ele grava, mas os outros metadados, como canais, níveis e palavras-chave, são opcionais; Se você definir os metadados opcionais, dependerá de quem consumirá os eventos.</span><span class="sxs-lookup"><span data-stu-id="2e63f-115">The manifest must identify the provider and the events that it writes but the other metadata such as channels, levels, and keywords are optional; whether you define the optional metadata depends on who will be consuming the events.</span></span> <span data-ttu-id="2e63f-116">Por exemplo, se os administradores ou a equipe de suporte consumirem os eventos usando uma ferramenta como a Visualizador de Eventos do Windows que lê eventos de canais de log de eventos, você deverá definir os canais nos quais os eventos são gravados.</span><span class="sxs-lookup"><span data-stu-id="2e63f-116">For example, if administrators or support personnel consume the events using a tool like the Windows Event Viewer that reads events from event log channels, then you must define the channels to which the events are written.</span></span> <span data-ttu-id="2e63f-117">No entanto, se o provedor só for habilitado por uma sessão de rastreamento ETW, você não precisará definir canais.</span><span class="sxs-lookup"><span data-stu-id="2e63f-117">However, if the provider will only be enabled by an ETW tracing session, then you do not need to define channels.</span></span>

<span data-ttu-id="2e63f-118">Embora os metadados níveis, tarefas, opcodes e palavras-chave sejam opcionais, você deve usá-los para agrupar logicamente ou segmentar os eventos.</span><span class="sxs-lookup"><span data-stu-id="2e63f-118">Although the levels, tasks, opcodes, and keywords metadata are optional, you should use them to logically group or bucket the events.</span></span> <span data-ttu-id="2e63f-119">O agrupamento de eventos ajuda os consumidores a consumir apenas os eventos que são interessantes.</span><span class="sxs-lookup"><span data-stu-id="2e63f-119">Grouping the events helps the consumers consume only those events that are of interest.</span></span> <span data-ttu-id="2e63f-120">Por exemplo, o consumidor poderia consultar todos os eventos em que o nível é "crítico" e a palavra-chave é "gravar" ou consultar todos os eventos gravados por uma tarefa específica.</span><span class="sxs-lookup"><span data-stu-id="2e63f-120">For example, the consumer could query for all events where level is "critical" and keyword is "write", or query for all events written by a specific task.</span></span>

<span data-ttu-id="2e63f-121">Além dos consumidores que usam o nível e as palavras-chave para consumir tipos específicos de eventos, uma sessão de rastreamento ETW pode usar o nível e os metadados de palavra-chave para informar ao ETW para limitar os eventos que são gravados no log de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="2e63f-121">In addition to consumers using level and keywords to consume specific types of events, an ETW tracing session can use the level and keyword metadata to tell ETW to limit the events that are written to the event tracing log.</span></span> <span data-ttu-id="2e63f-122">Por exemplo, a sessão pode limitar os eventos a apenas eventos nos quais o nível é "erro" ou "crítico" e a palavra-chave é "leitura".</span><span class="sxs-lookup"><span data-stu-id="2e63f-122">For example, the session could limit the events to only events where level is "error" or "critical" and keyword is "read".</span></span>

<span data-ttu-id="2e63f-123">Um provedor pode definir filtros que uma sessão usa para filtrar os eventos com base nos dados do evento.</span><span class="sxs-lookup"><span data-stu-id="2e63f-123">A provider can define filters that a session uses to filter the events based on event data.</span></span> <span data-ttu-id="2e63f-124">Com o nível e as palavras-chave, o ETW determina se o evento é gravado no log, mas com filtros, o provedor usa os critérios de dados de filtro para determinar se ele grava o evento nessa sessão.</span><span class="sxs-lookup"><span data-stu-id="2e63f-124">With level and keywords, ETW determines whether the event is written to the log but with filters, the provider uses the filter data criteria to determine whether it writes the event to that session.</span></span> <span data-ttu-id="2e63f-125">Os filtros são aplicáveis somente quando uma sessão de rastreamento ETW habilita seu provedor.</span><span class="sxs-lookup"><span data-stu-id="2e63f-125">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="2e63f-126">As seções a seguir mostram como definir os componentes do manifesto:</span><span class="sxs-lookup"><span data-stu-id="2e63f-126">The following sections show how to define the components of the manifest:</span></span>

-   [<span data-ttu-id="2e63f-127">Identificando o provedor</span><span class="sxs-lookup"><span data-stu-id="2e63f-127">Identifying the provider</span></span>](identifying-the-provider.md)
-   [<span data-ttu-id="2e63f-128">Definindo os canais nos quais os eventos são gravados</span><span class="sxs-lookup"><span data-stu-id="2e63f-128">Defining the channels to where the events are written</span></span>](defining-channels.md)
-   [<span data-ttu-id="2e63f-129">Definindo os níveis de severidade dos eventos que o provedor grava</span><span class="sxs-lookup"><span data-stu-id="2e63f-129">Defining the severity levels of events that the provider writes</span></span>](defining-severity-levels.md)
-   [<span data-ttu-id="2e63f-130">Definindo as tarefas e operações que seu provedor executa</span><span class="sxs-lookup"><span data-stu-id="2e63f-130">Defining the tasks and operations that your provider performs</span></span>](defining-tasks-and-opcodes.md)
-   [<span data-ttu-id="2e63f-131">Definindo as palavras-chave que classificam os eventos que o provedor grava</span><span class="sxs-lookup"><span data-stu-id="2e63f-131">Defining the keywords that classify the events that the provider writes</span></span>](defining-keywords-used-to-classify-types-of-events.md)
-   [<span data-ttu-id="2e63f-132">Definindo os filtros que o provedor usa para filtrar os eventos que ele grava</span><span class="sxs-lookup"><span data-stu-id="2e63f-132">Defining the filters that the provider uses to filter the events that it writes</span></span>](defining-filters.md)
-   [<span data-ttu-id="2e63f-133">Definindo os mapas de nome/valor que os dados de modelo referenciam</span><span class="sxs-lookup"><span data-stu-id="2e63f-133">Defining the name/value maps that your template data references</span></span>](defining-name-value-mappings.md)
-   [<span data-ttu-id="2e63f-134">Definindo os modelos que definem os dados específicos do evento</span><span class="sxs-lookup"><span data-stu-id="2e63f-134">Defining the templates that define the event-specific data</span></span>](defining-event-data-templates.md)
-   [<span data-ttu-id="2e63f-135">Definindo os eventos que o provedor grava</span><span class="sxs-lookup"><span data-stu-id="2e63f-135">Defining the events that the provider writes</span></span>](defining-events.md)

<span data-ttu-id="2e63f-136">Embora seja possível criar um manifesto de instrumentação manualmente, você deve considerar o uso da ferramenta ECManGen.exe que está incluída na \\ pasta bin do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="2e63f-136">Although you can author an instrumentation manifest manually, you should consider using the ECManGen.exe tool that is included in the \\Bin folder of the Windows SDK.</span></span> <span data-ttu-id="2e63f-137">A ferramenta de ECManGen.exe usa uma GUI que orienta você pela criação de um manifesto do zero sem precisar usar marcas XML.</span><span class="sxs-lookup"><span data-stu-id="2e63f-137">The ECManGen.exe tool uses a GUI that guides you through creating a manifest from scratch without ever having to use XML tags.</span></span> <span data-ttu-id="2e63f-138">Ter conhecimento das informações nesta seção e na seção do [esquema EventManifest](eventmanifestschema-schema.md) ajudará ao usar a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="2e63f-138">Having knowledge of the information in this section and in the [EventManifest Schema](eventmanifestschema-schema.md) section will help when using the tool.</span></span>

<span data-ttu-id="2e63f-139">Se você usar o Visual Studio como seu editor de XML, poderá adicionar o esquema [EventManifest](eventmanifestschema-schema.md) ao projeto (consulte o menu XML) para aproveitar o IntelliSense, a validação de esquema embutido e outros recursos para tornar a criação do manifesto mais fácil e precisa.</span><span class="sxs-lookup"><span data-stu-id="2e63f-139">If you use Visual Studio as your XML editor, you can add the [EventManifest](eventmanifestschema-schema.md) schema to the project (see the XML menu) to take advantage of Intellisense, inline schema validation, and other features to make writing the manifest easy and accurate.</span></span>

<span data-ttu-id="2e63f-140">Depois de gravar o manifesto, use o compilador de mensagem para validar o manifesto e gerar os arquivos de recurso e de cabeçalho que você inclui em seu provedor.</span><span class="sxs-lookup"><span data-stu-id="2e63f-140">After writing your manifest, use the message compiler to validate the manifest and generate the resource and header files that you include in your provider.</span></span> <span data-ttu-id="2e63f-141">Para obter mais informações, consulte [Compilando um manifesto de instrumentação](compiling-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="2e63f-141">For more information, see [Compiling an Instrumentation Manifest](compiling-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="2e63f-142">O exemplo a seguir mostra o esqueleto de um manifesto de evento totalmente definido.</span><span class="sxs-lookup"><span data-stu-id="2e63f-142">The following example shows the skeleton of a fully defined event manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 