---
title: Definindo níveis de severidade
description: Os níveis são usados para agrupar eventos e normalmente indicam a severidade ou o detalhamento de um evento.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8e2e979e75057a77cca267e540b3ec5469562f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104365784"
---
# <a name="defining-severity-levels"></a><span data-ttu-id="7999a-103">Definindo níveis de severidade</span><span class="sxs-lookup"><span data-stu-id="7999a-103">Defining Severity Levels</span></span>

<span data-ttu-id="7999a-104">Os níveis são usados para agrupar eventos e normalmente indicam a severidade ou o detalhamento de um evento.</span><span class="sxs-lookup"><span data-stu-id="7999a-104">Levels are used to group events and typically indicate the severity or verbosity of an event.</span></span> <span data-ttu-id="7999a-105">Para definir um nível, use o elemento **Level** .</span><span class="sxs-lookup"><span data-stu-id="7999a-105">To define a level, use the **level** element.</span></span> <span data-ttu-id="7999a-106">O arquivo de Winmeta.xml define os seguintes níveis de severidade usados com frequência:</span><span class="sxs-lookup"><span data-stu-id="7999a-106">The Winmeta.xml file defines the following commonly used severity levels:</span></span>

-   <span data-ttu-id="7999a-107">win:Critical</span><span class="sxs-lookup"><span data-stu-id="7999a-107">win:Critical</span></span>
-   <span data-ttu-id="7999a-108">win:Error</span><span class="sxs-lookup"><span data-stu-id="7999a-108">win:Error</span></span>
-   <span data-ttu-id="7999a-109">win:Warning</span><span class="sxs-lookup"><span data-stu-id="7999a-109">win:Warning</span></span>
-   <span data-ttu-id="7999a-110">win:Informational</span><span class="sxs-lookup"><span data-stu-id="7999a-110">win:Informational</span></span>
-   <span data-ttu-id="7999a-111">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="7999a-111">win:Verbose</span></span>

<span data-ttu-id="7999a-112">Os consumidores usam níveis para consultar eventos que contêm um valor de nível específico.</span><span class="sxs-lookup"><span data-stu-id="7999a-112">Consumers use levels to query for events that contain a specific level value.</span></span> <span data-ttu-id="7999a-113">Uma sessão de rastreamento ETW também pode usar níveis para limitar os eventos que são gravados no arquivo de log de rastreamento de eventos; eventos com um valor de nível igual ou menor que o valor de nível especificado são gravados no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="7999a-113">An ETW tracing session can also use levels to limit the events that are written to the event tracing log file; events with a level value equal to or less than the specified level value are written to the log file.</span></span> <span data-ttu-id="7999a-114">Por exemplo, se a sessão especificar o valor de nível para win: Warning, o arquivo de log conterá eventos de aviso, de erro e críticos.</span><span class="sxs-lookup"><span data-stu-id="7999a-114">For example, if the session specified the level value for win:Warning, the log file would contain warning, error, and critical events.</span></span>

<span data-ttu-id="7999a-115">O exemplo a seguir mostra como definir um nível.</span><span class="sxs-lookup"><span data-stu-id="7999a-115">The following example shows how to define a level.</span></span> <span data-ttu-id="7999a-116">Você deve especificar os atributos de **nome** e **valor** do nível.</span><span class="sxs-lookup"><span data-stu-id="7999a-116">You must specify the level's **name** and **value** attributes.</span></span> <span data-ttu-id="7999a-117">O valor do atributo de **valor** deve estar no intervalo de 16 a 255.</span><span class="sxs-lookup"><span data-stu-id="7999a-117">The value of the **value** attribute must be in the range from 16 through 255.</span></span> <span data-ttu-id="7999a-118">Os atributos de **símbolo** e **mensagem** são opcionais.</span><span class="sxs-lookup"><span data-stu-id="7999a-118">The **symbol** and **message** attributes are optional.</span></span>


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

                <levels>
                    <level name="NotValid"
                           value="16"
                           symbol="LEVEL_SAMPLEPROVIDER_NOTVALID"
                           message="$(string.Level.NotValid)"/>
                    <level name="Valid"
                           value="17"
                           symbol="LEVEL_SAMPLEPROVIDER_VALID"
                           message="$(string.Level.Valid)"/>
                </levels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Level.Valid" value="Valid"/>
                <string id="Level.NotValid" value="Not Valid"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
