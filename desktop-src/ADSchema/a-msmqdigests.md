---
title: MSMQ-Digests atributo
description: Uma matriz de resumos dos certificados correspondentes no atributo mSMQ-Sign-Certificates. Eles são usados para mapear um resumo em um certificado.
ms.assetid: a9b03edd-1506-4f2d-afe1-7d953977f6fa
ms.tgt_platform: multiple
keywords:
- Esquema de MSMQ-Digests do atributo AD
- Esquema de AD do atributo mSMQDigests
topic_type:
- apiref
api_name:
- MSMQ-Digests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d51c607b1d99af0aed46f259513f4bcf790844
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755891"
---
# <a name="msmq-digests-attribute"></a>MSMQ-Digests atributo

Uma matriz de resumos dos certificados correspondentes no atributo mSMQ-Sign-Certificates. Eles são usados para mapear um resumo em um certificado.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | MSMQ-Digests                                          |
| LDAP-Display-Name | mSMQDigests                                           |
| Tamanho              | Cada resumo é 16 bytes.                              |
| Privilégio de atualização  | \-                                                    |
| Frequência de atualização  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.948                                |
| System-ID-GUID    | 9a0dc33c-c100-11d1-bbc5-0080c76670c0                  |
| Sintaxe            | [**Objeto (link de réplica)**](s-object-replica-link.md) |



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
| É de valor único       | Falso                                                                                         |
| É indexado             | True                                                                                          |
| No catálogo global      | True                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Falso                                                                                         |
| É de valor único       | Falso                                                                                         |
| É indexado             | True                                                                                          |
| No catálogo global      | True                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Falso                                                                                         |
| É de valor único       | Falso                                                                                         |
| É indexado             | True                                                                                          |
| No catálogo global      | True                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Falso                                                                                         |
| É de valor único       | Falso                                                                                         |
| É indexado             | True                                                                                          |
| No catálogo global      | True                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Falso                                                                                         |
| É de valor único       | Falso                                                                                         |
| É indexado             | True                                                                                          |
| No catálogo global      | True                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Falso                                                                                         |
| É de valor único       | Falso                                                                                         |
| É indexado             | True                                                                                          |
| No catálogo global      | True                                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes usadas em        | [**MSMQ-migrado-usuário**](c-msmqmigrateduser.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





