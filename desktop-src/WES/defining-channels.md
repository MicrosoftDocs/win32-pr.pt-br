---
title: Definindo canais
description: Os eventos podem ser gravados em canais de log de eventos, arquivos de log de rastreamento de eventos ou ambos. Um canal é basicamente um coletor que coleta eventos.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3c73697aa11e7b63ace0ece33be23ca7a1b883
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104084404"
---
# <a name="defining-channels"></a><span data-ttu-id="2a699-104">Definindo canais</span><span class="sxs-lookup"><span data-stu-id="2a699-104">Defining Channels</span></span>

<span data-ttu-id="2a699-105">Os eventos podem ser gravados em canais de log de eventos, arquivos de log de rastreamento de eventos ou ambos.</span><span class="sxs-lookup"><span data-stu-id="2a699-105">Events can be written to event log channels, event tracing log files, or both.</span></span> <span data-ttu-id="2a699-106">Um canal é basicamente um coletor que coleta eventos.</span><span class="sxs-lookup"><span data-stu-id="2a699-106">A channel is basically a sink that collects events.</span></span> <span data-ttu-id="2a699-107">Se o público-alvo de seus eventos usar consumidores de eventos como o Visualizador de Eventos do Windows, você deverá definir novos canais para coletar seus eventos ou importar um canal existente que outro provedor definiu.</span><span class="sxs-lookup"><span data-stu-id="2a699-107">If the target audience for your events uses event consumers such as the Windows Event Viewer, you must define new channels to collect your events or import an existing channel that another provider defined.</span></span>

<span data-ttu-id="2a699-108">Para definir seus próprios canais, use o elemento **Channel** .</span><span class="sxs-lookup"><span data-stu-id="2a699-108">To define your own channels, use the **channel** element.</span></span> <span data-ttu-id="2a699-109">Para definir um canal importado, use o elemento **importChannel** .</span><span class="sxs-lookup"><span data-stu-id="2a699-109">To define an imported channel, use the **importChannel** element.</span></span> <span data-ttu-id="2a699-110">Você pode especificar até oito canais em qualquer combinação de canais ou canais importados que você definir.</span><span class="sxs-lookup"><span data-stu-id="2a699-110">You can specify up to eight channels in any combination of imported channels or channels that you define.</span></span>

<span data-ttu-id="2a699-111">O canal deve ser de um dos quatro tipos: admin, operacional, analítica e depuração.</span><span class="sxs-lookup"><span data-stu-id="2a699-111">The channel must be of one of four types: Admin, Operational, Analytic, and Debug.</span></span> <span data-ttu-id="2a699-112">Cada tipo de canal tem um público-alvo, que determina o tipo de eventos que você grava no canal.</span><span class="sxs-lookup"><span data-stu-id="2a699-112">Each channel type has an intended audience, which determines the type of events that you write to the channel.</span></span> <span data-ttu-id="2a699-113">Para obter uma descrição de cada tipo, consulte o tipo complexo [**channelType**](eventmanifestschema-channeltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2a699-113">For a description of each type, see the [**ChannelType**](eventmanifestschema-channeltype-complextype.md) complex type.</span></span>

<span data-ttu-id="2a699-114">Para especificar o canal no qual um evento é gravado, defina o atributo de **canal** da definição de evento para o mesmo valor que o atributo **chid** da definição de canal.</span><span class="sxs-lookup"><span data-stu-id="2a699-114">To specify the channel to which an event is written, set the event definition's **channel** attribute to the same value as the channel definition's **chid** attribute.</span></span> <span data-ttu-id="2a699-115">Os eventos só podem ser gravados em um canal por vez, mas também podem ser coletados por até 7 outras sessões de ETW ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="2a699-115">Events can only be written to one channel at a time, but can also be collected by up to 7 other ETW sessions at the same time.</span></span>

<span data-ttu-id="2a699-116">O exemplo a seguir mostra como importar um canal.</span><span class="sxs-lookup"><span data-stu-id="2a699-116">The following example shows how to import a channel.</span></span> <span data-ttu-id="2a699-117">Você deve definir os atributos **chid** e **Name** .</span><span class="sxs-lookup"><span data-stu-id="2a699-117">You must set the **chid** and **name** attributes.</span></span> <span data-ttu-id="2a699-118">O atributo **chid** identifica exclusivamente o canal — cada identificador de canal na lista de canais deve ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2a699-118">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="2a699-119">Defina o atributo **Name** para o mesmo nome que o provedor usou quando ele definiu o canal.</span><span class="sxs-lookup"><span data-stu-id="2a699-119">Set the **name** attribute to the same name that the provider used when it defined the channel.</span></span>


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

                <channels>
                    <channel chid="c1"
                             name="Microsoft-Windows-BaseProvider/Admin"
                             symbol="CHANNEL_BASEPROVIDER_ADMIN"
                             type="Admin"/>
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

<span data-ttu-id="2a699-120">Embora Winmeta.xml defina os canais herdados que você pode importar, você não deve usá-los, a menos que esteja dando suporte a consumidores herdados que consomem eventos dos canais herdados (por exemplo, aplicativo ou sistema).</span><span class="sxs-lookup"><span data-stu-id="2a699-120">Although Winmeta.xml defines legacy channels that you can import, you should not use them unless you are supporting legacy consumers that consume events out of the legacy channels (for example, Application or System).</span></span> <span data-ttu-id="2a699-121">O arquivo de Winmeta.xml está incluído no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="2a699-121">The Winmeta.xml file is included in the Windows SDK.</span></span>

<span data-ttu-id="2a699-122">O exemplo a seguir mostra como definir um canal.</span><span class="sxs-lookup"><span data-stu-id="2a699-122">The following example shows how to define a channel.</span></span> <span data-ttu-id="2a699-123">Você deve definir os atributos **chid**, **Name** e **Type** .</span><span class="sxs-lookup"><span data-stu-id="2a699-123">You must set the **chid**, **name**, and **type** attributes.</span></span> <span data-ttu-id="2a699-124">O atributo **chid** identifica exclusivamente o canal — cada identificador de canal na lista de canais deve ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2a699-124">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="2a699-125">Defina o atributo **chid** para um valor que seja exclusivo para os canais que seu provedor lista; o identificador do canal é referenciado em uma ou mais das suas definições de evento.</span><span class="sxs-lookup"><span data-stu-id="2a699-125">Set the **chid** attribute to a value that is unique for the channels that your provider lists; the channel identifier is referenced in one or more of your event definitions.</span></span> <span data-ttu-id="2a699-126">A Convenção para nomear o canal é usar o nome do provedor e o tipo de canal no formulário, *ProviderName* / *channelType*.</span><span class="sxs-lookup"><span data-stu-id="2a699-126">The convention for naming the channel is to use the provider name and channel type in the form, *providername*/*channeltype*.</span></span>

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

                <channels>
                    <importChannel chid="c1"
                                   name="Microsoft-Windows-BaseProvider/Admin"
                                   symbol="CHANNEL_BASEPROVIDER_ADMIN"
                                   />

                    <channel chid="c2"
                             name="Microsoft-Windows-SampleProvider/Operational"
                             type="Operational"
                             enabled="true"
                             />
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
