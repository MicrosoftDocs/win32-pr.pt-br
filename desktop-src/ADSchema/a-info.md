---
title: Atributo de comentário
description: Os comentários do usuário. Essa cadeia de caracteres pode ser uma cadeia de caracteres nula.
ms.assetid: c57493b3-a42a-49ad-8f8c-0afadbb3ba09
ms.tgt_platform: multiple
keywords:
- Atributo de comentário do esquema do AD
- atributo de informações esquema do AD
topic_type:
- apiref
api_name:
- Comment
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739203abd9cfbeb383ca4365bdc8b19135010830c4c23305aff18d86d9b03be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925486"
---
# <a name="comment-attribute-ad-schema"></a>Atributo de comentário (esquema do AD)

Os comentários do usuário. Essa cadeia de caracteres pode ser uma cadeia de caracteres nula.



| Entrada | Valor |
|-------------------|--------------------------------------------------------------------------|
| CN                | Comentário                                                                  |
| LDAP-Display-Name | informações                                                                     |
| Tamanho              | \-                                                                       |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                   |
| Frequência de atualização  | Sempre que o usuário ou administrador precisar adicionar comentários na conta. |
| Attribute-Id      | 1.2.840.113556.1.2.81                                                    |
| System-ID-GUID    | bf96793e-0de6-11d0-a285-00aa003049e2                                     |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                              |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Destinatário de email**](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Destinatário de email**](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Destinatário do email**](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No Catálogo Global      | Falso                                                |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Destinatário do email**](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No Catálogo Global      | Falso                                                |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Destinatário do email**](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | 0x3004                                               |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No Catálogo Global      | Falso                                                |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Destinatário do email**](c-mailrecipient.md)<br/> |



 

 





