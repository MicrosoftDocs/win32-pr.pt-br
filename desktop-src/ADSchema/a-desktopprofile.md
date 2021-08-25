---
title: Desktop-Profile atributo
description: O local do perfil de área de trabalho para um usuário ou grupo de usuários. Não usado.
ms.assetid: cbab8930-ce18-4b9c-ad60-5875bb23b822
ms.tgt_platform: multiple
keywords:
- Esquema de Desktop-Profile do atributo AD
- Esquema de AD do atributo desktopProfile
topic_type:
- apiref
api_name:
- Desktop-Profile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc9157730bce827c51a8705385afa61a92abc1d0d8f874844ac74d57fc31557
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925986"
---
# <a name="desktop-profile-attribute"></a>Desktop-Profile atributo

O local do perfil de área de trabalho para um usuário ou grupo de usuários. Não usado.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Desktop-Profile                             |
| LDAP-Display-Name | desktopProfile                              |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.346                      |
| System-ID-GUID    | eea65906-8ac6-11d0-afda-00c04fd930c9        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falso                                                                                                                                                                             |
| É de valor único       | Verdadeiro                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                             |
| No catálogo global      | Falso                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falso                                                                                                                                                                             |
| É de valor único       | Verdadeiro                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                             |
| No catálogo global      | Falso                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                 |
| MAPI-Id                | \-                                                                                                 |
| System-Only            | Falso                                                                                              |
| É de valor único       | Verdadeiro                                                                                               |
| É indexado             | Falso                                                                                              |
| No catálogo global      | Falso                                                                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                       |
| Range-Lower            | \-                                                                                                 |
| Range-Upper            | \-                                                                                                 |
| Search-Flags           | 0x00000000                                                                                         |
| System-Flags           | 0x00000010                                                                                         |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falso                                                                                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                             |
| No Catálogo Global      | Falso                                                                                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falso                                                                                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                             |
| No Catálogo Global      | Falso                                                                                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falso                                                                                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                             |
| No Catálogo Global      | Falso                                                                                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                                                                |
| System-Only            | Falso                                                                                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                             |
| No Catálogo Global      | Falso                                                                                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                      |
| Range-Lower            | \-                                                                                                                                                                                |
| Range-Upper            | \-                                                                                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                        |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





