---
description: Contém credenciais de logon para uma conexão.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Elemento UserLogonCred (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090578"
---
# <a name="userlogoncred-contexttype-element"></a>Elemento UserLogonCred (contextType)

O elemento **UserLogonCred (ContextType)** contém credenciais de logon para uma conexão.

Esse elemento pode ter os seguintes elementos filho.

-   [**Usu**](schema-username-userlogoncred-element.md)
-   [**Senha**](schema-password-userlogoncred-element.md)
-   [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md)

Esse elemento pode ter um máximo de uma ocorrência.

Esse elemento é opcional.

``` syntax
<xs:element name="UserLogonCred">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="UserName"
                type="nameType"
             />
            <xs:element name="IgnorePassword"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="Password"
                type="string"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

O elemento **UserLogonCred** é definido pelo tipo complexo [**ContextType**](schema-contexttype-complextype.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Type                                           | Descrição                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md) | booleano                                        | Como lidar com senhas ao atualizar perfis.<br/> |
| [**Senha**](schema-password-userlogoncred-element.md)             | string                                         | Senha do usuário.<br/>                                   |
| [**Usu**](schema-username-userlogoncred-element.md)             | [**nometype**](schema-nametype-simpletype.md) | Nome de usuário.<br/>                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Contexto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




