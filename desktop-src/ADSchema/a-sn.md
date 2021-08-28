---
title: Atributo sobrenome
description: Esse atributo contém a família ou o sobrenome de um usuário.
ms.assetid: d9d53c9f-4efa-47c4-aec4-518fb8a868b3
ms.tgt_platform: multiple
keywords:
- Atributo sobrenome do esquema do AD
- Esquema de AD do atributo SN
topic_type:
- apiref
api_name:
- Surname
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655557c23475dbc2d7f2e92fb48f5f71a8e818954bff83f5a47bb2470a26ca20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836186"
---
# <a name="surname-attribute"></a>Atributo sobrenome

Esse atributo contém a família ou o sobrenome de um usuário.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Sobrenome                                                                          |
| LDAP-Display-Name | sn                                                                               |
| Tamanho              | \-                                                                               |
| Privilégio de atualização  | Qualquer pessoa pode atualizar esse objeto com base na segurança do objeto que está sendo criado. |
| Frequência de atualização  | \-                                                                               |
| Attribute-Id      | 2.5.4.4                                                                          |
| System-ID-GUID    | bf967a41-0de6-11d0-a285-00aa003049e2                                             |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | 0x3A11                                |
| System-Only            | Falso                                 |
| É de valor único       | Verdadeiro                                  |
| É indexado             | Verdadeiro                                  |
| No catálogo global      | Verdadeiro                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 64                                    |
| Search-Flags           | 0x00000005                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Pessoa**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falso                                                                                         |
| É de valor único       | Verdadeiro                                                                                          |
| É indexado             | Verdadeiro                                                                                          |
| No catálogo global      | Verdadeiro                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falso                                                                                         |
| É de valor único       | Verdadeiro                                                                                          |
| É indexado             | Verdadeiro                                                                                          |
| No catálogo global      | Verdadeiro                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falso                                                                                         |
| É de valor único       | Verdadeiro                                                                                          |
| É indexado             | Verdadeiro                                                                                          |
| No catálogo global      | Verdadeiro                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falso                                                                                         |
| É de valor único       | Verdadeiro                                                                                          |
| É indexado             | Verdadeiro                                                                                          |
| No catálogo global      | Verdadeiro                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falso                                                                                         |
| É de valor único       | Verdadeiro                                                                                          |
| É indexado             | Verdadeiro                                                                                          |
| No catálogo global      | Verdadeiro                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**Pessoa**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





