---
title: Identificando o provedor
description: Um manifesto pode identificar um ou mais provedores. Para identificar um provedor, use o elemento Provider.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45941a540f8804beccc408435fc202593ddad601
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104499006"
---
# <a name="identifying-the-provider"></a>Identificando o provedor

Um manifesto pode identificar um ou mais provedores. Para identificar um provedor, use o elemento **Provider** . Você deve especificar os atributos **Name**, **GUID**, **resourceFileName**, **messageFileName** e **Symbol** . Se você localizar o manifesto, também deverá especificar o atributo **Message** , que os consumidores usam como exibir o nome do provedor. Se você não especificar o atributo **Message** , os consumidores usarão o valor do atributo **Name** .

Você pode identificar até 16 provedores no manifesto. Se você quiser identificar mais de 16 provedores, deverá incluir a seção **messagetable** do manifesto que os provedores seventeenth e on devem usar para atribuir valores de recursos para as cadeias de caracteres de mensagem que eles definem — a tabela de mensagens não deve incluir nenhuma cadeia de caracteres de mensagem que os provedores de 1 a 16 definidos.

O exemplo a seguir mostra como usar o elemento **Provider** para identificar um provedor.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
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
