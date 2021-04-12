---
title: Tipo simples de strTableRef
description: Define uma cadeia de caracteres que faz referência a uma cadeia de caracteres de mensagem que é definida em uma tabela de cadeia de caracteres no manifesto ou em um arquivo de mensagem (. MC).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- Log de eventos de tipo simples strTableRef
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499448"
---
# <a name="strtableref-simple-type"></a>Tipo simples de strTableRef

Define uma cadeia de caracteres que faz referência a uma cadeia de caracteres de mensagem que é definida em uma tabela de cadeia de caracteres no manifesto ou em um arquivo de mensagem (. MC).

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

O tipo simples **strTableRef** é um **xs: String** que é restrito pelo seguinte padrão:

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    A cadeia de caracteres deve estar no formato, $string. *stringid* ou $MC.*symbolid*. Se a cadeia de caracteres estiver no formato, $string. *stringid*, ele deve fazer referência a uma cadeia de caracteres na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto. Se a cadeia de caracteres estiver no formato, $mc.*symbolid*, ela deverá fazer referência a um símbolo definido no arquivo de mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



 

 





