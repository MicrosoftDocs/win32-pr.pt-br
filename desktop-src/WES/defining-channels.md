---
title: Definindo canais
description: Os eventos podem ser gravados em canais de log de eventos, arquivos de log de rastreamento de eventos ou ambos. Um canal é basicamente um sink que coleta eventos.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c2f932616a131e478c100996fd0b76034b3cccdebf4e3714fd5b9b38ba9678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032476"
---
# <a name="defining-channels"></a>Definindo canais

Os eventos podem ser gravados em canais de log de eventos, arquivos de log de rastreamento de eventos ou ambos. Um canal é basicamente um sink que coleta eventos. Se o público-alvo de seus eventos usar consumidores de eventos como o Windows Visualizador de Eventos, você deverá definir novos canais para coletar seus eventos ou importar um canal existente definido por outro provedor.

Para definir seus próprios canais, use o **elemento channel.** Para definir um canal importado, use o **elemento importChannel.** Você pode especificar até oito canais em qualquer combinação de canais importados ou canais que você definir.

O canal deve ser de um dos quatro tipos: Admin, Operational, Analytic e Debug. Cada tipo de canal tem um público-alvo pretendido, que determina o tipo de eventos que você escreve no canal. Para ver uma descrição de cada tipo, consulte o [**tipo complexo ChannelType.**](eventmanifestschema-channeltype-complextype.md)

Para especificar o canal no qual um evento é  gravado, defina o atributo de canal da definição de evento com o mesmo valor que o atributo **chid da** definição de canal. Os eventos só podem ser gravados em um canal por vez, mas também podem ser coletados por até 7 outras sessões ETW ao mesmo tempo.

O exemplo a seguir mostra como importar um canal. Você deve definir os **atributos chid** **e name.** O **atributo chid** identifica exclusivamente o canal – cada identificador de canal em sua lista de canais deve ser exclusivo. De definir **o** atributo name com o mesmo nome que o provedor usou quando definiu o canal.


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

Embora Winmeta.xml defina canais herdado que você pode importar, você não deve usá-los, a menos que esteja dando suporte a consumidores herdado que consomem eventos fora dos canais herdado (por exemplo, Aplicativo ou Sistema). O Winmeta.xml arquivo está incluído no SDK do Windows.

O exemplo a seguir mostra como definir um canal. Você deve definir os **atributos chid**, **name** e **type.** O **atributo chid** identifica exclusivamente o canal – cada identificador de canal em sua lista de canais deve ser exclusivo. De definir **o atributo chid** como um valor exclusivo para os canais que seu provedor lista; o identificador de canal é referenciado em uma ou mais de suas definições de evento. A convenção para nomear o canal é usar o nome do provedor e o tipo de canal no formulário, *providername* / *channeltype*.

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
