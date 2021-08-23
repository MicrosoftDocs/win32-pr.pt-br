---
title: Atributo FRS-Working-Path
description: O caminho para o banco de dados de replicação de arquivo.
ms.assetid: 43db1214-17a3-4458-b082-1cf69d06384c
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo FRS-Working-Path
- Esquema do AD do atributo fRSWorkingPath
topic_type:
- apiref
api_name:
- FRS-Working-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 438e329915ebdffa888cb82bc7fad269cc3a81abac977a82860b20137ebb2172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323326"
---
# <a name="frs-working-path-attribute"></a>Atributo FRS-Working-Path

O caminho para o banco de dados de replicação de arquivo.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | FRS-Working-Path                            |
| Ldap-Display-Name | fRSWorkingPath                              |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.486                      |
| System-Id-Guid    | 1be8f173-a9ff-11d0-afe2-00c04fd930c9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
| Range-Upper            | 2.048                                                           |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**NTFRS-Subscriptions**](c-ntfrssubscriptions.md)<br/> |



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
| Range-Upper            | 2.048                                                           |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**NTFRS-Subscriptions**](c-ntfrssubscriptions.md)<br/> |



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
| Range-Upper            | 2.048                                                           |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**NTFRS-assinaturas**](c-ntfrssubscriptions.md)<br/> |



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
| Range-Upper            | 2.048                                                           |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**NTFRS-assinaturas**](c-ntfrssubscriptions.md)<br/> |



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
| Range-Upper            | 2.048                                                           |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**NTFRS-assinaturas**](c-ntfrssubscriptions.md)<br/> |



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
| Range-Upper            | 2.048                                                           |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**NTFRS-assinaturas**](c-ntfrssubscriptions.md)<br/> |



 

 





