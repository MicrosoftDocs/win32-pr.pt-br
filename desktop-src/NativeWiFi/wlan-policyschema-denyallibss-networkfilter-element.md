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
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789883"
---
# <a name="denyallibss-networkfilter-element"></a>Elemento denyAllIBSS (networkFilter)

O elemento denyAllIBSS (networkFilter) especifica se o acesso a todas as redes ad hoc está bloqueado. Quando **denyAllIBSS** tem um valor de true, os computadores não podem se conectar a uma rede ad hoc; caso contrário, os computadores podem se conectar a redes ad hoc.

O valor padrão para esse elemento é FALSE. Se **denyAllIBSS** não for especificado em um perfil, por padrão, os computadores poderão se conectar a redes ad-hoc.

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

O elemento **denyAllIBSS** é definido pelo elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 




