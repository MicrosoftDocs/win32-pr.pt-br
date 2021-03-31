---
title: Time-Refresh atributo
description: Esse atributo tem o intervalo durante o qual um registro de recurso contido em uma zona integrada Active Directory deve ser atualizado para o servidor DNS. O intervalo padrão é de 7 dias.
ms.assetid: 9e473c29-7fcf-4d6d-8a7c-2791c7822c7d
ms.tgt_platform: multiple
keywords:
- Esquema de Time-Refresh do atributo AD
- Esquema de AD do atributo timerefresh
topic_type:
- apiref
api_name:
- Time-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bc360686b1692d2dbda1ee23ad6351e69d3afe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919552"
---
# <a name="time-refresh-attribute"></a>Time-Refresh atributo

Esse atributo tem o intervalo durante o qual um registro de recurso contido em uma zona integrada Active Directory deve ser atualizado para o servidor DNS. O intervalo padrão é de 7 dias.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Time-Refresh                         |
| LDAP-Display-Name | timerefresh                          |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.503               |
| System-ID-GUID    | ddac0cf1-af8f-11d0-afeb-00c04fd930c9 |
| Syntax            | [**Intervalo**](s-interval.md)       |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | Falso                                                                                                                         |
| É de valor único       | True                                                                                                                          |
| É indexado             | Falso                                                                                                                         |
| No catálogo global      | Falso                                                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| Classes usadas em        | [**Link-Track-OMT-entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | Falso                                                                                                                         |
| É de valor único       | True                                                                                                                          |
| É indexado             | Falso                                                                                                                         |
| No catálogo global      | Falso                                                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| Classes usadas em        | [**Link-Track-OMT-entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | Falso                                                                                                                         |
| É de valor único       | True                                                                                                                          |
| É indexado             | Falso                                                                                                                         |
| No catálogo global      | Falso                                                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| Classes usadas em        | [**Link-Track-OMT-entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | Falso                                                                                                                         |
| É de valor único       | True                                                                                                                          |
| É indexado             | Falso                                                                                                                         |
| No catálogo global      | Falso                                                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| Classes usadas em        | [**Link-Track-OMT-entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | Falso                                                                                                                         |
| É de valor único       | True                                                                                                                          |
| É indexado             | Falso                                                                                                                         |
| No catálogo global      | Falso                                                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| Classes usadas em        | [**Link-Track-OMT-entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | Falso                                                                                                                         |
| É de valor único       | True                                                                                                                          |
| É indexado             | Falso                                                                                                                         |
| No catálogo global      | Falso                                                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| Classes usadas em        | [**Link-Track-OMT-entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-entry**](c-linktrackvolentry.md)<br/> |



 

 





