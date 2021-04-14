---
description: Especifica se este é o perfil padrão para o dispositivo.
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
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461086"
---
# <a name="isdefault-mbnprofile-element"></a>Elemento IsDefault (MBNProfile)

O elemento **IsDefault (MBNProfile)** especifica se esse é o perfil padrão para o dispositivo.

Esse é um elemento opcional e, se não for especificado, o perfil não será definido como o perfil padrão.

O perfil padrão é usado pelo serviço de banda larga móvel para os seguintes fins

-   O serviço de banda larga móvel usa as configurações de conexão do perfil padrão ao executar conexões de rede automáticas. Essas configurações incluem nome do ponto de acesso, nome de usuário, senha, etc.
-   A política de conexão automática para um dispositivo de banda larga móvel é obtida do perfil padrão.
-   A interface do usuário da conexão de rede do sistema operacional também usa dados de conexão do perfil padrão para operações de conexão.

Os provedores de serviços de celular podem fornecer os detalhes de conexão em um perfil e configurar esse perfil como um perfil padrão. O serviço de banda larga móvel usará essas configurações de conexão sem avisar o usuário para obter detalhes.

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

O elemento **IsDefault** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
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

 

 




