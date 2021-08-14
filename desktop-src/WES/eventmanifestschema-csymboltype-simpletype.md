---
title: Tipo simples CSymbolType (Windows log de eventos)
description: Tipo simples CSymbolType (Windows Log de Eventos) – define um nome de símbolo C/C++ válido.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- CSymbolType tipo simples EventLog
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e51438a49a45c167b247882f0976b27a4ad8d4da048437f385ccff545663b4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589889"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>Tipo simples CSymbolType (Windows log de eventos)

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

    O nome do símbolo pode estar vazio ou conter caracteres alfanuméricos e sublinhados. Se o nome estiver vazio, o compilador de mensagem gerará o nome do símbolo. Se você especificar um nome, o nome deverá começar com um sublinhado ( \_ ) ou um caractere alfabético.

## <a name="remarks"></a>Comentários

Se o nome do símbolo estiver vazio, o compilador de mensagem usará o atributo **name** do elemento que você está definindo para gerar o nome do símbolo. O compilador substitui quaisquer caracteres não alfanuméricos e dígitos à frente por sublinhados. Por exemplo, se o  atributo de nome do canal for Microsoft-Windows-SampleProvider/Operational, o compilador usará o Microsoft \_ Windows \_ SampleProvider Operational como o nome do \_ símbolo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



 

 





