---
title: Elemento instrumentationManifest
description: O nó raiz do manifesto.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- EventLog do elemento instrumentationManifest
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c15092d7a7eafd625e9c2026965af053d38fe4b9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104172575"
---
# <a name="instrumentationmanifest-element"></a>Elemento instrumentationManifest

O nó raiz do manifesto.

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                        | Type                                                                               | Descrição                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Instrumentação**](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [**InstrumentationType**](eventmanifestschema-instrumentationtype-complextype.md) | Esta seção define um ou mais provedores de eventos e os eventos que eles registram.<br/>                                                                                                                                                                                                                     |
| [**Localizar**](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [**Localizaçãotype**](eventmanifestschema-localizationtype-complextype.md)       | Esta seção define as cadeias de caracteres de mensagem localizadas que os consumidores usam para exibição. Por exemplo, esta seção conteria a cadeia de caracteres de mensagem localizada para o nome do seu provedor, os eventos que você definir e quaisquer atributos de evento que você definir, como canais, tarefas e OpCodes.<br/> |
| [**los**](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)               | Esta seção define os tipos de metadados que outros manifestos podem usar. Para obter um exemplo, consulte o arquivo Winmeta.xml incluído na \\ pasta include do SDK do Windows.<br/>                                                                                                                                    |



## <a name="remarks"></a>Comentários

O elemento **instrumentationManifest** deve conter os seguintes namespaces:

<dl> xmlns = " https://schemas.microsoft.com/win/2004/08/events "  
xmlns: Win = " https://manifests.microsoft.com/win/2004/08/windows/events "  
xmlns: XS = " https://www.w3.org/2001/XMLSchema "  
</dl>

Um manifesto deve conter uma seção de instrumentação e uma seção de localização. A seção de instrumentação e a seção de metadados são mutuamente exclusivas (você não pode definir ambos no mesmo manifesto). Embora você possa criar um manifesto que contenha uma seção de metadados, o serviço não o usará; os únicos metadados que o serviço reconhece são os metadados encontrados no arquivo de Winmeta.xml.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o esqueleto de um manifesto de instrumentação totalmente definido.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





