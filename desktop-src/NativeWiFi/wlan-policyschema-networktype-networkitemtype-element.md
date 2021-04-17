---
description: Especifica um tipo de rede.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Elemento NetworkType (networkitemtype)
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
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757236"
---
# <a name="networktype-networkitemtype-element"></a>Elemento NetworkType (networkitemtype)

O elemento NetworkType (networkitemtype) especifica um tipo de rede. Há dois tipos de redes: redes de infraestrutura (ESS) e redes ad hoc (IBSS).

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

O elemento **NetworkType** é definido pelo tipo complexo [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

**Possíveis elementos pai imediatos na instância de esquema**
</dt> <dt>

[**rede (permitirlist)**](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[**rede (bloquearlist)**](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




