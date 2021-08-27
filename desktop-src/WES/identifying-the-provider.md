---
title: Identificando o provedor
description: Um manifesto pode identificar um ou mais provedores. Para identificar um provedor, use o elemento provider.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ae37b20ea37d7e67d97846d9e9338e36d52f94
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812663"
---
# <a name="identifying-the-provider"></a>Identificando o provedor

Um manifesto pode identificar um ou mais provedores. Para identificar um provedor, use o **elemento provider.** Você deve especificar o **nome**, **guid**, **resourceFileName,** **messageFileName** e atributos **de** símbolo. Se você localizar o manifesto, também deverá especificar o atributo **de** mensagem, que os consumidores usam como a exibição do nome do provedor. Se você não especificar o atributo **de mensagem,** os consumidores usarão o valor do **atributo name.**

Você pode identificar até 16 provedores no manifesto. Se você quiser identificar mais de 16 provedores, deverá incluir a seção **messageTable** do manifesto que os provedores de 1 a 16 devem usar para atribuir valores de recurso para as cadeias de caracteres de mensagem que eles definem. A tabela de mensagens não deve incluir nenhuma cadeia de caracteres de mensagem definida pelos provedores de 1 a 16.

O exemplo a seguir mostra como usar o elemento **provider** para identificar um provedor.


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
