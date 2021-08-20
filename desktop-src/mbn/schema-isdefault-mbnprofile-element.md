---
description: Especifica se esse é o perfil padrão para o dispositivo.
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: Elemento IsDefault (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: 7dada4789b0a1c1f11676359972eeff074928ca064c04679e35fb7e83132ef53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065900"
---
# <a name="isdefault-mbnprofile-element"></a>Elemento IsDefault (MBNProfile)

O **elemento IsDefault (MBNProfile)** especifica se esse é o perfil padrão para o dispositivo.

Esse é um elemento opcional e, se ele não for especificado, o perfil não será definido como o perfil padrão.

O perfil padrão é usado pelo serviço de banda larga móvel para as seguintes finalidades

-   O serviço de Banda Larga Móvel usa configurações de conexão do perfil padrão ao executar conexões de rede automáticas. Essas configurações incluem nome do ponto de acesso, nome de usuário, senha etc.
-   A política de conexão automática para um dispositivo de banda larga móvel é retirada do perfil padrão.
-   A interface do usuário de conexão de rede do sistema operacional também usa dados de conexão do perfil padrão para operações de conexão.

Os provedores de serviços de celular podem fornecer os detalhes de conexão em um perfil e configurar esse perfil como um perfil padrão. O serviço de Banda Larga Móvel usará essas configurações de conexão sem solicitar detalhes ao usuário.

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

O **elemento IsDefault** é definido pelo [**elemento MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows aplicativos UWP de 7 \[ \| áreas de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




