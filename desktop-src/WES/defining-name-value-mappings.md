---
title: Definindo mapeamentos de nome/valor
description: Um provedor pode definir uma lista de pares de nome/valor que os consumidores usam para mapear valores inteiros para cadeias de caracteres.
ms.assetid: d16b2410-a0de-42da-8f2a-98341c90ed87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62020adeb46bac96cada70cf5830e17213d69868
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104365785"
---
# <a name="defining-namevalue-mappings"></a><span data-ttu-id="661b3-103">Definindo mapeamentos de nome/valor</span><span class="sxs-lookup"><span data-stu-id="661b3-103">Defining Name/Value Mappings</span></span>

<span data-ttu-id="661b3-104">Um provedor pode definir uma lista de pares de nome/valor que os consumidores usam para mapear valores inteiros para cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="661b3-104">A provider can define a list of name/value pairs that consumers use to map integer values to strings.</span></span> <span data-ttu-id="661b3-105">Os pares de nome/valor podem mapear valores inteiros para cadeias de caracteres ou valores de bits de valores de bits para cadeias de caracteres; cada valor corresponde a um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="661b3-105">The name/value pairs can map integer values to strings or bit values bit values to strings; each value corresponds to a string value.</span></span> <span data-ttu-id="661b3-106">Use mapeamentos em itens de dados inteiros que contenham valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="661b3-106">Use mappings on integer data items that contain enumeration values.</span></span>

<span data-ttu-id="661b3-107">Os consumidores podem usar o mapa de valores para recuperar a cadeia de caracteres associada a um valor e exibi-la em vez de exibir o valor inteiro ou de bits.</span><span class="sxs-lookup"><span data-stu-id="661b3-107">Consumers can use the value map to retrieve the string associated with a value and display it instead of displaying the integer or bit value.</span></span> <span data-ttu-id="661b3-108">Para definir um mapa de valor inteiro, use os elementos **valueMap** e **MAP** .</span><span class="sxs-lookup"><span data-stu-id="661b3-108">To define an integer value map, use the **valueMap** and **map** elements.</span></span> <span data-ttu-id="661b3-109">Para definir um mapa de valor de bit, use os elementos **bitmap** e **MAP** .</span><span class="sxs-lookup"><span data-stu-id="661b3-109">To define a bit value map, use the **bitmap** and **map** elements.</span></span>

<span data-ttu-id="661b3-110">O exemplo a seguir mostra como definir um mapa de valor e um bitmap.</span><span class="sxs-lookup"><span data-stu-id="661b3-110">The following example shows how to define a value map and a bitmap.</span></span> <span data-ttu-id="661b3-111">Você deve especificar o atributo **Name** do mapa.</span><span class="sxs-lookup"><span data-stu-id="661b3-111">You must specify the map's **name** attribute.</span></span> <span data-ttu-id="661b3-112">Para cada par de nome/valor, você deve especificar o **valor** e o atributo de **mensagem** .</span><span class="sxs-lookup"><span data-stu-id="661b3-112">For each name/value pair, you must specify the **value** and **message** attribute.</span></span>


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

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
