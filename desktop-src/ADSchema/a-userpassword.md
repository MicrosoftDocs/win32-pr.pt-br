---
title: User-Password atributo
description: A senha do usuário no formato UTF-8. Este é um atributo somente gravação.
ms.assetid: fcbd5e46-93fc-461e-aa6e-26d08114e73a
ms.tgt_platform: multiple
keywords:
- Esquema de User-Password do atributo AD
- Esquema de AD de atributo userPassword
topic_type:
- apiref
api_name:
- User-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84dbb0b8bbc9ebf6995738050cddb226049658b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105753638"
---
# <a name="user-password-attribute"></a>User-Password atributo

A senha do usuário no formato UTF-8. Este é um atributo somente gravação.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | User-Password                                         |
| LDAP-Display-Name | userPassword                                          |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                |
| Frequência de atualização  | \-                                                    |
| Attribute-Id      | 2.5.4.35                                              |
| System-ID-GUID    | bf967a6e-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                     |
| MAPI-Id                | 0x8153                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                  |
| É de valor único       | Falso                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                  |
| No catálogo global      | Falso                                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                           |
| Range-Lower            | 1                                                                                                                                                      |
| Range-Upper            | 128                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                             |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                       |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                    |
| É de valor único       | Falso                                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                                    |
| No catálogo global      | Falso                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                                                                                        |
| Range-Upper            | 128                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                                                                                               |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                               |
| MAPI-Id                | 0x8153                                                                                                           |
| System-Only            | Falso                                                                                                            |
| É de valor único       | Falso                                                                                                            |
| É indexado             | Falso                                                                                                            |
| No catálogo global      | Falso                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> |



 

 





