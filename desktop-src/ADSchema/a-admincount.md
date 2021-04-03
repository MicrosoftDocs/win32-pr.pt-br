---
title: Admin-Count atributo
description: Indica que um determinado objeto teve suas ACLs alteradas para um valor mais seguro pelo sistema porque ele era um membro de um dos grupos administrativos (de forma direta ou transitiva).
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Esquema de Admin-Count do atributo AD
- Esquema de AD do atributo adminCount
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95b953aebaa39bb3fc3e4c9cf96632f32a37850
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645601"
---
# <a name="admin-count-attribute"></a>Admin-Count atributo

Indica que um determinado objeto teve suas ACLs alteradas para um valor mais seguro pelo sistema porque ele era um membro de um dos grupos administrativos (de forma direta ou transitiva).



| Entrada | Valor |
|-------------------|-----------------------------------------------------|
| CN                | Admin-Count                                         |
| LDAP-Display-Name | adminCount                                          |
| Tamanho              | 4 bytes                                             |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                    |
| Frequência de atualização  | Quando um objeto é adicionado a um grupo administrativo. |
| Attribute-Id      | 1.2.840.113556.1.4.150                              |
| System-ID-GUID    | bf967918-0de6-11d0-a285-00aa003049e2                |
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
| É de valor único       | True                                                                  |
| É indexado             | Falso                                                                 |
| No catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                          |
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
| É de valor único       | True                                                                  |
| É indexado             | Falso                                                                 |
| No catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                          |
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
| É de valor único       | True                                                                  |
| É indexado             | Falso                                                                 |
| No catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                          |
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
| É de valor único       | True                                                                  |
| É indexado             | Falso                                                                 |
| No catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                          |
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
| É de valor único       | True                                                                  |
| É indexado             | Falso                                                                 |
| No catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                          |
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
| É de valor único       | True                                                                  |
| É indexado             | Falso                                                                 |
| No catálogo global      | Falso                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





