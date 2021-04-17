---
title: Tipo simples de CSymbolType (log de eventos do Windows)
description: Define um nome de símbolo do C/C++ válido.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Log de eventos de tipo simples CSymbolType
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67b0ccb7c573aa4d71c038f9133cea7c95cdfbd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813210"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>Tipo simples de CSymbolType (log de eventos do Windows)

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

    O nome do símbolo pode ser vazio ou conter caracteres alfanuméricos e sublinhados. Se o nome estiver vazio, o compilador de mensagem irá gerar o nome do símbolo. Se você especificar um nome, o nome deverá começar com um sublinhado ( \_ ) ou um caractere alfabético.

## <a name="remarks"></a>Comentários

Se o nome do símbolo estiver vazio, o compilador de mensagem usará o atributo **Name** do elemento que você está definindo para gerar o nome do símbolo. O compilador substitui os caracteres não alfanuméricos e os dígitos à esquerda por sublinhados. Por exemplo, se o atributo de **nome** do canal for Microsoft-Windows-SampleProvider/Operational, o compilador usará o Microsoft \_ Windows \_ SampleProvider \_ operacional como o nome do símbolo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



 

 





