---
title: Security-Identifier atributo
description: Um valor exclusivo de comprimento variável usado para identificar uma conta de usuário, uma conta de grupo ou uma sessão de logon à qual uma ACE se aplica.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Esquema de Security-Identifier do atributo AD
- Esquema de AD do atributo securityIdentifier
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd921d0bcba08c2174475007476add8e8787456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645407"
---
# <a name="security-identifier-attribute"></a>Security-Identifier atributo

Um valor exclusivo de comprimento variável usado para identificar uma conta de usuário, uma conta de grupo ou uma sessão de logon à qual uma ACE se aplica.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Security-Identifier                  |
| LDAP-Display-Name | securityIdentifier                   |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.121               |
| System-ID-GUID    | bf967a2f-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| É de valor único       | True                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No catálogo global      | Falso                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| É de valor único       | True                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No catálogo global      | True                                                                                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| É de valor único       | True                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No catálogo global      | True                                                                                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| É de valor único       | True                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No catálogo global      | True                                                                                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| É de valor único       | True                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No catálogo global      | True                                                                                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| É de valor único       | True                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No catálogo global      | True                                                                                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



 

 





