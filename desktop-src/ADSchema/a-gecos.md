---
title: Atributo gecos
description: Contém as informações armazenadas no campo GECOS.
ms.assetid: 017884a5-697f-481d-b119-075deb96fd6f
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo gecos
topic_type:
- apiref
api_name:
- gecos
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad96c4e73808608a6175e42ba81b5115b6a84fe9daf2048b4d3d0fefdf8eb05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961365"
---
# <a name="gecos-attribute"></a>Atributo gecos

Contém as informações armazenadas no campo GECOS.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Gecos                                |
| Ldap-Display-Name | Gecos                                |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.3.6.1.1.1.1.2                      |
| System-Id-Guid    | a3e03f1f-1d55-4253-a0af-30c2a784e46e |
| Syntax            | [**String(IA5)**](s-string-ia5.md)  |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------|
| ID do link                | \-                                                |
| MAPI-Id                | \-                                                |
| System-Only            | Falso                                             |
| Tem valor único       | Verdadeiro                                              |
| É indexado             | Falso                                             |
| No Catálogo Global      | Falso                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                      |
| Range-Lower            | \-                                                |
| Range-Upper            | \-                                                |
| Search-Flags           | 0x00000000                                        |
| System-Flags           | 0x00000000                                        |
| Classes usadas em        | [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------|
| ID do link                | \-                                                |
| MAPI-Id                | \-                                                |
| System-Only            | Falso                                             |
| Tem valor único       | Verdadeiro                                              |
| É indexado             | Falso                                             |
| No Catálogo Global      | Falso                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                      |
| Range-Lower            | \-                                                |
| Range-Upper            | \-                                                |
| Search-Flags           | 0x00000000                                        |
| System-Flags           | 0x00000000                                        |
| Classes usadas em        | [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------|
| ID do link                | \-                                                |
| MAPI-Id                | \-                                                |
| System-Only            | Falso                                             |
| Tem valor único       | Verdadeiro                                              |
| É indexado             | Falso                                             |
| No Catálogo Global      | Falso                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                      |
| Range-Lower            | \-                                                |
| Range-Upper            | \-                                                |
| Search-Flags           | 0x00000000                                        |
| System-Flags           | 0x00000000                                        |
| Classes usadas em        | [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------|
| ID do link                | \-                                                |
| MAPI-Id                | \-                                                |
| System-Only            | Falso                                             |
| É de valor único       | Verdadeiro                                              |
| É indexado             | Falso                                             |
| No catálogo global      | Falso                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                      |
| Range-Lower            | \-                                                |
| Range-Upper            | \-                                                |
| Search-Flags           | 0x00000000                                        |
| System-Flags           | 0x00000000                                        |
| Classes usadas em        | [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="remarks"></a>Comentários

O campo GECOS é um campo opcional que é usado para armazenar várias partes de informações, como o nome completo do usuário.

## <a name="see-also"></a>Confira também

<dl> <dt>

[RFC 2307](https://www.ietf.org/rfc/rfc2307.txt)
</dt> </dl>

 

 





