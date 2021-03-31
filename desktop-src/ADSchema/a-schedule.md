---
title: Atributo de agendamento
description: Um BLOB de agendamento, conforme definido pelo serviço de trabalho do Windows NT. Usado pela replicação.
ms.assetid: 5eb6409d-3fb5-4368-8b7f-ce19567b7260
ms.tgt_platform: multiple
keywords:
- Esquema de atributo de agendamento do AD
- Esquema de atributo de agendamento do AD
topic_type:
- apiref
api_name:
- Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abf53e86f77ecffc872d8b007e32b1f964ae244e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086846"
---
# <a name="schedule-attribute"></a>Atributo de agendamento

Um BLOB de agendamento, conforme definido pelo serviço de trabalho do Windows NT. Usado pela replicação.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Agenda                                              |
| LDAP-Display-Name | schedule                                              |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | \-                                                    |
| Frequência de atualização  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.211                                |
| System-ID-GUID    | dd712224-10e4-11d0-a05f-00aa006c33ed                  |
| Sintaxe            | [**Objeto (link de réplica)**](s-object-replica-link.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| É de valor único       | True                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| É de valor único       | True                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                            |
| MAPI-Id                | \-                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                         |
| É de valor único       | True                                                                                                                                                          |
| É indexado             | Falso                                                                                                                                                         |
| No catálogo global      | Falso                                                                                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                  |
| Range-Lower            | \-                                                                                                                                                            |
| Range-Upper            | \-                                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                                                    |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| É de valor único       | True                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| É de valor único       | True                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| É de valor único       | True                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| É de valor único       | True                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS – configurações de site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



 

 





