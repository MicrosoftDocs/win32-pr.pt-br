---
title: Atributo MSMQ-multicast-address
description: Isso faz parte de um objeto MSMQ, ele é definido chamando-se API para MQCreateQueue ou MQSetProperties. Ele controla se o MSMQ aceitará mensagens de um endereço multicast.
ms.assetid: 65622cc9-81d9-42c6-b208-cac703f32244
ms.tgt_platform: multiple
keywords:
- MSMQ-multicast – atributo de endereço do AD Schema
- Esquema de MSMQ-MulticastAddress do atributo AD
topic_type:
- apiref
api_name:
- MSMQ-Multicast-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ad4deca3f742dc072f7a83363b608c1c470f50fca1626793c59b13e91fcc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762736"
---
# <a name="msmq-multicast-address-attribute"></a>Atributo MSMQ-multicast-address

Isso faz parte de um objeto MSMQ, ele é definido chamando-se API para MQCreateQueue ou MQSetProperties. Ele controla se o MSMQ aceitará mensagens de um endereço multicast.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | MSMQ-endereço de multicast                      |
| LDAP-Display-Name | MSMQ-MulticastAddress                       |
| Tamanho              | 4 bytes                                     |
| Privilégio de atualização  | O proprietário da fila.                            |
| Frequência de atualização  | Quando uma fila é criada.                    |
| Attribute-Id      | 1.2.840.113556.1.4.1714                     |
| System-ID-GUID    | 1d2f4412-f10d-4337-9b48-6e5b125cd265        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



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
| É de valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Verdadeiro                                         |
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
| É de valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Verdadeiro                                         |
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
| É de valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Verdadeiro                                         |
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
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Verdadeiro                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
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
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Verdadeiro                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Fila MSMQ**](c-msmqqueue.md)<br/> |



 

 





