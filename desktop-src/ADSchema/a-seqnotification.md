---
title: Seq-Notification atributo
description: Esse atributo contém um contador que é incrementado diariamente. Esse valor de contador é dado ao serviço de acompanhamento de link, que adiciona o valor a seus volumes e vincula arquivos de origem quando eles são atualizados. O controlador de domínio mantém esse valor.
ms.assetid: 63fbded5-a21f-4a0e-aadc-568e199e8b9e
ms.tgt_platform: multiple
keywords:
- Seq-Notification atributo AD Schema
- Esquema do AD do atributo seqNotification
topic_type:
- apiref
api_name:
- Seq-Notification
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e33b2cb90617796ee48bbe3790d2692dbee9d424944135a0f4c31f5faa7724
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836706"
---
# <a name="seq-notification-attribute"></a>Seq-Notification atributo

Esse atributo contém um contador que é incrementado diariamente. Esse valor de contador é dado ao serviço de acompanhamento de link, que adiciona o valor a seus volumes e vincula arquivos de origem quando eles são atualizados. O controlador de domínio mantém esse valor.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Seq-Notification                     |
| Ldap-Display-Name | seqNotification                      |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.504               |
| System-Id-Guid    | ddac0cf2-af8f-11d0-afeb-00c04fd930c9 |
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
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| Tem valor único       | Verdadeiro                                                           |
| É indexado             | Falso                                                          |
| No Catálogo Global      | Falso                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                   |
| Range-Lower            | \-                                                             |
| Range-Upper            | \-                                                             |
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
| Range-Lower            | \-                                                             |
| Range-Upper            | \-                                                             |
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
| Range-Lower            | \-                                                             |
| Range-Upper            | \-                                                             |
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
| Range-Lower            | \-                                                             |
| Range-Upper            | \-                                                             |
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
| Range-Lower            | \-                                                             |
| Range-Upper            | \-                                                             |
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
| Range-Lower            | \-                                                             |
| Range-Upper            | \-                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes usadas em        | [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



 

 





