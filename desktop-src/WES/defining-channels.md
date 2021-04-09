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
# <a name="defining-channels"></a>Definindo canais

Os eventos podem ser gravados em canais de log de eventos, arquivos de log de rastreamento de eventos ou ambos. Um canal é basicamente um coletor que coleta eventos. Se o público-alvo de seus eventos usar consumidores de eventos como o Visualizador de Eventos do Windows, você deverá definir novos canais para coletar seus eventos ou importar um canal existente que outro provedor definiu.

Para definir seus próprios canais, use o elemento **Channel** . Para definir um canal importado, use o elemento **importChannel** . Você pode especificar até oito canais em qualquer combinação de canais ou canais importados que você definir.

O canal deve ser de um dos quatro tipos: admin, operacional, analítica e depuração. Cada tipo de canal tem um público-alvo, que determina o tipo de eventos que você grava no canal. Para obter uma descrição de cada tipo, consulte o tipo complexo [**channelType**](eventmanifestschema-channeltype-complextype.md) .

Para especificar o canal no qual um evento é gravado, defina o atributo de **canal** da definição de evento para o mesmo valor que o atributo **chid** da definição de canal. Os eventos só podem ser gravados em um canal por vez, mas também podem ser coletados por até 7 outras sessões de ETW ao mesmo tempo.

O exemplo a seguir mostra como importar um canal. Você deve definir os atributos **chid** e **Name** . O atributo **chid** identifica exclusivamente o canal — cada identificador de canal na lista de canais deve ser exclusivo. Defina o atributo **Name** para o mesmo nome que o provedor usou quando ele definiu o canal.


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

Embora Winmeta.xml defina os canais herdados que você pode importar, você não deve usá-los, a menos que esteja dando suporte a consumidores herdados que consomem eventos dos canais herdados (por exemplo, aplicativo ou sistema). O arquivo de Winmeta.xml está incluído no SDK do Windows.

O exemplo a seguir mostra como definir um canal. Você deve definir os atributos **chid**, **Name** e **Type** . O atributo **chid** identifica exclusivamente o canal — cada identificador de canal na lista de canais deve ser exclusivo. Defina o atributo **chid** para um valor que seja exclusivo para os canais que seu provedor lista; o identificador do canal é referenciado em uma ou mais das suas definições de evento. A Convenção para nomear o canal é usar o nome do provedor e o tipo de canal no formulário, *ProviderName* / *channelType*.

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
