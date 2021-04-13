---
title: Atributo de origem protegido pelo MSMQ
description: Isso faz parte de um objeto MSMQ, ele é definido chamando-se API para MQCreateQueue ou MQSetProperties. Ele controla se o MSMQ aceita mensagens somente de uma fonte protegida (por exemplo, HTTPS) para essa fila.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo de origem protegido pelo MSMQ
- Esquema de MSMQ-SecuredSource do atributo AD
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499978"
---
# <a name="msmq-secured-source-attribute"></a>Atributo de origem protegido pelo MSMQ

Isso faz parte de um objeto MSMQ, ele é definido chamando-se API para MQCreateQueue ou MQSetProperties. Ele controla se o MSMQ aceita mensagens somente de uma fonte protegida (por exemplo, HTTPS) para essa fila.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Fonte protegida pelo MSMQ                  |
| LDAP-Display-Name | MSMQ-SecuredSource                   |
| Tamanho              | 4 bytes                              |
| Privilégio de atualização  | O proprietário da fila.                     |
| Frequência de atualização  | Quando uma fila é criada.             |
| Attribute-Id      | 1.2.840.113556.1.4.1713              |
| System-ID-GUID    | 8bf0221b-7a06-4d63-91f0-1499941813d3 |
| Syntax            | [**Boolean**](s-boolean.md)         |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | Falso                                        |
| No catálogo global      | True                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | Falso                                        |
| No catálogo global      | True                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | Falso                                        |
| No catálogo global      | True                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | Falso                                        |
| No catálogo global      | True                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | Falso                                        |
| No catálogo global      | True                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



 

 





