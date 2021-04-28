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
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114574"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




