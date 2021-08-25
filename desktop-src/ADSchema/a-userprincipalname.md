---
title: Atributo User-principal-Name
description: Esse atributo contém o UPN que é um nome de logon no estilo da Internet para um usuário baseado na RFC 822 padrão da Internet.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- Atributo User-principal-Name do AD Schema
- Esquema de atributo userPrincipalName do AD
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba8ac5196de660c4cff4b90801470581cc660491902ec5b48f0ced8337c498b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835281"
---
# <a name="user-principal-name-attribute"></a>Atributo User-principal-Name

Esse atributo contém o UPN que é um nome de logon no estilo da Internet para um usuário baseado na [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)padrão da Internet. O UPN é menor do que o nome distinto e mais fácil de lembrar. Por convenção, isso deve ser mapeado para o nome de email do usuário. O valor definido para esse atributo é igual ao comprimento da ID do usuário e do nome de domínio. Para obter mais informações sobre esse atributo, consulte [atributos de nomenclatura de usuário](/windows/desktop/AD/naming-properties).



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | User-Principal-Name                         |
| LDAP-Display-Name | userPrincipalName                           |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.      |
| Frequência de atualização  | Em teoria, isso nunca deve ser alterado.         |
| Attribute-Id      | 1.2.840.113556.1.4.656                      |
| System-ID-GUID    | 28630ebb-41d5-11d1-a9c1-0000f80367c1        |
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
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No catálogo global      | Verdadeiro                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No catálogo global      | Verdadeiro                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|--------------|
| ID do link                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Falso        |
| É de valor único       | Verdadeiro         |
| É indexado             | Verdadeiro         |
| No catálogo global      | Verdadeiro         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000001   |
| System-Flags           | 0x00000012   |
| Classes usadas em        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No catálogo global      | Verdadeiro                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No catálogo global      | Verdadeiro                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No catálogo global      | Verdadeiro                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No catálogo global      | Verdadeiro                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="remarks"></a>Comentários

No ADAM, esse atributo não precisa estar no formato padrão RFC 822 da Internet; pode ser um nome simples.

 

