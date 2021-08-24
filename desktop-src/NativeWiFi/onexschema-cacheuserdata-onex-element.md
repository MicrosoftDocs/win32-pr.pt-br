---
description: Especifica se as credenciais do usuário são armazenadas em cache para conexões subsequentes.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: Elemento cacheUserData (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d7f4663153fa9aff176180387ebaf0321ab3d48ec2c382e9e84c0f524d6e0ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800866"
---
# <a name="cacheuserdata-onex-element"></a>Elemento cacheUserData (OneX)

O elemento cacheUserData (OneX) especifica se as credenciais do usuário são armazenadas em cache para conexões subsequentes. Quando cacheUserData é TRUE, as credenciais são armazenadas em cache. Quando cacheUserData é FALSE, as credenciais não são armazenadas em cache e o usuário pode ser solicitado a obter credenciais em tentativas de conexão subsequentes.

Esse elemento é opcional. Quando cacheUserData não é especificado em um perfil, as credenciais do usuário são armazenadas em cache.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

O **elemento cacheUserData** é definido pelo [**elemento OneX.**](onexschema-onex-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




