---
title: Canonical-Name atributo
description: O nome do objeto em formato canônico.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Canonical-Name atributo AD Schema
- Esquema do AD do atributo canonicalName
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d88b31dd351e255c252188388bd1ba06b3a1c073163f5cd2cc9d2deac16a74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119307186"
---
# <a name="canonical-name-attribute"></a>Canonical-Name atributo

O nome do objeto em formato canônico. myserver2.fabrikam.com/users/jeffsmith é um exemplo de um nome diferenciado em formato canônico. Esse é um atributo construído. Os resultados retornados são idênticos aos retornados pela seguinte função do Active Directory: DsCrackNames(NULL, DS \_ NAME \_ FLAG \_ SYNTACTICAL \_ ONLY, DS \_ FQDN \_ 1779 \_ NAME, DS \_ \_ CANONICAL NAME, ...).

Para obter mais informações sobre formatos de nome, [**consulte DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Canonical-Name                              |
| Ldap-Display-Name | canonicalName                               |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.916                      |
| System-Id-Guid    | 9a7ad945-ca53-11d1-bbd0-0080c76670c0        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Falso                           |
| É indexado             | Falso                           |
| No Catálogo Global      | Falso                           |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Falso                           |
| É indexado             | Falso                           |
| No Catálogo Global      | Falso                           |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Falso                           |
| É indexado             | Falso                           |
| No Catálogo Global      | Falso                           |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Falso                           |
| É indexado             | Falso                           |
| No Catálogo Global      | Falso                           |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Falso                           |
| É indexado             | Falso                           |
| No Catálogo Global      | Falso                           |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Falso                           |
| É indexado             | Falso                           |
| No Catálogo Global      | Falso                           |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Falso                           |
| É indexado             | Falso                           |
| No Catálogo Global      | Falso                           |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



 

