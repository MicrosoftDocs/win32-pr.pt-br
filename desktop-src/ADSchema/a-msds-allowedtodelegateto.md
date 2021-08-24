---
title: Atributo ms-DS-Allowed-To-Delegate-To
description: Esse é um atributo em objetos de conta de serviço (conta de usuário ou computador).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- Atributo ms-DS-Allowed-To-Delegate-To
- Esquema do AD do atributo msDS-AllowedToDelegateTo
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d3a91abc375e67806387170ee6bda450c6f2bf167a3971f9808cd04e4c24d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704926"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a>Atributo ms-DS-Allowed-To-Delegate-To

Esse é um atributo em objetos de conta de serviço (conta de usuário ou computador). Ele contém uma lista de SPNs (Nomes de Entidade de Serviço). Esse atributo é usado para configurar um serviço para que ele possa obter tíquetes de serviço que podem ser usados para Delegação Restrita.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | ms-DS-Allowed-To-Delegate-To                |
| Ldap-Display-Name | msDS-AllowedToDelegateTo                    |
| Tamanho              | 0 a 64K                                    |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | Raramente                                |
| Attribute-Id      | 1.2.840.113556.1.4.1787                     |
| System-Id-Guid    | 800d94d7-b7a1-42a1-b14d-7cae1423d07f        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------|
| ID do link                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falso                                                              |
| Tem valor único       | Falso                                                              |
| É indexado             | Falso                                                              |
| No Catálogo Global      | Falso                                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------|
| ID do link                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falso                                                              |
| Tem valor único       | Falso                                                              |
| É indexado             | Falso                                                              |
| No Catálogo Global      | Falso                                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------|
| ID do link                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falso                                                              |
| Tem valor único       | Falso                                                              |
| É indexado             | Falso                                                              |
| No Catálogo Global      | Falso                                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------|
| ID do link                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falso                                                              |
| Tem valor único       | Falso                                                              |
| É indexado             | Falso                                                              |
| No Catálogo Global      | Falso                                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------|
| ID do link                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falso                                                              |
| Tem valor único       | Falso                                                              |
| É indexado             | Falso                                                              |
| No Catálogo Global      | Falso                                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





