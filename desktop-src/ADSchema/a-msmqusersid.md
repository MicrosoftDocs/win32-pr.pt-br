---
title: Atributo MSMQ-User-Sid
description: O SID do usuário migrado.
ms.assetid: 2bc658b7-987e-464e-9bf9-d4c7fd8a0df8
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MSMQ-User-Sid
- Esquema de AD do atributo mSMQUserSid
topic_type:
- apiref
api_name:
- MSMQ-User-Sid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d521a1f5cdfe49f4e6c030af0d70ef00a326b3382d1f80dd9b71eda977bc417b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960355"
---
# <a name="msmq-user-sid-attribute"></a>Atributo MSMQ-User-Sid

O SID do usuário migrado.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | MSMQ-usuário-Sid                                         |
| LDAP-Display-Name | mSMQUserSid                                           |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | \-                                                    |
| Frequência de atualização  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1337                               |
| System-ID-GUID    | c58aae32-56f9-11d2-90d0-00c04fd91ab1                  |
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
|------------------------|-------------------------------------------------------------|
| ID do link                | \-                                                          |
| MAPI-Id                | \-                                                          |
| System-Only            | Verdadeiro                                                        |
| É de valor único       | Verdadeiro                                                        |
| É indexado             | Falso                                                       |
| No catálogo global      | Verdadeiro                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                |
| Range-Lower            | 0                                                           |
| Range-Upper            | 128                                                         |
| Search-Flags           | 0x00000000                                                  |
| System-Flags           | 0x00000010                                                  |
| Classes usadas em        | [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------|
| ID do link                | \-                                                          |
| MAPI-Id                | \-                                                          |
| System-Only            | Verdadeiro                                                        |
| É de valor único       | Verdadeiro                                                        |
| É indexado             | Falso                                                       |
| No catálogo global      | Verdadeiro                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                |
| Range-Lower            | 0                                                           |
| Range-Upper            | 128                                                         |
| Search-Flags           | 0x00000000                                                  |
| System-Flags           | 0x00000012                                                  |
| Classes usadas em        | [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------|
| ID do link                | \-                                                          |
| MAPI-Id                | \-                                                          |
| System-Only            | Verdadeiro                                                        |
| É de valor único       | Verdadeiro                                                        |
| É indexado             | Falso                                                       |
| No catálogo global      | Verdadeiro                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                |
| Range-Lower            | 0                                                           |
| Range-Upper            | 128                                                         |
| Search-Flags           | 0x00000000                                                  |
| System-Flags           | 0x00000012                                                  |
| Classes usadas em        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------|
| ID do link                | \-                                                          |
| MAPI-Id                | \-                                                          |
| System-Only            | Verdadeiro                                                        |
| Tem valor único       | Verdadeiro                                                        |
| É indexado             | Falso                                                       |
| No Catálogo Global      | Verdadeiro                                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                                |
| Range-Lower            | 0                                                           |
| Range-Upper            | 128                                                         |
| Search-Flags           | 0x00000000                                                  |
| System-Flags           | 0x00000012                                                  |
| Classes usadas em        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------|
| ID do link                | \-                                                          |
| MAPI-Id                | \-                                                          |
| System-Only            | Verdadeiro                                                        |
| Tem valor único       | Verdadeiro                                                        |
| É indexado             | Falso                                                       |
| No Catálogo Global      | Verdadeiro                                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                                |
| Range-Lower            | 0                                                           |
| Range-Upper            | 128                                                         |
| Search-Flags           | 0x00000000                                                  |
| System-Flags           | 0x00000012                                                  |
| Classes usadas em        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------|
| ID do link                | \-                                                          |
| MAPI-Id                | \-                                                          |
| System-Only            | Verdadeiro                                                        |
| Tem valor único       | Verdadeiro                                                        |
| É indexado             | Falso                                                       |
| No Catálogo Global      | Verdadeiro                                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                                |
| Range-Lower            | 0                                                           |
| Range-Upper            | 128                                                         |
| Search-Flags           | 0x00000000                                                  |
| System-Flags           | 0x00000012                                                  |
| Classes usadas em        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> |



 

 





