---
title: Definindo os Filtros
description: Um provedor pode definir filtros que uma sessão usa para filtrar eventos com base nos dados do evento.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dd2a21b9c4e01ebc4a32a160b24022c79197b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084827"
---
# <a name="defining-filters"></a><span data-ttu-id="c5b2a-103">Definindo os Filtros</span><span class="sxs-lookup"><span data-stu-id="c5b2a-103">Defining Filters</span></span>

<span data-ttu-id="c5b2a-104">Um provedor pode definir filtros que uma sessão usa para filtrar eventos com base nos dados do evento.</span><span class="sxs-lookup"><span data-stu-id="c5b2a-104">A provider can define filters that a session uses to filter events based on event data.</span></span> <span data-ttu-id="c5b2a-105">Com o nível e as palavras-chave, o ETW determina se o evento é gravado no log.</span><span class="sxs-lookup"><span data-stu-id="c5b2a-105">With level and keywords, ETW determines whether the event is written to the log.</span></span> <span data-ttu-id="c5b2a-106">No entanto, com filtros, o provedor usa os critérios de dados de filtro que a sessão de controle passa para ele (consulte a função [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) ) para determinar se ele grava o evento nessa sessão.</span><span class="sxs-lookup"><span data-stu-id="c5b2a-106">However, with filters, the provider uses the filter data criteria that the controlling session passes to it (see the [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) function) to determine whether it writes the event to that session.</span></span> <span data-ttu-id="c5b2a-107">Os filtros são aplicáveis somente quando uma sessão de rastreamento ETW habilita seu provedor.</span><span class="sxs-lookup"><span data-stu-id="c5b2a-107">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="c5b2a-108">Normalmente, os provedores apenas gravam eventos e a sessão identifica os tipos de eventos que ele deseja usando o nível e as palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="c5b2a-108">Typically, providers just write events, and the session identifies the types of events that it wants using level and keywords.</span></span> <span data-ttu-id="c5b2a-109">Se o provedor tiver definido um filtro de dados para um tipo de evento, a sessão poderá usá-lo para filtrar eventos para esse tipo de evento com base nos dados do evento (a semântica do filtro é definida pelo provedor).</span><span class="sxs-lookup"><span data-stu-id="c5b2a-109">If the provider defined a data filter for an event type, the session could use it to filter out events for that event type based on the event data (the semantics of the filter is defined by the provider).</span></span> <span data-ttu-id="c5b2a-110">Por exemplo, se seu provedor gerar eventos de processo, você poderá definir um filtro de dados que filtrou eventos de processo com base em um identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="c5b2a-110">For example, if your provider generates process events, you could define a data filter that filtered process events based on a process identifier.</span></span> <span data-ttu-id="c5b2a-111">Em seguida, a sessão pode passar um identificador de processo como filtrar dados para o provedor e receber apenas eventos de processo para esse identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="c5b2a-111">The session could then pass a process identifier as filter data to the provider and receive only process events for that process identifier.</span></span>

<span data-ttu-id="c5b2a-112">O exemplo a seguir mostra como usar o elemento **Filter** para definir um filtro.</span><span class="sxs-lookup"><span data-stu-id="c5b2a-112">The following example shows how to use the **filter** element to define a filter.</span></span> <span data-ttu-id="c5b2a-113">Você deve especificar os atributos de **nome** e **valor** do filtro; os outros atributos são opcionais.</span><span class="sxs-lookup"><span data-stu-id="c5b2a-113">You must specify the filter's **name** and **value** attributes; the other attributes are optional.</span></span> <span data-ttu-id="c5b2a-114">O atributo **tid** será necessário se o filtro exigir que a sessão passe dados de filtro.</span><span class="sxs-lookup"><span data-stu-id="c5b2a-114">The **tid** attribute is required if the filter requires that the session pass filter data.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <filters>
                    <filter name="Pid"
                            value="1"
                            tid="t1"
                            symbol="FILTER_PID"/>
                </filters>

                <templates>
                    <template tid="t1">
                        <data name="Pid" inType="win:UInt32"/>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```