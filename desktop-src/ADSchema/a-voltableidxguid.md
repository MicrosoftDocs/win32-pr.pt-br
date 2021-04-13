---
title: Atributo Vol-Table-IDX-GUID
description: O identificador de índice para uma entrada de tabela de faixa de link-volume.
ms.assetid: f6df4ff1-87aa-480e-90f5-0a47822cd461
ms.tgt_platform: multiple
keywords:
- Vol-Table-IDX-GUID atributo AD Schema
- Esquema de AD do atributo volTableIdxGUID
topic_type:
- apiref
api_name:
- Vol-Table-Idx-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a760d99b6883ea070e2f06daf11227056ea74a08
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500022"
---
# <a name="vol-table-idx-guid-attribute"></a>Atributo Vol-Table-IDX-GUID

O identificador de índice para uma entrada de tabela de faixa de link-volume.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Vol-Table-IDX-GUID                                    |
| LDAP-Display-Name | volTableIdxGUID                                       |
| Tamanho              | 16 bytes                                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                      |
| Frequência de atualização  | Sempre que um novo link para um arquivo for criado.             |
| Attribute-Id      | 1.2.840.113556.1.4.334                                |
| System-ID-GUID    | 1f0075fb-7e40-11d0-afd6-00c04fd930c9                  |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | True                                                           |
| É indexado             | True                                                           |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000001                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | True                                                           |
| É indexado             | True                                                           |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000001                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | True                                                           |
| É indexado             | True                                                           |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000001                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | True                                                           |
| É indexado             | True                                                           |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000001                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | True                                                           |
| É indexado             | True                                                           |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000001                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | True                                                           |
| É indexado             | True                                                           |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000001                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



 

 





