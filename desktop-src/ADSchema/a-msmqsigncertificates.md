---
title: Atributo MSMQ-Sign-Certificates
description: Esse atributo contém um número de certificados. Um usuário pode gerar um certificado por computador. Para cada certificado, também mantemos um resumo.
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- Atributo AD do MSMQ-Sign-Certificates
- Esquema de AD do atributo mSMQSignCertificates
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ee82a5a2bf64acc315dfb535ca6897261ef0cb26f5e249a8c8593cc492b53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081740"
---
# <a name="msmq-sign-certificates-attribute"></a>Atributo MSMQ-Sign-Certificates

Esse atributo contém um número de certificados. Um usuário pode gerar um certificado por computador. Para cada certificado, também mantemos um resumo.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| CN                | MSMQ-assinar certificados                                                                 |
| LDAP-Display-Name | mSMQSignCertificates                                                                   |
| Tamanho              | O tipo de atributo é um BLOB, o tamanho não é limitado e os dados são mantidos em nosso próprio formato. |
| Privilégio de atualização  | \-                                                                                     |
| Frequência de atualização  | \-                                                                                     |
| Attribute-Id      | 1.2.840.113556.1.4.947                                                                 |
| System-ID-GUID    | 9a0dc33b-c100-11d1-bbc5-0080c76670c0                                                   |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md)                                  |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Falso                                                                                         |
| É de valor único       | Verdadeiro                                                                                          |
| É indexado             | Falso                                                                                         |
| No catálogo global      | Verdadeiro                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Falso                                                                                         |
| É de valor único       | Verdadeiro                                                                                          |
| É indexado             | Falso                                                                                         |
| No catálogo global      | Verdadeiro                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Falso                                                                                         |
| É de valor único       | Verdadeiro                                                                                          |
| É indexado             | Falso                                                                                         |
| No catálogo global      | Verdadeiro                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Falso                                                                                         |
| Tem valor único       | Verdadeiro                                                                                          |
| É indexado             | Falso                                                                                         |
| No Catálogo Global      | Verdadeiro                                                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Falso                                                                                         |
| Tem valor único       | Verdadeiro                                                                                          |
| É indexado             | Falso                                                                                         |
| No Catálogo Global      | Verdadeiro                                                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Falso                                                                                         |
| Tem valor único       | Verdadeiro                                                                                          |
| É indexado             | Falso                                                                                         |
| No Catálogo Global      | Verdadeiro                                                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





