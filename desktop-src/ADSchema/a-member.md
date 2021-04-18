---
title: Atributo de membro
description: A lista de usuários que pertencem ao grupo.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Atributo de membro esquema do AD
- atributo de membro esquema do AD
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105771756"
---
# <a name="member-attribute"></a>Atributo de membro

A lista de usuários que pertencem ao grupo.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Membro                                                |
| LDAP-Display-Name | member                                                |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | Administrador de domínio                                  |
| Frequência de atualização  | Cada vez que um usuário é adicionado ou removido de um grupo. |
| Attribute-Id      | 2.5.4.31                                              |
| System-ID-GUID    | bf9679c0-0de6-11d0-a285-00aa003049e2                  |
| Sintaxe            | [**Objeto (DS-DN)**](s-object-ds-dn.md)               |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | 2                                                                                       |
| MAPI-Id                | 0x8009                                                                                  |
| System-Only            | Falso                                                                                   |
| É de valor único       | Falso                                                                                   |
| É indexado             | Falso                                                                                   |
| No catálogo global      | True                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000012                                                                              |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Grupos de nomes**](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| É de valor único       | Falso                                                                                                                                 |
| É indexado             | Falso                                                                                                                                 |
| No catálogo global      | True                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Grupos de nomes**](c-groupofnames.md)<br/> [**Grupo MSMQ**](c-msmq-group.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | 2                                   |
| MAPI-Id                | 0x8009                              |
| System-Only            | Falso                               |
| É de valor único       | Falso                               |
| É indexado             | Falso                               |
| No catálogo global      | True                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000012                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| É de valor único       | Falso                                                                                                                                 |
| É indexado             | Falso                                                                                                                                 |
| No catálogo global      | True                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Grupos de nomes**](c-groupofnames.md)<br/> [**Grupo MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| É de valor único       | Falso                                                                                                                                 |
| É indexado             | Falso                                                                                                                                 |
| No catálogo global      | True                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Grupos de nomes**](c-groupofnames.md)<br/> [**Grupo MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| É de valor único       | Falso                                                                                                                                 |
| É indexado             | Falso                                                                                                                                 |
| No catálogo global      | True                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Grupos de nomes**](c-groupofnames.md)<br/> [**Grupo MSMQ**](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| É de valor único       | Falso                                                                                                                                 |
| É indexado             | Falso                                                                                                                                 |
| No catálogo global      | True                                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Grupos de nomes**](c-groupofnames.md)<br/> [**Grupo MSMQ**](c-msmq-group.md)<br/> |



 

 





