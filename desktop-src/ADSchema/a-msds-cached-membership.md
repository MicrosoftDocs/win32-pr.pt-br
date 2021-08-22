---
title: Atributo ms-DS-Cached-Membership
description: O atributo ms-DS-Cached-Membership é usado pelo Gerenciador de Contas de Segurança para expansão de grupo durante a avaliação do token.
ms.assetid: e54c5d55-d292-4a6e-942a-3818f5d75301
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo ms-DS-Cached-Membership
- Esquema do AD do atributo msDS-Cached-Membership
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efcc26dc7a8d296b64103508585739340f12c8e8b4c0f6434b3b464dcc4d5356
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119296566"
---
# <a name="ms-ds-cached-membership-attribute"></a>Atributo ms-DS-Cached-Membership

O **atributo ms-DS-Cached-Membership** é usado pelo Gerenciador de Contas de Segurança para expansão de grupo durante a avaliação do token.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | ms-DS-Cached-Membership                               |
| Ldap-Display-Name | msDS-Cached-Membership                                |
| Tamanho              | BLOB binário de até 3 quilobytes.                     |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                      |
| Frequência de atualização  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1441                               |
| System-Id-Guid    | 69cab008-cdd4-4bc9-lt8-0ff37efe1b20                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | True                              |
| É indexado             | Falso                             |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | True                              |
| É indexado             | Falso                             |
| No catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



 

 





