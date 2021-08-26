---
description: Tipo simples de UInt32type (contadores de desempenho) – define um tipo de inteiro sem sinal.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Tipo simples UInt32type (contadores de desempenho)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92eafff1be2c1dc924a7041ad45cadfca994d03d776f61a3c866d6c3c2f6f380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033376"
---
# <a name="uint32type-simple-type-performance-counters"></a>Tipo simples UInt32type (contadores de desempenho)

Define um tipo inteiro sem sinal.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Comentários

Você pode especificar o valor como um inteiro de 4 bytes ou um valor hexadecimal no intervalo de 0 a 4.294.967.295.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 




