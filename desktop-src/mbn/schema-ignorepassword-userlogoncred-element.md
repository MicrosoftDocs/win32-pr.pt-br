---
description: Especifica como lidar com senhas ao atualizar perfis.
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: Elemento IgnorePassword (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 40211a8f848d8d0551ed39297178bc985d9efba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812310"
---
# <a name="ignorepassword-userlogoncred-element"></a>Elemento IgnorePassword (UserLogonCred)

O elemento **IgnorePassword (UserLogonCred)** especifica como lidar com senhas ao atualizar perfis.

Se definido como **true** e um perfil com o mesmo nome existir no momento da operação de atualização, a senha desse perfil será executada e armazenada em um novo perfil.

Esse elemento é opcional.

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

O elemento **IgnorePassword** é definido pelo elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**UserLogonCred (contextType)**](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




