---
title: Telefone-página inicial-atributo primário
description: O número de telefone residencial principal do usuário.
ms.assetid: 624d89fd-942c-448d-bd51-7d93954370b1
ms.tgt_platform: multiple
keywords:
- Telefone-página inicial-esquema de AD do atributo primário
- Esquema de AD do atributo homePhone
topic_type:
- apiref
api_name:
- Phone-Home-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d2e68116a15dcbf4431d33bb56b4ffed8ee2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105749380"
---
# <a name="phone-home-primary-attribute"></a>Telefone-página inicial-atributo primário

O número de telefone residencial principal do usuário.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Telefone-residência-primário                                                               |
| LDAP-Display-Name | homePhone                                                                        |
| Tamanho              | \-                                                                               |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                           |
| Frequência de atualização  | Quando o registro do usuário é criado e sempre que o número de telefone precisa ser alterado. |
| Attribute-Id      | 0.9.2342.19200300.100.1.20                                                       |
| System-ID-GUID    | f0f8ffa1-1191-11d0-a060-00aa006c33ed                                             |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------|
| ID do link                | \-                                                                 |
| MAPI-Id                | 0x3A09                                                             |
| System-Only            | Falso                                                              |
| É de valor único       | True                                                               |
| É indexado             | Falso                                                              |
| No catálogo global      | True                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| É de valor único       | True                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                    |
| No catálogo global      | True                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| É de valor único       | True                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                    |
| No catálogo global      | True                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| É de valor único       | True                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                    |
| No catálogo global      | True                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| É de valor único       | True                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                    |
| No catálogo global      | True                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| É de valor único       | True                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                    |
| No catálogo global      | True                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





