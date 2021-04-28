---
title: Tipo simples UInt32type (log de eventos do Windows)
description: Tipo simples de UInt32type (log de eventos do Windows) – define um tipo inteiro sem sinal.
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- Log de eventos de tipo simples UInt32type
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 631bb3e8424db8a5d781aaa43df6096730aaa4d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090564"
---
# <a name="uint32type-simple-type-windows-event-log"></a>Tipo simples UInt32type (log de eventos do Windows)

Define um tipo inteiro sem sinal. O valor pode ser especificado como um inteiro de 4 bytes ou um valor hexadecimal no intervalo de 0 a 4.294.967.295.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





