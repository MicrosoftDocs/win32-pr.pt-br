---
title: Security-Identifier atributo
description: Um valor exclusivo de comprimento variável usado para identificar uma conta de usuário, conta de grupo ou sessão de logon à qual uma ACE se aplica.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Security-Identifier atributo AD Schema
- esquema do AD do atributo securityIdentifier
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f15449127dd11e7e0ebfef9f63d8e79470ed662377cbdd1929ed072b2502dae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836866"
---
# <a name="security-identifier-attribute"></a>Security-Identifier atributo

Um valor exclusivo de comprimento variável usado para identificar uma conta de usuário, conta de grupo ou sessão de logon à qual uma ACE se aplica.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Security-Identifier                  |
| Ldap-Display-Name | Securityidentifier                   |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.121               |
| System-Id-Guid    | bf967a2f-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**String(Sid)**](s-string-sid.md)  |



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
| Tem valor único       | Verdadeiro                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No Catálogo Global      | Falso                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No Catálogo Global      | Verdadeiro                                                                                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No Catálogo Global      | Verdadeiro                                                                                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No Catálogo Global      | Verdadeiro                                                                                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No Catálogo Global      | Verdadeiro                                                                                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No Catálogo Global      | Verdadeiro                                                                                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> [**Domínio confiável**](c-trusteddomain.md)<br/> |



 

 





