---
title: Object-Sid atributo
description: Um valor binário que especifica o identificador de segurança (SID) do usuário. O SID é um valor exclusivo usado para identificar o usuário como uma entidade de segurança.
ms.assetid: 78ef0158-f59e-43df-b3fc-fb0f709936f6
ms.tgt_platform: multiple
keywords:
- Esquema de Object-Sid do atributo AD
- atributo do AD de atributos do objectSid
topic_type:
- apiref
api_name:
- Object-Sid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b536650177f873cbbc349096e84c3de274b8d376
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086875"
---
# <a name="object-sid-attribute"></a>Object-Sid atributo

Um valor binário que especifica o identificador de segurança (SID) do usuário. O SID é um valor exclusivo usado para identificar o usuário como uma entidade de segurança.



| Entrada | Valor |
|-------------------|--------------------------------------------------------------|
| CN                | Object-Sid                                                   |
| LDAP-Display-Name | objectSid                                                    |
| Tamanho              | \-                                                           |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                             |
| Frequência de atualização  | Esse valor é definido pelo sistema quando a conta é criada. |
| Attribute-Id      | 1.2.840.113556.1.4.146                                       |
| System-ID-GUID    | bf9679e8-0de6-11d0-a285-00aa003049e2                         |
| Sintaxe            | [**Cadeia de caracteres (SID)**](s-string-sid.md)                          |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                      |
| É de valor único       | True                                                                                                                                                                                                                                                       |
| É indexado             | True                                                                                                                                                                                                                                                       |
| No catálogo global      | True                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**Entidade de segurança estrangeira**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | True                                                                                                                                                                                                                                                       |
| É de valor único       | True                                                                                                                                                                                                                                                       |
| É indexado             | True                                                                                                                                                                                                                                                       |
| No catálogo global      | True                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**Entidade de segurança estrangeira**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                               |
| MAPI-Id                | 0x8027                                                                                                                                                                                           |
| System-Only            | True                                                                                                                                                                                             |
| É de valor único       | True                                                                                                                                                                                             |
| É indexado             | True                                                                                                                                                                                             |
| No catálogo global      | True                                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                |
| Range-Upper            | 28                                                                                                                                                                                               |
| Search-Flags           | 0x00000009                                                                                                                                                                                       |
| System-Flags           | 0x00000012                                                                                                                                                                                       |
| Classes usadas em        | [**Entidade de segurança estrangeira**](c-foreignsecurityprincipal.md)<br/> [**ms-DS-BIND-proxy**](c-msds-bindproxy.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | True                                                                                                                                                                                                                                                       |
| É de valor único       | True                                                                                                                                                                                                                                                       |
| É indexado             | True                                                                                                                                                                                                                                                       |
| No catálogo global      | True                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**Entidade de segurança estrangeira**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | True                                                                                                                                                                                                                                                       |
| É de valor único       | True                                                                                                                                                                                                                                                       |
| É indexado             | True                                                                                                                                                                                                                                                       |
| No catálogo global      | True                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**Entidade de segurança estrangeira**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | True                                                                                                                                                                                                                                                       |
| É de valor único       | True                                                                                                                                                                                                                                                       |
| É indexado             | True                                                                                                                                                                                                                                                       |
| No catálogo global      | True                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**Entidade de segurança estrangeira**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | True                                                                                                                                                                                                                                                       |
| É de valor único       | True                                                                                                                                                                                                                                                       |
| É indexado             | True                                                                                                                                                                                                                                                       |
| No catálogo global      | True                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**Entidade de segurança estrangeira**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> |



 

 





