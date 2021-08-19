---
title: Admin-Count atributo
description: Indica que um determinado objeto teve suas ACLs alteradas para um valor mais seguro pelo sistema porque ele era membro de um dos grupos administrativos (direta ou transitivamente).
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Admin-Count atributo AD Schema
- Esquema do AD do atributo adminCount
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d652d53627643e1028ee73cc67678119c689e46d8f4ec289c92ca32127e098dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022844"
---
# <a name="admin-count-attribute"></a>Admin-Count atributo

Indica que um determinado objeto teve suas ACLs alteradas para um valor mais seguro pelo sistema porque ele era membro de um dos grupos administrativos (direta ou transitivamente).



| Entrada | Valor |
|-------------------|-----------------------------------------------------|
| CN                | Admin-Count                                         |
| Ldap-Display-Name | adminCount                                          |
| Tamanho              | 4 bytes                                             |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                    |
| Frequência de atualização  | Quando um objeto é adicionado a um grupo administrativo. |
| Attribute-Id      | 1.2.840.113556.1.4.150                              |
| System-Id-Guid    | bf967918-0de6-11d0-a285-00aa003049e2                |
| Syntax            | [**Enumeração**](s-enumeration.md)                |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------|
| ID do link                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Tem valor único       | Verdadeiro                                                                  |
| É indexado             | Falso                                                                 |
| No Catálogo Global      | Falso                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------|
| ID do link                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Tem valor único       | Verdadeiro                                                                  |
| É indexado             | Falso                                                                 |
| No Catálogo Global      | Falso                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------|
| ID do link                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Tem valor único       | Verdadeiro                                                                  |
| É indexado             | Falso                                                                 |
| No Catálogo Global      | Falso                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------|
| ID do link                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Tem valor único       | Verdadeiro                                                                  |
| É indexado             | Falso                                                                 |
| No Catálogo Global      | Falso                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------|
| ID do link                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Tem valor único       | Verdadeiro                                                                  |
| É indexado             | Falso                                                                 |
| No Catálogo Global      | Falso                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------|
| ID do link                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falso                                                                 |
| Tem valor único       | Verdadeiro                                                                  |
| É indexado             | Falso                                                                 |
| No Catálogo Global      | Falso                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





