---
title: FRS-atributo de nível de autenticação de parceiro
description: O nível de segurança RPC.
ms.assetid: ec7a8d92-33c0-415a-bc38-5b7df81226bc
ms.tgt_platform: multiple
keywords:
- FRS-parceiro-do atributo de nível de autenticação esquema do AD
- Esquema de AD do atributo fRSPartnerAuthLevel
topic_type:
- apiref
api_name:
- FRS-Partner-Auth-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9549798a8360468a96e70e85906e9f83ae9cefedc5883247438105f104472839
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119306376"
---
# <a name="frs-partner-auth-level-attribute"></a>FRS-atributo de nível de autenticação de parceiro

O nível de segurança RPC.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | FRS-parceiro-nível de autenticação               |
| LDAP-Display-Name | fRSPartnerAuthLevel                  |
| Tamanho              | 4 bytes                              |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.877               |
| System-ID-GUID    | 2a132580-9373-11d1-aebc-0000f80367c1 |
| Syntax            | [**Enumeração**](s-enumeration.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| É de valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No Catálogo Global      | Falso                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Membro NTFRS**](c-ntfrsmember.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No Catálogo Global      | Falso                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Membro NTFRS**](c-ntfrsmember.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No Catálogo Global      | Falso                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Membro NTFRS**](c-ntfrsmember.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



 

 





