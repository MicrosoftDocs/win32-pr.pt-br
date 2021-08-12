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
ms.openlocfilehash: 5057f94dd91e2d7090c4f147ba987324e369dda706031ecebb8a79b165214414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619861"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



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

 

 




