---
title: Tipo simples strTableRef
description: Define uma cadeia de caracteres que faz referência a uma cadeia de caracteres de mensagem definida em uma tabela de cadeia de caracteres no manifesto ou em um arquivo de mensagem (.mc).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- Tipo simples strTableRef EventLog
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97280b342015338be1cea089f8cb14121e2e51466506e89818501302c3fa891a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750912"
---
# <a name="strtableref-simple-type"></a>Tipo simples strTableRef

Define uma cadeia de caracteres que faz referência a uma cadeia de caracteres de mensagem definida em uma tabela de cadeia de caracteres no manifesto ou em um arquivo de mensagem (.mc).

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O **tipo simples strTableRef** é uma cadeia de **caracteres xs:restrita** pelo seguinte padrão:

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    A cadeia de caracteres deve estar no formato , $string. *stringid* ou $mc.*symbolid.* Se a cadeia de caracteres estiver no formato , $string. *stringid*, ele deve referenciar uma cadeia de caracteres na seção [**stringTable**](eventmanifestschema-stringtable-resources-element.md) do manifesto. Se a cadeia de caracteres estiver no formato , $mc.*symbolid*, ele deverá referenciar um símbolo definido no arquivo de mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



 

 





