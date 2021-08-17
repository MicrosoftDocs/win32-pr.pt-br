---
title: Tipo complexo OpcodeType
description: Define uma operação dentro de um componente do aplicativo.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- Tipo complexo OpcodeType EventLog
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b18fa8a7591a54877251e10448842c3cd9d2394099028bf3a2cb680aee979bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136209"
---
# <a name="opcodetype-complex-type"></a>Tipo complexo OpcodeType

Define uma operação dentro de um componente do aplicativo. Usado em conjunto com uma tarefa para identificar a seção do aplicativo que está registrando o evento em log.

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="mofValue"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nome     | Tipo                                                              | Descrição                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message  | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | O nome de exibição localizado para o opcode. A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**stringTable**](eventmanifestschema-stringtable-resources-element.md) do manifesto. <br/>                                                                                                     |
| mofValue | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Reservado apenas para uso interno.<br/>                                                                                                                                                                                                                                                                           |
| name     | **QName**                                                         | O nome do opcode. Esse nome deve ser exclusivo dentro do escopo desse provedor. <br/>                                                                                                                                                                                                                      |
| símbolo   | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para referenciar o opcode em seu aplicativo. O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o opcode no arquivo de header que o compilador gera. Se você não especificar um símbolo, o compilador gerará um para você.<br/> |
| valor    | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | O valor opcode. Você pode especificar valores nos intervalos 10 e 239. Para ver uma lista de valores de opcode predefinidos, consulte Comentários.<br/>                                                                                                                                                                                    |



## <a name="remarks"></a>Comentários

A seguir estão os valores de opcode predefinidos que você pode usar. Esses valores são definidos no arquivo Winmeta.xml que está incluído no SDK do Windows.



| Nome          | Valor | Símbolo                      | Descrição                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| win:Info      | 0     | INFORMAÇÕES SOBRE \_ O WINEVENT OPCODE \_      | Um evento informativo.                                                                                |
| win:Start     | 1     | INÍCIO DO \_ WINEVENT OPCODE \_     | Um evento que representa o início de uma atividade.                                                         |
| win:Stop      | 2     | WINEVENT \_ OPCODE \_ STOP      | Um evento que representa a interrupção de uma atividade. O evento corresponde ao último evento de início não organizado. |
| Win:DC \_ Start | 3     | INÍCIO DE \_ DC DO WINEVENT OPCODE \_ \_ | Um evento que representa a coleta de dados começando. Esses são tipos de evento de rundown.                      |
| win:DC \_ Stop  | 4     | WINEVENT \_ OPCODE \_ DC \_ STOP  | Um evento que representa a interrupção da coleta de dados. Esses são tipos de evento de rundown.                      |
| win:Extension | 5     | EXTENSÃO \_ WINEVENT OPCODE \_ | Um evento de extensão.                                                                                    |
| win:Reply     | 6     | RESPOSTA DO \_ WINEVENT \_ OPCODE     | Um evento de resposta.                                                                                         |
| win:Resume    | 7     | WINEVENT \_ OPCODE \_ RESUME    | Um evento que representa uma atividade que é retomada após ser suspensa.                                   |
| win:Suspend   | 8     | WINEVENT \_ OPCODE \_ SUSPEND   | Um evento que representa a atividade que está sendo suspensa aguardando a conclusão de outra atividade.           |
| win:Send      | 9     | ENVIO DO \_ WINEVENT OPCODE \_      | Um evento que representa a transferência de atividade para outro componente.                                   |
| win:Receive   | 240   | RECEBIMENTO DE \_ OPCODE DO \_ WINEVENT   | Um evento que representa o recebimento de uma transferência de atividade de outro componente.                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





