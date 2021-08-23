---
title: Atributo Trust-Auth-Outgoing
description: Informações de autenticação para a parte de saída de uma confiança.
ms.assetid: 0b63554b-b57e-4ca5-8a78-2bce5ebfea2f
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Trust-Auth-Outgoing
- Esquema do AD do atributo trustAuthOutgoing
topic_type:
- apiref
api_name:
- Trust-Auth-Outgoing
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83cb16d27447d64291dd959115a175fff3aeb0af8c483a75062bf57ae810ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644866"
---
# <a name="trust-auth-outgoing-attribute"></a>Atributo Trust-Auth-Outgoing

Informações de autenticação para a parte de saída de uma confiança.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Trust-Auth-Outgoing                                   |
| Ldap-Display-Name | trustAuthOutgoing                                     |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | \-                                                    |
| Frequência de atualização  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.135                                |
| System-Id-Guid    | bf967a5f-0de6-11d0-a285-00aa003049e2                  |
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
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No Catálogo Global      | Falso                                                |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No Catálogo Global      | Falso                                                |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No Catálogo Global      | Falso                                                |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



 

 





