---
title: Country-Code atributo
description: Especifica o código de país/região para o idioma de escolha do usuário. esse valor não é usado pelo Windows 2000.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Esquema de Country-Code do atributo AD
- Esquema de AD do atributo countryCode
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7843a2724043e504538ad6388e92dfc205463e76e082c266b5ee1f4f095207ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961775"
---
# <a name="country-code-attribute"></a>Country-Code atributo

Especifica o código de país/região para o idioma de escolha do usuário. esse valor não é usado pelo Windows 2000.



| Entrada | Valor |
|-------------------|-----------------------------------------|
| CN                | Country-Code                            |
| LDAP-Display-Name | countryCode                             |
| Tamanho              | 2 bytes                                 |
| Privilégio de atualização  | Proprietário da conta ou administrador de domínio   |
| Frequência de atualização  | Quando o país/região do usuário é alterado. |
| Attribute-Id      | 1.2.840.113556.1.4.25                   |
| System-ID-GUID    | 5fd42471-1262-11d0-a060-00aa006c33ed    |
| Syntax            | [**Enumeração**](s-enumeration.md)    |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| É de valor único       | Verdadeiro                                                                                                                              |
| É indexado             | Falso                                                                                                                             |
| No catálogo global      | Falso                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                      |
| Range-Lower            | \-                                                                                                                                |
| Range-Upper            | \-                                                                                                                                |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| É de valor único       | Verdadeiro                                                                                                                              |
| É indexado             | Falso                                                                                                                             |
| No catálogo global      | Falso                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | Verdadeiro                                                           |
| É indexado             | Falso                                                          |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 65535                                                          |
| Search-Flags           | 0x00000010                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| É de valor único       | Verdadeiro                                                                                                                              |
| É indexado             | Falso                                                                                                                             |
| No catálogo global      | Falso                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| É de valor único       | Verdadeiro                                                                                                                              |
| É indexado             | Falso                                                                                                                             |
| No catálogo global      | Falso                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| É de valor único       | Verdadeiro                                                                                                                              |
| É indexado             | Falso                                                                                                                             |
| No catálogo global      | Falso                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| É de valor único       | Verdadeiro                                                                                                                              |
| É indexado             | Falso                                                                                                                             |
| No catálogo global      | Falso                                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



 

 





