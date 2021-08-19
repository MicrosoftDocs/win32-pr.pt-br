---
title: Atributo de agendamento
description: um BLOB de agendamento, conforme definido pelo serviço de trabalho Windows NT. Usado pela replicação.
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
ms.openlocfilehash: 6b65ff20b9eaba0c8429f5fec164e44a3e4b842e82bfddcca61461f6832f55d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022214"
---
# <a name="schedule-attribute"></a>Atributo de agendamento

um BLOB de agendamento, conforme definido pelo serviço de trabalho Windows NT. Usado pela replicação.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Agenda                                              |
| LDAP-Display-Name | schedule                                              |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | \-                                                    |
| Frequência de atualização  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.211                                |
| System-ID-GUID    | dd712224-10e4-11d0-a05f-00aa006c33ed                  |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md) |



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
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-Configurações de Site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-Configurações de Site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                            |
| MAPI-Id                | \-                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                         |
| É de valor único       | Verdadeiro                                                                                                                                                          |
| É indexado             | Falso                                                                                                                                                         |
| No catálogo global      | Falso                                                                                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                  |
| Range-Lower            | \-                                                                                                                                                            |
| Range-Upper            | \-                                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                                                    |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-Configurações de Site**](c-ntdssitesettings.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-Configurações de Site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-Configurações de Site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-Configurações de Site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> [**NTDS-Configurações de Site**](c-ntdssitesettings.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**Link de site**](c-sitelink.md)<br/> |



 

 





