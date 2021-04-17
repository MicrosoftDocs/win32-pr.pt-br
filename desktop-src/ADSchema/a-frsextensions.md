---
title: FRS-Extensions atributo
description: Dados binários usados pela replicação de arquivo.
ms.assetid: 8384f097-533c-49b6-898b-f4120dcfc3fd
ms.tgt_platform: multiple
keywords:
- Esquema de FRS-Extensions do atributo AD
- Esquema de AD do atributo fRSExtensions
topic_type:
- apiref
api_name:
- FRS-Extensions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010677958b7d03841ca465db7bfd17e38aa4e003
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756061"
---
# <a name="frs-extensions-attribute"></a>FRS-Extensions atributo

Dados binários usados pela replicação de arquivo.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | FRS-Extensions                                        |
| LDAP-Display-Name | fRSExtensions                                         |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                      |
| Frequência de atualização  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.536                                |
| System-ID-GUID    | 52458020-ca6a-11D0-afff-0000f80367c1                  |
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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| É de valor único       | True                                                                                                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 65536                                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-configurações**](c-ntfrssettings.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**NTFRS-assinaturas**](c-ntfrssubscriptions.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| É de valor único       | True                                                                                                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 65536                                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-configurações**](c-ntfrssettings.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**NTFRS-assinaturas**](c-ntfrssubscriptions.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| É de valor único       | True                                                                                                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 65536                                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-configurações**](c-ntfrssettings.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**NTFRS-assinaturas**](c-ntfrssubscriptions.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| É de valor único       | True                                                                                                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 65536                                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-configurações**](c-ntfrssettings.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**NTFRS-assinaturas**](c-ntfrssubscriptions.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| É de valor único       | True                                                                                                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 65536                                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-configurações**](c-ntfrssettings.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**NTFRS-assinaturas**](c-ntfrssubscriptions.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| É de valor único       | True                                                                                                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 65536                                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> [**NTFRS-configurações**](c-ntfrssettings.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> [**NTFRS-assinaturas**](c-ntfrssubscriptions.md)<br/> |



 

 





