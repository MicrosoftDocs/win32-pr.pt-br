---
title: Home-Directory atributo
description: O diretório base da conta.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Esquema de Home-Directory do atributo AD
- Esquema de AD do atributo homeDirectory
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645487"
---
# <a name="home-directory-attribute"></a>Home-Directory atributo

O diretório base da conta. Se [**homeDrive**](a-homedrive.md) for definido e especificar uma letra de unidade, **HomeDirectory** deverá ser um caminho UNC. Caso contrário, **HomeDirectory** é um caminho local totalmente qualificado, incluindo a letra da unidade (por exemplo, *DriveLetter ***: \\** pasta _do diretório_* _\\_ * ). Esse valor pode ser uma cadeia de caracteres nula.



| Entrada | Valor |
|-------------------|------------------------------------------------------------------------------------|
| CN                | Home-Directory                                                                     |
| LDAP-Display-Name | homeDirectory                                                                      |
| Tamanho              | \-                                                                                 |
| Privilégio de atualização  | Administrador de domínio                                                               |
| Frequência de atualização  | Quando o registro do usuário é criado e sempre que o diretório base precisa ser alterado. |
| Attribute-Id      | 1.2.840.113556.1.4.44                                                              |
| System-ID-GUID    | bf967985-0de6-11d0-a285-00aa003049e2                                               |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                        |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | True                              |
| É indexado             | Falso                             |
| No catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | True                              |
| É indexado             | Falso                             |
| No catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| É de valor único       | True                                                                                |
| É indexado             | Falso                                                                               |
| No catálogo global      | Falso                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| É de valor único       | True                                                                                |
| É indexado             | Falso                                                                               |
| No catálogo global      | Falso                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| É de valor único       | True                                                                                |
| É indexado             | Falso                                                                               |
| No catálogo global      | Falso                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| É de valor único       | True                                                                                |
| É indexado             | Falso                                                                               |
| No catálogo global      | Falso                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**homeDrive**](a-homedrive.md)
</dt> </dl>

 

 





