---
description: Tipo simples de CSymbolType (contadores de desempenho) – define um nome de símbolo C/C++ válido.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Tipo simples de CSymbolType (contadores de desempenho)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0771bb1dffc006abf8e02e6c391278f7d0b03f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084224"
---
# <a name="csymboltype-simple-type-performance-counters"></a>Tipo simples de CSymbolType (contadores de desempenho)

Define um nome de símbolo do C/C++ válido.

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

O tipo simples **CSymbolType** é um **xs: String** que é restrito pelo seguinte padrão:

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    O nome do símbolo pode ser vazio ou conter caracteres alfanuméricos e sublinhados. Se você especificar um nome, o nome deverá começar com um sublinhado ( \_ ) ou um caractere alfabético.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




