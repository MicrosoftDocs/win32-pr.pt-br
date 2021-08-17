---
title: OMT-Guid atributo
description: O identificador exclusivo para uma entrada de tabela link-Track-Object-move.
ms.assetid: c8266178-4d0d-46d6-8fd9-d0c11c11c036
ms.tgt_platform: multiple
keywords:
- Esquema de OMT-Guid do atributo AD
- Esquema de AD do atributo oMTGuid
topic_type:
- apiref
api_name:
- OMT-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6aee5dd8a93611cf485286b4f833257a9e2525c96ed476ab55e7da32c645ccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442136"
---
# <a name="omt-guid-attribute"></a>OMT-Guid atributo

O identificador exclusivo para uma entrada de tabela link-Track-Object-move.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | OMT-Guid                                              |
| LDAP-Display-Name | oMTGuid                                               |
| Tamanho              | 16 bytes                                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                      |
| Frequência de atualização  | Sempre que o link de um arquivo é alterado.                 |
| Attribute-Id      | 1.2.840.113556.1.4.505                                |
| System-ID-GUID    | ddac0cf3-af8f-11d0-afeb-00c04fd930c9                  |
| Sintaxe            | [**Objeto (link de réplica)**](s-object-replica-link.md) |



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
| Classes usadas em        | [**Link-Track-OMT-entry**](c-linktrackomtentry.md)<br/> |



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
| Classes usadas em        | [**Link-Track-OMT-entry**](c-linktrackomtentry.md)<br/> |



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
| Classes usadas em        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| Tem valor único       | True                                                           |
| É indexado             | Falso                                                          |
| No Catálogo Global      | Falso                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| Tem valor único       | True                                                           |
| É indexado             | Falso                                                          |
| No Catálogo Global      | Falso                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| Tem valor único       | True                                                           |
| É indexado             | Falso                                                          |
| No Catálogo Global      | Falso                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> |



 

 





