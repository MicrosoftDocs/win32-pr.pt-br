---
title: Atributo FRS-Service-Command
description: Uma cadeia de caracteres Unicode que um administrador pode definir para passar um comando para cada membro do conjunto de réplicas. Não usado.
ms.assetid: 9d8b6fd1-9040-42d2-816c-86fed4d54c41
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo FRS-Service-Command
- Esquema do AD do atributo fRSServiceCommand
topic_type:
- apiref
api_name:
- FRS-Service-Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9590e367c345995decff0901dd478cc5229176abbbcd708d6fc796ee3aa1bd69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961495"
---
# <a name="frs-service-command-attribute"></a>Atributo FRS-Service-Command

Uma cadeia de caracteres Unicode que um administrador pode definir para passar um comando para cada membro do conjunto de réplicas. Não usado.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | FRS-Service-Command                         |
| Ldap-Display-Name | fRSServiceCommand                           |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.500                      |
| System-Id-Guid    | ddac0cee-af8f-11d0-afeb-00c04fd930c9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                               |
| Tem valor único       | Verdadeiro                                                                                                                                                                |
| É indexado             | Falso                                                                                                                                                               |
| No Catálogo Global      | Falso                                                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                        |
| Range-Lower            | 0                                                                                                                                                                   |
| Range-Upper            | 512                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                                                          |
| Classes usadas em        | [**Membro NTFRS**](c-ntfrsmember.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**Assinante NTFRS**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                               |
| Tem valor único       | Verdadeiro                                                                                                                                                                |
| É indexado             | Falso                                                                                                                                                               |
| No Catálogo Global      | Falso                                                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                        |
| Range-Lower            | 0                                                                                                                                                                   |
| Range-Upper            | 512                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                                                          |
| Classes usadas em        | [**Membro NTFRS**](c-ntfrsmember.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**Assinante NTFRS**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                               |
| Tem valor único       | Verdadeiro                                                                                                                                                                |
| É indexado             | Falso                                                                                                                                                               |
| No Catálogo Global      | Falso                                                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                        |
| Range-Lower            | 0                                                                                                                                                                   |
| Range-Upper            | 512                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                                                          |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                               |
| É de valor único       | Verdadeiro                                                                                                                                                                |
| É indexado             | Falso                                                                                                                                                               |
| No catálogo global      | Falso                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                        |
| Range-Lower            | 0                                                                                                                                                                   |
| Range-Upper            | 512                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                                                          |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                               |
| É de valor único       | Verdadeiro                                                                                                                                                                |
| É indexado             | Falso                                                                                                                                                               |
| No catálogo global      | Falso                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                        |
| Range-Lower            | 0                                                                                                                                                                   |
| Range-Upper            | 512                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                                                          |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                               |
| É de valor único       | Verdadeiro                                                                                                                                                                |
| É indexado             | Falso                                                                                                                                                               |
| No catálogo global      | Falso                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                        |
| Range-Lower            | 0                                                                                                                                                                   |
| Range-Upper            | 512                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                                                          |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> |



 

 





