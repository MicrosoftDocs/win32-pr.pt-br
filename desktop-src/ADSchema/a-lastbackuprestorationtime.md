---
title: Atributo Last-Backup-Restoration-Time
description: Quando ocorreu a última restauração do sistema.
ms.assetid: 44850c16-3f17-4883-9a54-3e82ca7d63da
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Last-Backup-Restoration-Time
- Esquema do AD do atributo lastBackupRestorationTime
topic_type:
- apiref
api_name:
- Last-Backup-Restoration-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507d19c03dada2430eee9eab5cfdc76cc043a5bc7385fdc9e17925a5dbd6e78c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804396"
---
# <a name="last-backup-restoration-time-attribute"></a>Atributo Last-Backup-Restoration-Time

Quando ocorreu a última restauração do sistema.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Tempo de restauração do último backup         |
| Ldap-Display-Name | lastBackupRestorationTime            |
| Tamanho              | 8 bytes                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.     |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.519               |
| System-Id-Guid    | 1fbb0be8-ba63-11d0-afef-0000f80367c1 |
| Syntax            | [**Intervalo**](s-interval.md)       |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| Tem valor único       | Verdadeiro                                     |
| É indexado             | Falso                                    |
| No Catálogo Global      | Falso                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| Tem valor único       | Verdadeiro                                     |
| É indexado             | Falso                                    |
| No Catálogo Global      | Falso                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| Tem valor único       | Verdadeiro                                     |
| É indexado             | Falso                                    |
| No Catálogo Global      | Falso                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| É de valor único       | Verdadeiro                                     |
| É indexado             | Falso                                    |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| É de valor único       | Verdadeiro                                     |
| É indexado             | Falso                                    |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| É de valor único       | Verdadeiro                                     |
| É indexado             | Falso                                    |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| É de valor único       | Verdadeiro                                     |
| É indexado             | Falso                                    |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





