---
title: MSMQ-atributo de nível de privacidade
description: O nível de privacidade exigido pela fila.
ms.assetid: 37addd1c-9c92-4155-99ff-dd711927717f
ms.tgt_platform: multiple
keywords:
- MSMQ-esquema de atributos de atributo de nível de privacidade
- Esquema de AD do atributo mSMQPrivacyLevel
topic_type:
- apiref
api_name:
- MSMQ-Privacy-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cb153a74fb07e82f528cdbd21dddadd528e88cb2ea49cd422bff3fd69ab623b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081790"
---
# <a name="msmq-privacy-level-attribute"></a>MSMQ-atributo de nível de privacidade

O nível de privacidade exigido pela fila.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | MSMQ-privacidade-nível                   |
| LDAP-Display-Name | mSMQPrivacyLevel                     |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.924               |
| System-ID-GUID    | 9a0dc327-c100-11d1-bbc5-0080c76670c0 |
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
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Verdadeiro                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | 0                                            |
| Range-Upper            | 2                                            |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Verdadeiro                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | 0                                            |
| Range-Upper            | 2                                            |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Verdadeiro                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | 0                                            |
| Range-Upper            | 2                                            |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Verdadeiro                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | 0                                            |
| Range-Upper            | 2                                            |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Verdadeiro                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | 0                                            |
| Range-Upper            | 2                                            |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Verdadeiro                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | 0                                            |
| Range-Upper            | 2                                            |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



 

 





