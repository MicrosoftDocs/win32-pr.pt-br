---
title: atributo ms-DS-Security-Group-extra-classes
description: Os nomes comuns das classes não padrão que podem ser adicionadas a um grupo de segurança por meio do snap-in Active Directory usuários e computadores.
ms.assetid: 3808cb03-3d54-46ca-bad8-23120ed2ca07
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-Security-Group-extra-classes
- atributo msDS-Security-Group-extra-classes, esquema do AD
topic_type:
- apiref
api_name:
- ms-DS-Security-Group-Extra-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c64746abd1114ebb3e4a97cf912a35ac730d6062721e8a11d67103d1fe82b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544726"
---
# <a name="ms-ds-security-group-extra-classes-attribute"></a>atributo ms-DS-Security-Group-extra-classes

Os nomes comuns das classes não padrão que podem ser adicionadas a um grupo de segurança por meio do snap-in Active Directory usuários e computadores.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | ms-DS-Security-Group-extra-classes          |
| LDAP-Display-Name | msDS-Security-Group-extra classes           |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio                        |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.1688                     |
| System-ID-GUID    | 4f146ae8-a4fe-4801-a731-f51848a4f4e4        |
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

[**ms-DS-Non-Security-Group-Extra-Classes**](a-msds-non-security-group-extra-classes.md)
</dt> </dl>

 

 





