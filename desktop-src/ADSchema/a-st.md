---
title: Atributo State-ou-província-Name
description: O nome do Estado ou da província de um usuário.
ms.assetid: 2096318e-29bf-4021-a422-371835f3a62b
ms.tgt_platform: multiple
keywords:
- Esquema de atributo de nome de estado ou província
- Esquema de AD do atributo St
topic_type:
- apiref
api_name:
- State-Or-Province-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c818eb0a885d598edc10b5857aee23e336095c301d3b1059b25ba7b2f9fd986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959985"
---
# <a name="state-or-province-name-attribute"></a>Atributo State-ou-província-Name

O nome do Estado ou da província de um usuário.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Estado-ou-província-nome                                                           |
| LDAP-Display-Name | st                                                                               |
| Tamanho              | \-                                                                               |
| Privilégio de atualização  | Qualquer pessoa pode atualizar esse objeto com base na segurança do objeto que está sendo criado. |
| Frequência de atualização  | \-                                                                               |
| Attribute-Id      | 2.5.4.8                                                                          |
| System-ID-GUID    | bf967a39-0de6-11d0-a285-00aa003049e2                                             |
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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                         |
| MAPI-Id                | 0x3A28                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                      |
| No catálogo global      | Verdadeiro                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                          |
| Range-Upper            | 128                                                                                                                                                        |
| Search-Flags           | 0x00000010                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                 |
| Classes usadas em        | [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



 

 





