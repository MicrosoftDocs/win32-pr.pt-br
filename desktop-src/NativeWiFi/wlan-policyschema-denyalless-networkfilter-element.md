---
description: Especifica se o acesso a todas as redes de infraestrutura está bloqueado.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: Elemento denyAllESS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164396"
---
# <a name="denyalless-networkfilter-element"></a>Elemento denyAllESS (networkFilter)

O elemento denyAllESS (networkFilter) especifica se o acesso a todas as redes de infraestrutura está bloqueado. Quando **denyAllESS** tem um valor de true, os computadores não podem se conectar a uma rede de infraestrutura; caso contrário, os computadores podem se conectar a redes de infraestrutura.

O valor padrão para esse elemento é FALSE. Se **denyAllESS** não for especificado em um perfil, por padrão, os computadores poderão se conectar a redes de infraestrutura.

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

O elemento **denyAllESS** é definido pelo elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

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

 

 




