---
title: Atributo ms-DS-Logon-Time-Sync-Interval
description: Esse atributo controla a granularidade, em dias, com a qual a hora do último logon de um usuário ou computador, registrada no atributo lastLogonTimestamp, é replicada para todos os DCs em um domínio.
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo ms-DS-Logon-Time-Sync-Interval
- Esquema do AD do atributo msDS-LogonTimeSyncInterval
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa27a1d6281eda7eea9f88a11c4ca6632422a1cfd9f0cb471aab513018c56150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118684630"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a>Atributo ms-DS-Logon-Time-Sync-Interval

Esse atributo controla a granularidade, em dias, com a qual a hora do último logon de um usuário ou computador, registrada no atributo lastLogonTimestamp, é replicada para todos os DCs em um domínio.



| Entrada | Valor |
|-------------------|------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-Logon-Time-Sync-Interval                                                                             |
| Ldap-Display-Name | msDS-LogonTimeSyncInterval                                                                                 |
| Tamanho              | 4 bytes                                                                                                    |
| Privilégio de atualização  | Administrador de domínio                                                                                       |
| Frequência de atualização  | Raramente, como essa é uma configuração de política, ela é atualizada somente quando uma alteração na política em todo o domínio é desejada. |
| Attribute-Id      | 1.2.840.113556.1.4.1784                                                                                    |
| System-Id-Guid    | ad7940f8-e43a-4a42-83bc-d688e59ea605                                                                       |
| Syntax            | [**Enumeração**](s-enumeration.md)                                                                       |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sam-domínio**](c-samdomain.md)<br/> |



 

 





