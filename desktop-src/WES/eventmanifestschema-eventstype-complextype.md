---
title: Tipo complexo EventsType
description: Contém uma lista de provedores que são definidos no manifesto. | Tipo complexo EventsType
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- Tipo complexo EventsType EventLog
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d0cee50c0332d283c439448fd80c7abe319fec5065f39dcad4e053baf600bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055984"
---
# <a name="eventstype-complex-type"></a>Tipo complexo EventsType

Contém uma lista de provedores que são definidos no manifesto.

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho

| Elemento | Type | Descrição |
|---------|------|-------------|
| message |      | Define uma cadeia de caracteres de mensagem. |
| messageTable | | Define uma lista de cadeias de caracteres de mensagem. Você não deve ter que usar uma tabela de mensagens, exceto nos casos a seguir em que você deve definir uma tabela de mensagens para atribuir explicitamente números de recurso a cadeias de caracteres de mensagem. <ul><li>Você está migrando de um arquivo de texto de mensagem (.mc) para um manifesto, mas ainda está escrevendo eventos nos canais do aplicativo e do sistema, para que os consumidores herddos continuem consumindo os eventos. Para fazer isso funcionar, os identificadores de recurso para as cadeias de caracteres de mensagem definidas no manifesto devem ser os mesmos que os identificadores de evento. No entanto, o compilador de mensagem atribui automaticamente identificadores de recurso às cadeias de caracteres de mensagem. Para substituir o compilador, use a tabela de mensagens e de definido o atributo value como o identificador de evento e o atributo de mensagem para se referir a uma cadeia de caracteres na tabela de cadeia de caracteres na seção de localização do manifesto.</li><li>Se você quiser identificar mais de 16 provedores, deverá incluir a tabela de mensagens que os provedores e em devem usar para atribuir valores de recurso para as cadeias de caracteres de mensagem que eles definem. Se o provedor fizer referência a cadeias de caracteres de mensagem definidas pelos provedores de 1 a 16, você não incluirá essas cadeias de caracteres de mensagem na tabela de mensagens.</li></ul>|
| [**Provedor**](eventmanifestschema-provider-eventstype-element.md) | [**ProviderType**](eventmanifestschema-providertype-complextype.md) | Uma lista de provedores que você deseja definir. |

## <a name="attributes"></a>Atributos

| Nome    | Tipo                                                             | Descrição                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.                               |
| mid     | xs:string                                                        | Não usado.                                                                              |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O nome simbólico que você deseja que o compilador de mensagem crie para essa cadeia de caracteres de mensagem.|
| valor   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | O número a ser usado como o identificador de mensagem para esta mensagem.                          |


## <a name="remarks"></a>Comentários

O limite prático do número de provedores que você pode definir em um manifesto é de 16 provedores. Se você especificar mais de 16 provedores, deverá usar uma tabela de mensagens para atribuir explicitamente números de recursos às cadeias de caracteres de mensagem referenciadas pelo provedor. Para obter mais detalhes, consulte o elemento de mensagem acima.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------|
| Cliente mínimo com suporte | Windows Somente \[ aplicativos da área de trabalho do Vista\]       |
| Servidor mínimo com suporte | Windows Somente aplicativos da área de trabalho server 2008 \[\] |
