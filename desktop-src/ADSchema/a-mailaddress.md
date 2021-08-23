---
title: Atributo SMTP-Mail-Address
description: Atributo de endereço de email genérico. Usado na caixa como um atributo opcional de objetos de servidor, em que ele é consumido pela replicação DS baseada em email (se os computadores estão configurados).
ms.assetid: 54fd710c-d140-4d46-9db3-0c72fb5fb08c
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo SMTP-Mail-Address
- Esquema do AD do atributo mailAddress
topic_type:
- apiref
api_name:
- SMTP-Mail-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6ffc0e535b97994d3ef6ed451516eafa68c59940468f31bd88ffab84a878dbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301286"
---
# <a name="smtp-mail-address-attribute"></a>Atributo SMTP-Mail-Address

Atributo de endereço de email genérico. Usado na caixa como um atributo opcional de objetos de servidor, em que ele é consumido pela replicação DS baseada em email (se os computadores estão configurados).



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Endereço de email SMTP                           |
| Ldap-Display-Name | Mailaddress                                 |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio                        |
| Frequência de atualização  | Quase nunca                                |
| Attribute-Id      | 1.2.840.113556.1.4.786                      |
| System-Id-Guid    | 26d9736f-6070-11d1-a9c6-0000f80367c1        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| Tem valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No Catálogo Global      | Falso                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| Tem valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No Catálogo Global      | Falso                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Servidor**](c-server.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| Tem valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No Catálogo Global      | Falso                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| É de valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No catálogo global      | Falso                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| É de valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No catálogo global      | Falso                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| É de valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No catálogo global      | Falso                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| É de valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No catálogo global      | Falso                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Servidor**](c-server.md)<br/> |



 

 





