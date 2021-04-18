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
ms.openlocfilehash: f58948573db281aacb00e227ff0fbc2f1cdf82b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759064"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 




