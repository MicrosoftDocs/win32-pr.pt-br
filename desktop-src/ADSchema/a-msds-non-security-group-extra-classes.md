---
title: atributo ms-DS-non-Security-Group-extra-classes
description: Os nomes comuns das classes não padrão que podem ser adicionadas a um grupo de não segurança por meio do snap-in Active Directory usuários e computadores.
ms.assetid: 5b89c8d2-0450-480b-9252-17ae375e3a57
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-non-Security-Group-extra-classes
- atributo msDS-non-Security-Group-extra-classes, esquema do AD
topic_type:
- apiref
api_name:
- ms-DS-Non-Security-Group-Extra-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01ec292c29de72cb2df92eb7c4246392e3b12b4dc2008caf2a09ab1be5a8b1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118683921"
---
# <a name="ms-ds-non-security-group-extra-classes-attribute"></a>atributo ms-DS-non-Security-Group-extra-classes

Os nomes comuns das classes não padrão que podem ser adicionadas a um grupo de não segurança por meio do snap-in Active Directory usuários e computadores.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | ms-DS-non-Security-Group-extra-classes      |
| LDAP-Display-Name | msDS-não Security-Group-extra-classes       |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio                        |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.1689                     |
| System-ID-GUID    | 2de144fc-1f52-486f-bdf4-16fcc3084e54        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------|
| ID do link                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| É de valor único       | Falso                                               |
| É indexado             | Falso                                               |
| No catálogo global      | Falso                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Classes usadas em        | [**DS-interface do usuário-Configurações**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------|
| ID do link                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| É de valor único       | Falso                                               |
| É indexado             | Falso                                               |
| No catálogo global      | Falso                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Classes usadas em        | [**DS-interface do usuário-Configurações**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------|
| ID do link                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| É de valor único       | Falso                                               |
| É indexado             | Falso                                               |
| No catálogo global      | Falso                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Classes usadas em        | [**DS-interface do usuário-Configurações**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------|
| ID do link                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| Tem valor único       | Falso                                               |
| É indexado             | Falso                                               |
| No Catálogo Global      | Falso                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Classes usadas em        | [**DS-UI-Configurações**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------|
| ID do link                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| Tem valor único       | Falso                                               |
| É indexado             | Falso                                               |
| No Catálogo Global      | Falso                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Classes usadas em        | [**DS-UI-Configurações**](c-dsuisettings.md)<br/> |



## <a name="remarks"></a>Comentários

A lista a seguir identifica as classes padrão que podem ser adicionadas a um grupo por meio Usuários e Computadores do Active Directory snap-in.

-   [**Grupo**](c-group.md)
-   [**Usuário**](c-user.md)
-   [**inetOrgPerson**](c-inetorgperson.md)
-   [**Contact**](c-contact.md)
-   [**Computador**](c-computer.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ms-DS-Security-Group-Extra-Classes**](a-msds-security-group-extra-classes.md)
</dt> </dl>

 

 





