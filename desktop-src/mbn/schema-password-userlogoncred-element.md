---
description: Especifica a senha usada para autenticar um usuário.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Elemento Password (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753688"
---
# <a name="password-userlogoncred-element"></a>Elemento Password (UserLogonCred)

O elemento [**password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) especifica a senha usada para autenticar um usuário.

O elemento é uma cadeia de até 255 caracteres.

Esse elemento é opcional.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

O elemento **password** é definido pelo elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .

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

 

 




