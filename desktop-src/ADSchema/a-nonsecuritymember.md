---
title: Atributo não membro de segurança
description: Membros não de segurança de um grupo. Usado para Exchange listas de distribuição.
ms.assetid: 0db135e4-dcba-4afb-a174-3c7b2b40688e
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo não membro de segurança
- Esquema do AD do atributo nonSecurityMember
topic_type:
- apiref
api_name:
- Non-Security-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba59e37e4d4be5549e9ab5f36747f1cfd0046a9fb01ca91e2a9e79f353f148a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648376"
---
# <a name="non-security-member-attribute"></a>Atributo não membro de segurança

Membros não de segurança de um grupo. Usado para Exchange listas de distribuição.



| Entrada | Valor |
|-------------------|--------------------------------------------------|
| CN                | Não membro de segurança                              |
| Ldap-Display-Name | nonSecurityMember                                |
| Tamanho              | \-                                               |
| Privilégio de atualização  | Administrador de domínio                             |
| Frequência de atualização  | Sempre que um usuário é adicionado ou removido da DL. |
| Attribute-Id      | 1.2.840.113556.1.4.530                           |
| System-Id-Guid    | 52458018-ca6a-11d0-afff-0000f80367c1             |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)          |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Falso                               |
| Tem valor único       | Falso                               |
| É indexado             | Falso                               |
| No Catálogo Global      | Falso                               |
| Descritor de segurança NT | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Falso                               |
| Tem valor único       | Falso                               |
| É indexado             | Falso                               |
| No Catálogo Global      | Falso                               |
| Descritor de segurança NT | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Falso                               |
| Tem valor único       | Falso                               |
| É indexado             | Falso                               |
| No Catálogo Global      | Falso                               |
| Descritor de segurança NT | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Falso                               |
| É de valor único       | Falso                               |
| É indexado             | Falso                               |
| No catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Falso                               |
| É de valor único       | Falso                               |
| É indexado             | Falso                               |
| No catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | 50                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Falso                               |
| É de valor único       | Falso                               |
| É indexado             | Falso                               |
| No catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000010                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



 

 





