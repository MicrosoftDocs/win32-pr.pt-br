---
title: Token-groups-no-GC-atributo aceitável
description: Esse atributo contém a lista de SIDs devido a uma operação de expansão de associação de grupo transitiva em um determinado usuário ou computador. Os grupos de tokens não poderão ser recuperados se um catálogo global não estiver presente para recuperar as associações inversas transitivas.
ms.assetid: 08718c69-6339-40dc-8486-a7cd72028ed1
ms.tgt_platform: multiple
keywords:
- Token-groups-no-GC-esquema de AD do atributo aceitável
- Esquema de AD do atributo tokenGroupsNoGCAcceptable
topic_type:
- apiref
api_name:
- Token-Groups-No-GC-Acceptable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc625d75409e266c90efa9a5a4cea5d7d3cf741c6e14f00faa8aa263ef88853
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835826"
---
# <a name="token-groups-no-gc-acceptable-attribute"></a>Token-groups-no-GC-atributo aceitável

Esse atributo contém a lista de SIDs devido a uma operação de expansão de associação de grupo transitiva em um determinado usuário ou computador. Os grupos de tokens não poderão ser recuperados se um catálogo global não estiver presente para recuperar as associações inversas transitivas.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Token-groups-no-GC-aceitável        |
| LDAP-Display-Name | tokenGroupsNoGCAcceptable            |
| Tamanho              | \-                                   |
| Privilégio de atualização  | O sistema define esse valor.          |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1303              |
| System-ID-GUID    | 040fc392-33df-11d2-98b2-0000f87a57d4 |
| Syntax            | [**Cadeia de caracteres (SID)**](s-string-sid.md)  |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



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



 

 





