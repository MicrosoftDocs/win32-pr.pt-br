---
title: Unicode-Pwd atributo
description: a senha do usuário em um formato de Windows NT unidirecional (OWF). Windows 2000 usa o Windows NT OWF. Essa propriedade é usada somente pelo sistema operacional. Observe que você não pode derivar a senha de limpeza do formulário OWF da senha.
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- Esquema de Unicode-Pwd do atributo AD
- Esquema de AD do atributo unicodePwd
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e21929cf41b58688f768ada0b608ca3ef0892a4a54043c30f5cac2d5a72258b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681083"
---
# <a name="unicode-pwd-attribute"></a>Unicode-Pwd atributo

a senha do usuário em um formato de Windows NT unidirecional (OWF). Windows 2000 usa o Windows NT OWF. Essa propriedade é usada somente pelo sistema operacional. Observe que você não pode derivar a senha de limpeza do formulário OWF da senha.



| Entrada | Valor |
|-------------------|------------------------------------------------------------------------------|
| CN                | Unicode-Pwd                                                                  |
| LDAP-Display-Name | unicodePwd                                                                   |
| Tamanho              | \-                                                                           |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                       |
| Frequência de atualização  | Quando o registro do usuário é criado e sempre que a senha precisa ser alterada. |
| Attribute-Id      | 1.2.840.113556.1.4.90                                                        |
| System-ID-GUID    | bf9679e1-0de6-11d0-a285-00aa003049e2                                         |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md)                        |



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
| É indexado             | Falso                             |
| No catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------|
| ID do link                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| É de valor único       | Verdadeiro                                                              |
| É indexado             | Falso                                                             |
| No catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classes usadas em        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



 

 





