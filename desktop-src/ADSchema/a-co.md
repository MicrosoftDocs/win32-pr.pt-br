---
title: Text-Country atributo
description: O país/região em que o usuário está localizado.
ms.assetid: 6024de35-9ab5-4e03-97dc-0ebf830e5754
ms.tgt_platform: multiple
keywords:
- Esquema de Text-Country do atributo AD
- Esquema do AD do atributo co
topic_type:
- apiref
api_name:
- Text-Country
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f208ffe60e968632b6f90b534a5240c85f819587
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645593"
---
# <a name="text-country-attribute"></a>Text-Country atributo

O país/região em que o usuário está localizado.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Text-Country                                |
| LDAP-Display-Name | co                                          |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.2.131                      |
| System-ID-GUID    | f0f8ffa7-1191-11d0-a060-00aa006c33ed        |
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
| MAPI-Id                | 0x3A26                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                     |
| É de valor único       | True                                                                                                                                                                      |
| É indexado             | Falso                                                                                                                                                                     |
| No catálogo global      | Falso                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                |
| Classes usadas em        | [**País**](c-country.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                |
| MAPI-Id                | 0x3A26                                                                                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                                                                                             |
| É de valor único       | True                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                             |
| No catálogo global      | Falso                                                                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                 |
| Range-Upper            | 128                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                                                        |
| Classes usadas em        | [**País**](c-country.md)<br/> [**friendlyCountry**](c-friendlycountry.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                     |
| MAPI-Id                | 0x3A26                                                                                                 |
| System-Only            | Falso                                                                                                  |
| É de valor único       | True                                                                                                   |
| É indexado             | Falso                                                                                                  |
| No catálogo global      | Falso                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                           |
| Range-Lower            | 1                                                                                                      |
| Range-Upper            | 128                                                                                                    |
| Search-Flags           | 0x00000010                                                                                             |
| System-Flags           | 0x00000010                                                                                             |
| Classes usadas em        | [**País**](c-country.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                |
| MAPI-Id                | 0x3A26                                                                                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                                                                                             |
| É de valor único       | True                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                             |
| No catálogo global      | Falso                                                                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                 |
| Range-Upper            | 128                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                                                        |
| Classes usadas em        | [**País**](c-country.md)<br/> [**friendlyCountry**](c-friendlycountry.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                |
| MAPI-Id                | 0x3A26                                                                                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                                                                                             |
| É de valor único       | True                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                             |
| No catálogo global      | Falso                                                                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                 |
| Range-Upper            | 128                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                                                        |
| Classes usadas em        | [**País**](c-country.md)<br/> [**friendlyCountry**](c-friendlycountry.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                |
| MAPI-Id                | 0x3A26                                                                                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                                                                                             |
| É de valor único       | True                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                             |
| No catálogo global      | Falso                                                                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                 |
| Range-Upper            | 128                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                                                        |
| Classes usadas em        | [**País**](c-country.md)<br/> [**friendlyCountry**](c-friendlycountry.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                |
| MAPI-Id                | 0x3A26                                                                                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                                                                                             |
| É de valor único       | True                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                             |
| No catálogo global      | Falso                                                                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                 |
| Range-Upper            | 128                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                                                        |
| Classes usadas em        | [**País**](c-country.md)<br/> [**friendlyCountry**](c-friendlycountry.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



 

 





