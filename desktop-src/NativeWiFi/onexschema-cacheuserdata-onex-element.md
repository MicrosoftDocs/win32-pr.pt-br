---
description: Especifica se as credenciais do usuário são armazenadas em cache para as conexões subsequentes.
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
ms.openlocfilehash: 8650bb2e5899e96f921d57460c8ba49ffab0ea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921633"
---
# <a name="cacheuserdata-onex-element"></a>Elemento cacheUserData (OneX)

O elemento cacheUserData (OneX) especifica se as credenciais do usuário são armazenadas em cache para conexões subsequentes. Quando cacheUserData é TRUE, as credenciais são armazenadas em cache. Quando cacheUserData é FALSE, as credenciais não são armazenadas em cache e o usuário pode ser solicitado a fornecer credenciais em tentativas de conexão subsequentes.

Esse elemento é opcional. Quando cacheUserData não é especificado em um perfil, as credenciais do usuário são armazenadas em cache.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

O elemento **cacheUserData** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> </dl>

 

 




