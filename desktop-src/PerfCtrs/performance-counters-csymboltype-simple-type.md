---
description: Tipo simples CSymbolType (contadores de desempenho) – define um nome de símbolo C/C++ válido.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Tipo simples CSymbolType (contadores de desempenho)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4ebba4d72b7bc79f2aaefccfa2d71e57abd82aa06efb09abc2e83cebdb513f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033526"
---
# <a name="csymboltype-simple-type-performance-counters"></a>Tipo simples CSymbolType (contadores de desempenho)

Define um nome de símbolo C/C++ válido.

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Padrões

O **tipo simples CSymbolType** é uma cadeia de **caracteres xs:restrita** pelo seguinte padrão:

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    O nome do símbolo pode estar vazio ou conter caracteres alfanuméricos e sublinhados. Se você especificar um nome, o nome deverá começar com um sublinhado ( \_ ) ou um caractere alfabético.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 




