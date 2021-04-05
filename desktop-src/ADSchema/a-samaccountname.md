---
title: SAM-atributo de nome de conta
description: O nome de logon usado para dar suporte a clientes e servidores que executam versões anteriores do sistema operacional, como o Windows NT 4,0, o Windows 95, o Windows 98 e o LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- SAM-Account-Name atributo AD Schema
- Esquema do atributo do sAMAccountName
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825278"
---
# <a name="sam-account-name-attribute"></a>SAM-atributo de nome de conta

O nome de logon usado para dar suporte a clientes e servidores que executam versões anteriores do sistema operacional, como o Windows NT 4,0, o Windows 95, o Windows 98 e o LAN Manager.

Esse atributo deve ter 20 caracteres ou menos para dar suporte a clientes anteriores e não pode conter nenhum destes caracteres:

-   "/ \\ \[ \] : ; \| = , + \* ? < >



| Entrada | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| CN                | SAM-Account-Name                                                                         |
| LDAP-Display-Name | sAMAccountName                                                                           |
| Tamanho              | 20 caracteres ou menos.                                                                   |
| Privilégio de atualização  | Administrador de domínio                                                                     |
| Frequência de atualização  | Esse valor deve ser atribuído quando o registro de conta é criado e não deve ser alterado. |
| Attribute-Id      | 1.2.840.113556.1.4.221                                                                   |
| System-ID-GUID    | 3e0abfd0-126a-11d0-a060-00aa006c33ed                                                     |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                              |



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
| É de valor único       | True                                                         |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | True                                                         |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | True                                                         |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | True                                                         |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | True                                                         |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | True                                                         |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



 

 





