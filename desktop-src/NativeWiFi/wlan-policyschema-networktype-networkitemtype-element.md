---
description: Especifica um tipo de rede.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Elemento networkType (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 57616d6701ab4663fa6757ddec5df4886ec02faaf5088f61b6cb466ca834ec81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684386"
---
# <a name="networktype-networkitemtype-element"></a>Elemento networkType (networkItemType)

O elemento networkType (networkItemType) especifica um tipo de rede. Há dois tipos de redes: ESS (redes de infraestrutura) e redes ad hoc (IBSS).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

O **elemento networkType** é definido pelo tipo complexo [**networkItemType.**](wlan-policyschema-networkitemtype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

**Possíveis elementos pai imediatos na instância de esquema**
</dt> <dt>

[**network (allowList)**](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[**network (blockList)**](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




