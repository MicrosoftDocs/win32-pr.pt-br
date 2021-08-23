---
title: Given-Name atributo
description: Contém o nome (nome) do usuário.
ms.assetid: acffe751-9911-4e80-8a26-351a21a6385e
ms.tgt_platform: multiple
keywords:
- Given-Name atributo AD Schema
- Esquema do AD do atributo givenName
topic_type:
- apiref
api_name:
- Given-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ee788506d098123888a9389d9256dd4203cae463cf008723e99e8180750d591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706056"
---
# <a name="given-name-attribute"></a>Given-Name atributo

Contém o nome (nome) do usuário.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Given-Name                                  |
| Ldap-Display-Name | givenName                                   |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.      |
| Frequência de atualização  | Quando o registro do usuário é criado.          |
| Attribute-Id      | 2.5.4.42                                    |
| System-Id-Guid    | f0f8ff8e-1191-11d0-a060-00aa006c33ed        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
| Tem valor único       | Verdadeiro                                                               |
| É indexado             | Verdadeiro                                                               |
| No Catálogo Global      | Verdadeiro                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                       |
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
| Tem valor único       | Verdadeiro                                                                                                                   |
| É indexado             | Verdadeiro                                                                                                                   |
| No Catálogo Global      | Verdadeiro                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                           |
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
| Tem valor único       | Verdadeiro                                                                                                                   |
| É indexado             | Verdadeiro                                                                                                                   |
| No Catálogo Global      | Verdadeiro                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                           |
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
| É de valor único       | Verdadeiro                                                                                                                   |
| É indexado             | Verdadeiro                                                                                                                   |
| No catálogo global      | Verdadeiro                                                                                                                   |
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
| É de valor único       | Verdadeiro                                                                                                                   |
| É indexado             | Verdadeiro                                                                                                                   |
| No catálogo global      | Verdadeiro                                                                                                                   |
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
| É de valor único       | Verdadeiro                                                                                                                   |
| É indexado             | Verdadeiro                                                                                                                   |
| No catálogo global      | Verdadeiro                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





