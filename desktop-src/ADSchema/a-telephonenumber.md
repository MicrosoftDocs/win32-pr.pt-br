---
title: Telephone-Number atributo
description: O número de telefone principal.
ms.assetid: 6a7faad4-9d86-4821-9b00-67adbf1b05f2
ms.tgt_platform: multiple
keywords:
- Esquema de Telephone-Number do atributo AD
- Esquema de AD do atributo telephoneNumber
topic_type:
- apiref
api_name:
- Telephone-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba099342222fcae24871730f16624fcf6336221d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086829"
---
# <a name="telephone-number-attribute"></a>Telephone-Number atributo

O número de telefone principal.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Telephone-Number                                                                 |
| LDAP-Display-Name | telephoneNumber                                                                  |
| Tamanho              | \-                                                                               |
| Privilégio de atualização  | Qualquer pessoa pode atualizar esse objeto com base na segurança do objeto que está sendo criado. |
| Frequência de atualização  | \-                                                                               |
| Attribute-Id      | 2.5.4.20                                                                         |
| System-ID-GUID    | bf967a49-0de6-11d0-a285-00aa003049e2                                             |
| Sintaxe            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                      |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                      |
| É de valor único       | True                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                      |
| No catálogo global      | True                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**Destinatário de email**](c-mailrecipient.md)<br/> [**Organização**](c-organization.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| É de valor único       | True                                                                                                                                                                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> [**Organização**](c-organization.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**espaço**](c-room.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                               |
| MAPI-Id                | 0x3A08                                                                                                           |
| System-Only            | Falso                                                                                                            |
| É de valor único       | True                                                                                                             |
| É indexado             | Falso                                                                                                            |
| No catálogo global      | True                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 64                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| É de valor único       | True                                                                                                                                                                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> [**Organização**](c-organization.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**espaço**](c-room.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| É de valor único       | True                                                                                                                                                                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> [**Organização**](c-organization.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**espaço**](c-room.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| É de valor único       | True                                                                                                                                                                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> [**Organização**](c-organization.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**espaço**](c-room.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| É de valor único       | True                                                                                                                                                                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> [**Organização**](c-organization.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**espaço**](c-room.md)<br/> |



 

 





