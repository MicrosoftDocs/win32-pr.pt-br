---
title: Atributo FRS-Fault-Condition
description: A condição de falha para um membro.
ms.assetid: 2b0472bf-d6cb-4471-b1ca-93e2aedf6572
ms.tgt_platform: multiple
keywords:
- FRS-falha-esquema de atributo do AD
- Esquema de AD do atributo fRSFaultCondition
topic_type:
- apiref
api_name:
- FRS-Fault-Condition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fb968ed2d09da3a47348f8672960dd97d2d67030e1addcbbda6c7acceae49c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961505"
---
# <a name="frs-fault-condition-attribute"></a>Atributo FRS-Fault-Condition

A condição de falha para um membro.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | FRS-falha-condição                         |
| LDAP-Display-Name | fRSFaultCondition                           |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.491                      |
| System-ID-GUID    | 1be8f178-a9ff-11d0-afe2-00c04fd930c9        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | Falso                                                    |
| É de valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 16                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | Falso                                                    |
| É de valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 16                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | Falso                                                    |
| É de valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 16                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Assinante NTFRS**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | Falso                                                    |
| Tem valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 16                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Assinante NTFRS**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | Falso                                                    |
| Tem valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 16                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Assinante NTFRS**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | Falso                                                    |
| Tem valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 16                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Assinante NTFRS**](c-ntfrssubscriber.md)<br/> |



 

 





