---
title: Country-Name atributo
description: O país/região no endereço do usuário. O país/região é representado como um código de 2 caracteres com base no ISO-3166.
ms.assetid: a7c12019-01ca-4011-8320-cd7a4de882e9
ms.tgt_platform: multiple
keywords:
- Esquema de Country-Name do atributo AD
- Esquema de AD do atributo c
topic_type:
- apiref
api_name:
- Country-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066e488642622427348b02f68ecf8706cccdb74210ab641033f0374db253895c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119307206"
---
# <a name="country-name-attribute"></a>Country-Name atributo

O país/região no endereço do usuário. O país/região é representado como um código de 2 caracteres com base no ISO-3166.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Country-Name                                |
| LDAP-Display-Name | c                                           |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 2.5.4.6                                     |
| System-ID-GUID    | bf967945-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



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
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                        |
| MAPI-Id                | 0x8069                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                     |
| É de valor único       | Verdadeiro                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                     |
| No catálogo global      | Verdadeiro                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                         |
| Range-Upper            | 3                                                                                                                                                                         |
| Search-Flags           | 0x00000010                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                |
| Classes usadas em        | [**País**](c-country.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                        |
| MAPI-Id                | 0x8069                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                     |
| É de valor único       | Verdadeiro                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                     |
| No catálogo global      | Verdadeiro                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                         |
| Range-Upper            | 3                                                                                                                                                                         |
| Search-Flags           | 0x00000010                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                |
| Classes usadas em        | [**País**](c-country.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                     |
| MAPI-Id                | 0x8069                                                                                                 |
| System-Only            | Falso                                                                                                  |
| É de valor único       | Verdadeiro                                                                                                   |
| É indexado             | Falso                                                                                                  |
| No catálogo global      | Verdadeiro                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                           |
| Range-Lower            | 1                                                                                                      |
| Range-Upper            | 3                                                                                                      |
| Search-Flags           | 0x00000010                                                                                             |
| System-Flags           | 0x00000012                                                                                             |
| Classes usadas em        | [**País**](c-country.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                        |
| MAPI-Id                | 0x8069                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                     |
| Tem valor único       | Verdadeiro                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                     |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                         |
| Range-Upper            | 3                                                                                                                                                                         |
| Search-Flags           | 0x00000010                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                |
| Classes usadas em        | [**País**](c-country.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                        |
| MAPI-Id                | 0x8069                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                     |
| Tem valor único       | Verdadeiro                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                     |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                         |
| Range-Upper            | 3                                                                                                                                                                         |
| Search-Flags           | 0x00000010                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                |
| Classes usadas em        | [**País**](c-country.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                        |
| MAPI-Id                | 0x8069                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                     |
| Tem valor único       | Verdadeiro                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                     |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                         |
| Range-Upper            | 3                                                                                                                                                                         |
| Search-Flags           | 0x00000010                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                |
| Classes usadas em        | [**País**](c-country.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                        |
| MAPI-Id                | 0x8069                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                     |
| Tem valor único       | Verdadeiro                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                     |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                         |
| Range-Upper            | 3                                                                                                                                                                         |
| Search-Flags           | 0x00000010                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                |
| Classes usadas em        | [**País**](c-country.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



 

 





