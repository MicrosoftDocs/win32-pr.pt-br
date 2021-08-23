---
title: Tipo simples de UInt64type (esquema EventManifest)
description: Define um tipo longo sem sinal.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- Log de eventos de tipo simples de UInt64type
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 088cdead48fb62adf816b6065e211afcc994ec618db8b7e9a0597e6f72c1780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511336"
---
# <a name="uint64type-simple-type"></a>Tipo simples de UInt64type

Define um tipo longo sem sinal. O valor pode ser especificado como um inteiro de 8 bytes ou um valor hexadecimal no intervalo de 0 a 18446744073709551615.

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





