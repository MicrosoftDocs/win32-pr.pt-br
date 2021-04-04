---
title: Definindo palavras-chave usadas para classificar tipos de eventos
description: Os provedores usam palavras-chave para classificar diferentes tipos de eventos.
ms.assetid: 1cbad719-bc59-4255-8a15-9e45f363d199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48992c5cbafec5f945fa2f133924ccf0e2e7e96
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "103823607"
---
# <a name="defining-keywords-used-to-classify-types-of-events"></a>Definindo palavras-chave usadas para classificar tipos de eventos

Os provedores usam palavras-chave para classificar diferentes tipos de eventos. Por exemplo, você pode criar uma palavra-chave para todos os eventos de leitura e, em seguida, aplicar a palavra-chave Read a qualquer evento que executa uma operação de leitura, como a leitura de um arquivo ou registro. Os consumidores poderiam, então, usar os valores de bit da palavra-chave para filtrar a classificação de eventos diferente. Por exemplo, o consumidor pode solicitar todos os eventos de leitura ou todos os eventos de leitura da tarefa X (se você também agrupar eventos por tarefa). Para definir uma palavra-chave, use o elemento **keyword** .

Uma sessão de rastreamento ETW pode usar as palavras-chave (da mesma forma que usa nível) para limitar os eventos que o serviço ETW grava em seu arquivo de log de rastreamento de eventos. Uma sessão de rastreamento pode habilitar o provedor usando dois conjuntos de bitmasks de palavra-chave: um bitmask "any" em que o evento é gravado se qualquer um dos bits de palavra-chave do evento corresponder a qualquer um dos bits definidos nessa máscara e um bitmask "All", em que para os eventos que corresponderam ao caso de "any", o evento será gravado somente se todos os bits na máscara "All" existirem no bitmask da palavra-chave do evento.

Por exemplo, se o provedor definir um evento que especifica uma palavra-chave Read (bit 0) e uma palavra-chave de acesso local (bit 1), e um segundo evento que especifica uma palavra-chave Read (bit 0) e uma palavra-chave Remote Access (bit 2), você pode definir o bitmask "any" como 1 para receber todos os eventos de leitura ou pode definir o bitmask "any" como 1 e "All" bitmask como 3 para receber somente leituras locais.

Você deve especificar o **nome** da palavra-chave e os atributos de **máscara** . A máscara deve definir apenas um bit, entre o bit 0 e o bit 47. Bits 48 a 64 são reservados.

Os atributos de **símbolo** e **mensagem** são opcionais.

O exemplo a seguir mostra como definir uma palavra-chave.

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

                <keywords>
                    <keyword name="Read" mask="0x1" symbol="READ_KEYWORD"/>
                    <keyword name="Write" mask="0x2" symbol="WRITE_KEYWORD"/>
                    <keyword name="Local" mask="0x4" symbol="LOCAL_KEYWORD"/>
                    <keyword name="Remote" mask="0x8" symbol="REMOTE_KEYWORD"/>
                </keywords>

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
