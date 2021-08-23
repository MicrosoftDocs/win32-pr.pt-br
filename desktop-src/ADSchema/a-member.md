---
title: Atributo de membro
description: A lista de usuários que pertencem ao grupo.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo de membro
- atributo membro Esquema do AD
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1efe13163946cb5be6ca83b5d0c7f964b8d6b1981ce45f79166af01bd62e6c9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705506"
---
# <a name="member-attribute"></a>Atributo de membro

A lista de usuários que pertencem ao grupo.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Membro                                                |
| Ldap-Display-Name | member                                                |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | Administrador de domínio                                  |
| Frequência de atualização  | Cada vez que um usuário é adicionado ou removido de um grupo. |
| Attribute-Id      | 2.5.4.31                                              |
| System-Id-Guid    | bf9679c0-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)               |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
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
| Tem valor único       | Falso                                                                                   |
| É indexado             | Falso                                                                                   |
| No Catálogo Global      | Verdadeiro                                                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000012                                                                              |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Grupo de nomes**](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | Falso                                                                                                                                 |
| Tem valor único       | Falso                                                                                                                                 |
| É indexado             | Falso                                                                                                                                 |
| No Catálogo Global      | Verdadeiro                                                                                                                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Grupo de nomes**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | 2                                   |
| MAPI-Id                | 0x8009                              |
| System-Only            | Falso                               |
| Tem valor único       | Falso                               |
| É indexado             | Falso                               |
| No Catálogo Global      | Verdadeiro                                |
| Descritor de segurança NT | O:BAG: INADEQUADO: S:                        |
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
| No catálogo global      | Verdadeiro                                                                                                                                  |
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
| No catálogo global      | Verdadeiro                                                                                                                                  |
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
| No catálogo global      | Verdadeiro                                                                                                                                  |
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
| No Catálogo Global      | Verdadeiro                                                                                                                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Grupo de nomes**](c-groupofnames.md)<br/> [**MSMQ-Group**](c-msmq-group.md)<br/> |



 

 





