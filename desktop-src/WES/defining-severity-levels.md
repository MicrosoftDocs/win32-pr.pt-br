---
title: Definindo níveis de severidade
description: Os níveis são usados para agrupar eventos e normalmente indicam a severidade ou o detalhamento de um evento.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3c3c5e663e476f98bef5c9be3f20cae5e0e88a74a7996f6f515d1d92599eb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863676"
---
# <a name="defining-severity-levels"></a>Definindo níveis de severidade

Os níveis são usados para agrupar eventos e normalmente indicam a severidade ou o detalhamento de um evento. Para definir um nível, use o elemento **Level** . O arquivo de Winmeta.xml define os seguintes níveis de severidade usados com frequência:

-   win:Critical
-   win:Error
-   win:Warning
-   win:Informational
-   win:Verbose

Os consumidores usam níveis para consultar eventos que contêm um valor de nível específico. Uma sessão de rastreamento ETW também pode usar níveis para limitar os eventos que são gravados no arquivo de log de rastreamento de eventos; eventos com um valor de nível igual ou menor que o valor de nível especificado são gravados no arquivo de log. Por exemplo, se a sessão especificar o valor de nível para win: Warning, o arquivo de log conterá eventos de aviso, de erro e críticos.

O exemplo a seguir mostra como definir um nível. Você deve especificar os atributos de **nome** e **valor** do nível. O valor do atributo de **valor** deve estar no intervalo de 16 a 255. Os atributos de **símbolo** e **mensagem** são opcionais.


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
