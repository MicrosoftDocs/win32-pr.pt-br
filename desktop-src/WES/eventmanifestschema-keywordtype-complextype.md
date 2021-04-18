---
title: Tipo complexo keywordtype
description: Define uma palavra-chave que identifica uma categoria de eventos. | Tipo complexo keywordtype
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- EventLog de tipo complexo de keywordtype
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105759769"
---
# <a name="keywordtype-complex-type"></a>Tipo complexo keywordtype

Define uma palavra-chave que identifica uma categoria de eventos. Uma palavra-chave é uma marca que você anexa a um evento para agrupar eventos com base em seu uso.

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
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



| Nome    | Tipo                                                              | Descrição                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mask    | [**HexInt64Type**](eventmanifestschema-hex64type-simpletype.md)  | Um bitmask que deve ter apenas um único conjunto de bits. O bit representa uma categoria de eventos (por exemplo, eventos de leitura ou eventos de gravação). Você pode especificar valores de bit no intervalo de 0x0000000000000001 a 0x0000800000000000 (bits 0 a 47).<br/>                                                         |
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | O nome de exibição localizado para a palavra-chave. A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto.<br/>                                                                                                       |
| name    | **QName**                                                         | O nome da palavra-chave. O nome deve ser exclusivo na lista de palavras-chave que o provedor define.<br/>                                                                                                                                                                                                     |
| símbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | O símbolo a ser usado para referenciar a palavra-chave em seu aplicativo. O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para a palavra-chave no arquivo de cabeçalho que o compilador gera. Se você não especificar um símbolo, o compilador gerará um para você.<br/> |



## <a name="remarks"></a>Comentários

O arquivo de Winmeta.xml que está incluído no SDK do Windows contém uma lista de palavras-chave. Essas palavras-chave são reservadas e não devem ser usadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





