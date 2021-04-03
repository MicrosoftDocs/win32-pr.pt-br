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
# <a name="defining-filters"></a>Definindo os Filtros

Um provedor pode definir filtros que uma sessão usa para filtrar eventos com base nos dados do evento. Com o nível e as palavras-chave, o ETW determina se o evento é gravado no log. No entanto, com filtros, o provedor usa os critérios de dados de filtro que a sessão de controle passa para ele (consulte a função [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) ) para determinar se ele grava o evento nessa sessão. Os filtros são aplicáveis somente quando uma sessão de rastreamento ETW habilita seu provedor.

Normalmente, os provedores apenas gravam eventos e a sessão identifica os tipos de eventos que ele deseja usando o nível e as palavras-chave. Se o provedor tiver definido um filtro de dados para um tipo de evento, a sessão poderá usá-lo para filtrar eventos para esse tipo de evento com base nos dados do evento (a semântica do filtro é definida pelo provedor). Por exemplo, se seu provedor gerar eventos de processo, você poderá definir um filtro de dados que filtrou eventos de processo com base em um identificador de processo. Em seguida, a sessão pode passar um identificador de processo como filtrar dados para o provedor e receber apenas eventos de processo para esse identificador de processo.

O exemplo a seguir mostra como usar o elemento **Filter** para definir um filtro. Você deve especificar os atributos de **nome** e **valor** do filtro; os outros atributos são opcionais. O atributo **tid** será necessário se o filtro exigir que a sessão passe dados de filtro.


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