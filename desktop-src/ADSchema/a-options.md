---
title: Atributo Options
description: Um campo de bits, em que o significado do bit varia de objectClass para objectClass. Pode ocorrer em objetos de transporte entre sites, NTDS-Connection, NTDS-DSA, NTDS-Site-Settings e Site-Link.
ms.assetid: 07495cc1-1db0-4e0d-afbe-b21d2b50b6a1
ms.tgt_platform: multiple
keywords:
- Atributo de opções esquema do AD
- atributo de opções esquema do AD
topic_type:
- apiref
api_name:
- Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd970a805816e941c9eb017bf6b96302eef2b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456191"
---
# <a name="options-attribute"></a>Atributo Options

Um campo de bits, em que o significado do bit varia de objectClass para objectClass. Pode ocorrer em objetos de transporte entre sites, NTDS-Connection, NTDS-DSA, NTDS-Site-Settings e Site-Link.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Opções                              |
| LDAP-Display-Name | opções                              |
| Tamanho              | 4 bytes                              |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.307               |
| System-ID-GUID    | 19195a53-6da0-11d0-afd3-00c04fd930c9 |
| Syntax            | [**Enumeração**](s-enumeration.md) |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                  |
| É de valor único       | True                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                  |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                  |
| É de valor único       | True                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                  |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                  |
| É de valor único       | True                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                  |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                  |
| É de valor único       | True                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                  |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                  |
| É de valor único       | True                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                  |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                  |
| É de valor único       | True                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                  |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                  |
| É de valor único       | True                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                  |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



 

 





