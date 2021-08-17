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
ms.openlocfilehash: 0d86054b50ae511b3f519c1c289fb529eaa8a2e7279adb7b66cbfc2df32c3758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923116"
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
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                      |



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
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                      |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                       |
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
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                       |
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
| É de valor único       | Verdadeiro                                                                                                             |
| É indexado             | Falso                                                                                                            |
| No catálogo global      | Verdadeiro                                                                                                             |
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
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                       |
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
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                       |
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
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**Organização**](c-organization.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Quarto**](c-room.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classes usadas em        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**Organização**](c-organization.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Quarto**](c-room.md)<br/> |



 

 





