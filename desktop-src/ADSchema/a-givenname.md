---
title: Given-Name atributo
description: Contém o nome fornecido (nome) do usuário.
ms.assetid: acffe751-9911-4e80-8a26-351a21a6385e
ms.tgt_platform: multiple
keywords:
- Esquema de Given-Name do atributo AD
- Esquema de AD do atributo especificado
topic_type:
- apiref
api_name:
- Given-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76ab181c6aaf03c2a497be1718df789bfddc6b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825246"
---
# <a name="given-name-attribute"></a>Given-Name atributo

Contém o nome fornecido (nome) do usuário.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Given-Name                                  |
| LDAP-Display-Name | givenName                                   |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.      |
| Frequência de atualização  | Quando o registro do usuário é criado.          |
| Attribute-Id      | 2.5.4.42                                    |
| System-ID-GUID    | f0f8ff8e-1191-11d0-a060-00aa006c33ed        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



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
| MAPI-Id                | 0x3A06                                                             |
| System-Only            | Falso                                                              |
| É de valor único       | True                                                               |
| É indexado             | True                                                               |
| No catálogo global      | True                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000005                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| É de valor único       | True                                                                                                                   |
| É indexado             | True                                                                                                                   |
| No catálogo global      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| É de valor único       | True                                                                                                                   |
| É indexado             | True                                                                                                                   |
| No catálogo global      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| É de valor único       | True                                                                                                                   |
| É indexado             | True                                                                                                                   |
| No catálogo global      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| É de valor único       | True                                                                                                                   |
| É indexado             | True                                                                                                                   |
| No catálogo global      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| É de valor único       | True                                                                                                                   |
| É indexado             | True                                                                                                                   |
| No catálogo global      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





