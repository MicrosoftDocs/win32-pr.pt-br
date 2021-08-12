---
description: Especifica se o acesso a todas as redes ad hoc está bloqueado.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: Elemento denyAllIBSS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9f34a45a0fc527c4c27e24ad3137dfe49438f9255baf1893e1090137bfb40a3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619531"
---
# <a name="denyallibss-networkfilter-element"></a>Elemento denyAllIBSS (networkFilter)

O elemento denyAllIBSS (networkFilter) especifica se o acesso a todas as redes ad hoc está bloqueado. Quando **denyAllIBSS tem** um valor TRUE, os máquinas não podem se conectar a uma rede ad hoc; caso contrário, os máquinas podem se conectar a redes ad hoc.

O valor padrão para esse elemento é FALSE. Se **denyAllIBSS não** for especificado em um perfil, os máquinas padrão poderão se conectar a redes ad hoc.

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

O **elemento denyAllIBSS** é definido pelo [**elemento networkFilter.**](wlan-policyschema-networkfilter-wlanpolicy-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




