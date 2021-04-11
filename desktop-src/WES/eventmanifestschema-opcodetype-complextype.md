---
title: Tipo complexo de OpCodeType
description: Define uma operação dentro de um componente do aplicativo.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- Código de log de tipo complexo OpCodeType
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086337"
---
# <a name="opcodetype-complex-type"></a>Tipo complexo de OpCodeType

Define uma operação dentro de um componente do aplicativo. Usado em conjunto com uma tarefa para identificar a seção do aplicativo que está registrando o evento.

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
| message  | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | O nome de exibição localizado para o opcode. A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto. <br/>                                                                                                     |
| mofValue | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Reservado apenas para uso interno.<br/>                                                                                                                                                                                                                                                                           |
| name     | **QName**                                                         | O nome do opcode. Esse nome deve ser exclusivo dentro do escopo deste provedor. <br/>                                                                                                                                                                                                                      |
| símbolo   | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para referenciar o opcode em seu aplicativo. O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o opcode no arquivo de cabeçalho que o compilador gera. Se você não especificar um símbolo, o compilador gerará um para você.<br/> |
| value    | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | O valor de opcode. Você pode especificar valores no intervalo de 10 a 239. Para obter uma lista de valores de opcode predefinidos, consulte comentários.<br/>                                                                                                                                                                                    |



## <a name="remarks"></a>Comentários

A seguir estão os valores de opcode predefinidos que você pode usar. Esses valores são definidos no arquivo de Winmeta.xml que está incluído no SDK do Windows.



| Nome          | Valor | Símbolo                      | Descrição                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| Win: info      | 0     | \_informações de opcode WINEVENT \_      | Um evento informativo.                                                                                |
| Win: iniciar     | 1     | \_início do opcode WINEVENT \_     | Um evento que representa o início de uma atividade.                                                         |
| Win: parar      | 2     | \_parada de opcode WINEVENT \_      | Um evento que representa a interrupção de uma atividade. O evento corresponde ao último evento de início não emparelhado. |
| Win: \_ Iniciar DC | 3     | inicialização do WINEVENT \_ opcode \_ DC \_ | Um evento que representa a coleta de dados iniciando. Esses são tipos de evento de encerramento.                      |
| Win: parada de DC \_  | 4     | WINEVENT \_ opcode \_ DC \_ Stop  | Um evento que representa a interrupção da coleta de dados. Esses são tipos de evento de encerramento.                      |
| Win: extensão | 5     | \_extensão de opcode WINEVENT \_ | Um evento de extensão.                                                                                    |
| Win: responder     | 6     | \_resposta de opcode WINEVENT \_     | Um evento de resposta.                                                                                         |
| Win: retomar    | 7     | \_currículo de opcode WINEVENT \_    | Um evento que representa uma atividade retomada após ser suspensa.                                   |
| Win: suspender   | 8     | \_suspensão de opcode WINEVENT \_   | Um evento que representa a atividade que está sendo suspensa pendente da conclusão de outra atividade.           |
| Win: enviar      | 9     | \_envio de opcode WINEVENT \_      | Um evento que representa a atividade de transferência para outro componente.                                   |
| Win: receber   | 240   | \_recebimento de opcode WINEVENT \_   | Um evento que representa o recebimento de uma transferência de atividade de outro componente.                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





