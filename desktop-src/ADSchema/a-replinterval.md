---
title: Repl-Interval atributo
description: O atributo de objetos Site-Link que define o intervalo, em minutos, entre os ciclos de replicação entre os sites na lista de sites.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Esquema de Repl-Interval do atributo AD
- Esquema de AD do atributo replInterval
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e681b01fbc60b775b0cb947007056dc1d3d3adbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086859"
---
# <a name="repl-interval-attribute"></a>Repl-Interval atributo

O atributo de objetos Site-Link que define o intervalo, em minutos, entre os ciclos de replicação entre os sites na lista de sites. Deve ser um múltiplo de 15 minutos (a granularidade da replicação de DS entre sites), um mínimo de 15 minutos e um máximo de 10.080 minutos (uma semana).



| Entrada | Valor |
|-------------------|------------------------------------------------|
| CN                | Repl-Interval                                  |
| LDAP-Display-Name | replInterval                                   |
| Tamanho              | 4 bytes                                        |
| Privilégio de atualização  | Administrador corporativo                       |
| Frequência de atualização  | Quando o intervalo de replicação precisa ser alterado. |
| Attribute-Id      | 1.2.840.113556.1.4.1336                        |
| System-ID-GUID    | 45ba9d1a-56fa-11d2-90d0-00c04fd91ab1           |
| Sintaxe            | [**Enumeração**](s-enumeration.md)           |



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
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | True                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | True                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | True                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | True                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | True                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | True                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | True                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Transporte entre sites**](c-intersitetransport.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



 

 





