---
title: Coll-atributo de período de lixo
description: Esse atributo está localizado no serviço de diretório CN, CN Windows NT, serviços CN, configuração CN,... objeto. Ele representa o tempo, em horas, entre as execuções de coleta de lixo DS.
ms.assetid: 982a75f9-04b5-489e-99b3-a9fd3fb280c8
ms.tgt_platform: multiple
keywords:
- Coll-esquema de AD do atributo de período de lixo
- Esquema de AD do atributo garbageCollPeriod
topic_type:
- apiref
api_name:
- Garbage-Coll-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64890df97cf4c131ad0dcdbed8cb80bf20b66a83
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755257"
---
# <a name="garbage-coll-period-attribute"></a>Coll-atributo de período de lixo

Esse atributo está localizado em CN = serviço de diretório, CN = Windows NT, CN = Services, CN = Configuration,... objeto. Ele representa o tempo, em horas, entre as execuções de coleta de lixo DS.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Lixo-Coll-period                  |
| LDAP-Display-Name | garbageCollPeriod                    |
| Tamanho              | 4 bytes                              |
| Privilégio de atualização  | Administrador de domínio                 |
| Frequência de atualização  | Muito raro.                           |
| Attribute-Id      | 1.2.840.113556.1.2.301               |
| System-ID-GUID    | 5fd424a1-1262-11d0-a060-00aa006c33ed |
| Syntax            | [**Enumeração**](s-enumeration.md) |



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
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Falso                                                                                                 |
| É de valor único       | True                                                                                                  |
| É indexado             | Falso                                                                                                 |
| No catálogo global      | Falso                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes usadas em        | [**Destinatário de email**](c-mailrecipient.md)<br/> [**NTDS-serviço**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Falso                                                                                                 |
| É de valor único       | True                                                                                                  |
| É indexado             | Falso                                                                                                 |
| No catálogo global      | Falso                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes usadas em        | [**Destinatário de email**](c-mailrecipient.md)<br/> [**NTDS-serviço**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | 0x80AF                                           |
| System-Only            | Falso                                            |
| É de valor único       | True                                             |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-serviço**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Falso                                                                                                 |
| É de valor único       | True                                                                                                  |
| É indexado             | Falso                                                                                                 |
| No catálogo global      | Falso                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes usadas em        | [**Destinatário de email**](c-mailrecipient.md)<br/> [**NTDS-serviço**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Falso                                                                                                 |
| É de valor único       | True                                                                                                  |
| É indexado             | Falso                                                                                                 |
| No catálogo global      | Falso                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes usadas em        | [**Destinatário de email**](c-mailrecipient.md)<br/> [**NTDS-serviço**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Falso                                                                                                 |
| É de valor único       | True                                                                                                  |
| É indexado             | Falso                                                                                                 |
| No catálogo global      | Falso                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes usadas em        | [**Destinatário de email**](c-mailrecipient.md)<br/> [**NTDS-serviço**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Falso                                                                                                 |
| É de valor único       | True                                                                                                  |
| É indexado             | Falso                                                                                                 |
| No catálogo global      | Falso                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes usadas em        | [**Destinatário de email**](c-mailrecipient.md)<br/> [**NTDS-serviço**](c-ntdsservice.md)<br/> |



 

 





