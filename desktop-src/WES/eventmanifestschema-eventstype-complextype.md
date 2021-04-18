---
title: Tipo complexo EventType
description: Contém uma lista de provedores que são definidos no manifesto. | Tipo complexo EventType
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- EventLog tipo complexo de EventType
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105788821"
---
# <a name="eventstype-complex-type"></a>Tipo complexo EventType

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
| mensagem de | | Define uma lista de cadeias de caracteres de mensagem. Você não deve ter que usar uma tabela de mensagens, exceto nos casos a seguir, em que você deve definir uma tabela de mensagens para atribuir explicitamente números de recursos a cadeias de caracteres de mensagem. <ul><li>Você está migrando de um arquivo de texto de mensagem (. MC) para um manifesto, mas ainda está gravando eventos para os canais do aplicativo e do sistema, para que os consumidores herdados continuem consumindo os eventos. Para fazer isso funcionar, os identificadores de recurso para as cadeias de caracteres de mensagem definidos no manifesto devem ser iguais aos identificadores de evento. No entanto, o compilador de mensagem atribui automaticamente identificadores de recurso às cadeias de caracteres de mensagem. Para substituir o compilador, use a tabela Message e defina o atributo Value para o identificador de evento e o atributo Message para se referir a uma cadeia de caracteres na tabela de cadeia de caracteres na seção localização do manifesto.</li><li>Se você quiser identificar mais de 16 provedores, deverá incluir a tabela de mensagens que os provedores seventeenth e on devem usar para atribuir valores de recursos para as cadeias de caracteres de mensagem que eles definem. Se o provedor fizer referência a cadeias de caracteres de mensagem que os provedores de 1 a 16 definidos, você não incluirá essas cadeias de caracteres de mensagem na tabela de mensagens.</li></ul>|
| [**operador**](eventmanifestschema-provider-eventstype-element.md) | [**ProviderType**](eventmanifestschema-providertype-complextype.md) | Uma lista de provedores que você deseja definir. |

## <a name="attributes"></a>Atributos

| Nome    | Tipo                                                             | Descrição                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.                               |
| mid     | xs:string                                                        | Não usado.                                                                              |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O nome simbólico que você deseja que o compilador de mensagem crie para essa cadeia de caracteres de mensagem.|
| value   | [**UInt32type**](eventmanifestschema-hexint32type-simpletype.md) | O número a ser usado como o identificador da mensagem para esta mensagem.                          |


## <a name="remarks"></a>Comentários

O limite prático do número de provedores que você pode definir em um manifesto é de 16 provedores. Se você especificar mais de 16 provedores, deverá usar uma tabela de mensagens para atribuir explicitamente números de recursos às cadeias de caracteres de mensagens que o provedor referencia. Para obter mais detalhes, consulte o elemento Message acima.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------|
| Cliente mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Vista\]       |
| Servidor mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Server 2008\] |
