---
title: Atributo Vol-Table-GUID
description: O identificador exclusivo para uma entrada de tabela Link-Track-Volume.
ms.assetid: 3a63406a-e751-4234-a601-8f5a57f0a3b7
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Vol-Table-GUID
- Esquema do AD do atributo volTableGUID
topic_type:
- apiref
api_name:
- Vol-Table-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d692efd1f16c8e66816d49ec13f947b88da0fa0f8200787a5d5f9cda1bdf0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065566"
---
# <a name="vol-table-guid-attribute"></a>Atributo Vol-Table-GUID

O identificador exclusivo para uma entrada de tabela Link-Track-Volume.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Vol-Table-GUID                                        |
| Ldap-Display-Name | volTableGUID                                          |
| Tamanho              | 16 bytes                                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                      |
| Frequência de atualização  | Sempre que um novo link para um arquivo é criado.             |
| Attribute-Id      | 1.2.840.113556.1.4.336                                |
| System-Id-Guid    | 1f0075fd-7e40-11d0-afd6-00c04fd930c9                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
| Tem valor único       | Verdadeiro                                                           |
| É indexado             | Falso                                                          |
| No Catálogo Global      | Falso                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| Tem valor único       | Verdadeiro                                                           |
| É indexado             | Falso                                                          |
| No Catálogo Global      | Falso                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| Tem valor único       | Verdadeiro                                                           |
| É indexado             | Falso                                                          |
| No Catálogo Global      | Falso                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                   |
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
| É de valor único       | Verdadeiro                                                           |
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
| É de valor único       | Verdadeiro                                                           |
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
| É de valor único       | Verdadeiro                                                           |
| É indexado             | Falso                                                          |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



 

 





