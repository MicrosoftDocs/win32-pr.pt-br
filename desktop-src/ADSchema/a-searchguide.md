---
title: Search-Guide atributo
description: Especifica informações de critérios de pesquisa sugeridos, que podem ser incluídos em algumas entradas que devem ser um objeto base conveniente para a operação de pesquisa, por exemplo, país/região ou organização.
ms.assetid: 69823ef3-efa8-4732-bbec-27ed8fec81cc
ms.tgt_platform: multiple
keywords:
- Esquema de Search-Guide do atributo AD
- Esquema de AD do atributo searchGuide
topic_type:
- apiref
api_name:
- Search-Guide
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711202ebc39649e7e1aea2a4459c3a7147eb2ff6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755441"
---
# <a name="search-guide-attribute"></a>Search-Guide atributo

Especifica informações de critérios de pesquisa sugeridos, que podem ser incluídos em algumas entradas que devem ser um objeto base conveniente para a operação de pesquisa, por exemplo, país/região ou organização.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Search-Guide                                          |
| LDAP-Display-Name | searchGuide                                           |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | Administrador de domínio                                  |
| Frequência de atualização  | Sempre que um novo guia de pesquisa for desejado.               |
| Attribute-Id      | 2.5.4.14                                              |
| System-ID-GUID    | bf967a2e-0de6-11d0-a285-00aa003049e2                  |
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
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| É de valor único       | Falso                                                                                                                                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                                                                                                                                     |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| É de valor único       | Falso                                                                                                                                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                                                                                                                                     |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                 |
| MAPI-Id                | 0x812E                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                              |
| É de valor único       | Falso                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                              |
| No catálogo global      | Falso                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classes usadas em        | [**País**](c-country.md)<br/> [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| É de valor único       | Falso                                                                                                                                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                                                                                                                                     |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| É de valor único       | Falso                                                                                                                                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                                                                                                                                     |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| É de valor único       | Falso                                                                                                                                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                                                                                                                                     |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| É de valor único       | Falso                                                                                                                                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                                                                                                                                     |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidade**](c-locality.md)<br/> [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



 

 





