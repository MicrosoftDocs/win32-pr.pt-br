---
title: Atributo Vol-Table-GUID
description: O identificador exclusivo para uma entrada de tabela de faixa de link-volume.
ms.assetid: 3a63406a-e751-4234-a601-8f5a57f0a3b7
ms.tgt_platform: multiple
keywords:
- Atributo Vol-Table-GUID do AD Schema
- Esquema de AD do atributo volTableGUID
topic_type:
- apiref
api_name:
- Vol-Table-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a23bcd088304b4a683ce3ff0f203d3c82fecf8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456162"
---
# <a name="vol-table-guid-attribute"></a>Atributo Vol-Table-GUID

O identificador exclusivo para uma entrada de tabela de faixa de link-volume.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Vol-Table-GUID                                        |
| LDAP-Display-Name | volTableGUID                                          |
| Tamanho              | 16 bytes                                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                      |
| Frequência de atualização  | Sempre que um novo link para um arquivo for criado.             |
| Attribute-Id      | 1.2.840.113556.1.4.336                                |
| System-ID-GUID    | 1f0075fd-7e40-11d0-afd6-00c04fd930c9                  |
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
| É indexado             | Falso                                                          |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | True                                                           |
| É indexado             | Falso                                                          |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | True                                                           |
| É indexado             | Falso                                                          |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | True                                                           |
| É indexado             | Falso                                                          |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | True                                                           |
| É indexado             | Falso                                                          |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | True                                                           |
| É indexado             | Falso                                                          |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



 

 





