---
description: Define uma rede bloqueada.
ms.assetid: ccf24d45-cae0-4eb7-951a-004a5f71e04a
title: Elemento de rede (blocklist)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 893c557ca5c20dd73f10f2a31d3b416d76116deb206f5d04420d35443d902130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984456"
---
# <a name="network-blocklist-element"></a>Elemento de rede (blocklist)

O elemento de rede (blocklist) define uma rede bloqueada. Um computador não pode se conectar a uma rede bloqueada.

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

O elemento **Network** é definido pelo elemento [**blocklist**](wlan-policyschema-blocklist-networkfilter-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Bloqueios**](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Blocklist (networkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> </dl>

 

 




