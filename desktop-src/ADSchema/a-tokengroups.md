---
title: Token-Groups atributo
description: Um atributo computado que contém a lista de SIDs devido a uma operação de expansão de associação de grupo transitiva em um determinado usuário ou computador. Os grupos de tokens não poderão ser recuperados se nenhum catálogo global estiver presente para recuperar as associações inversas transitivas.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Esquema de Token-Groups do atributo AD
- Esquema de AD do atributo tokenGroups
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b8971f9ba5baead73b7704760dcc86430f5ce1a318ac6bcbd9dfaf4125a21af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022064"
---
# <a name="token-groups-attribute"></a>Token-Groups atributo

Um atributo computado que contém a lista de SIDs devido a uma operação de expansão de associação de grupo transitiva em um determinado usuário ou computador. Os grupos de tokens não poderão ser recuperados se nenhum catálogo global estiver presente para recuperar as associações inversas transitivas.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Token-Groups                         |
| LDAP-Display-Name | tokenGroups                          |
| Tamanho              | \-                                   |
| Privilégio de atualização  | Esse valor é definido pelo sistema.     |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1301              |
| System-ID-GUID    | b7c69e6d-2cc7-11d2-854e-00a0c983f608 |
| Syntax            | [**Cadeia de caracteres (SID)**](s-string-sid.md)  |



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
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Falso                                                        |
| É indexado             | Falso                                                        |
| No catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Falso                                                        |
| É indexado             | Falso                                                        |
| No catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Falso                                                        |
| É indexado             | Falso                                                        |
| No catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Tem valor único       | Falso                                                        |
| É indexado             | Falso                                                        |
| No Catálogo Global      | Falso                                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Tem valor único       | Falso                                                        |
| É indexado             | Falso                                                        |
| No Catálogo Global      | Falso                                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Tem valor único       | Falso                                                        |
| É indexado             | Falso                                                        |
| No Catálogo Global      | Falso                                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Tem valor único       | Falso                                                        |
| É indexado             | Falso                                                        |
| No Catálogo Global      | Falso                                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> |



 

 





