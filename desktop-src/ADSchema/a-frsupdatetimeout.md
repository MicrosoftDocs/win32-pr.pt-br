---
title: FRS-atualizar-atributo de tempo limite
description: O tempo máximo, em minutos, a aguardar para concluir uma atualização antes de desistir.
ms.assetid: 0c06510e-d4a8-42f8-bf81-13a9f103e237
ms.tgt_platform: multiple
keywords:
- FRS-Update-Timeout-esquema de atributo do AD
- Esquema de AD do atributo fRSUpdateTimeout
topic_type:
- apiref
api_name:
- FRS-Update-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711177ae5c676e2a18bd89af772827a52dd475ec3831e11df71ba25c63fbc4c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323365"
---
# <a name="frs-update-timeout-attribute"></a>FRS-atualizar-atributo de tempo limite

O tempo máximo, em minutos, a aguardar para concluir uma atualização antes de desistir.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | FRS-Update-Timeout                   |
| LDAP-Display-Name | fRSUpdateTimeout                     |
| Tamanho              | 4 bytes                              |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.485               |
| System-ID-GUID    | 1be8f172-a9ff-11d0-afe2-00c04fd930c9 |
| Syntax            | [**Enumeração**](s-enumeration.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Falso                                                                                                     |
| É de valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No catálogo global      | Falso                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Falso                                                                                                     |
| É de valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No catálogo global      | Falso                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**NTFRS-assinante**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Falso                                                                                                     |
| É de valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No catálogo global      | Falso                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**NTFRS-membro**](c-ntfrsmember.md)<br/> [**Assinante NTFRS**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Falso                                                                                                     |
| Tem valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No Catálogo Global      | Falso                                                                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Membro NTFRS**](c-ntfrsmember.md)<br/> [**Assinante NTFRS**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Falso                                                                                                     |
| Tem valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No Catálogo Global      | Falso                                                                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Membro NTFRS**](c-ntfrsmember.md)<br/> [**Assinante NTFRS**](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Falso                                                                                                     |
| Tem valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No Catálogo Global      | Falso                                                                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Membro NTFRS**](c-ntfrsmember.md)<br/> [**Assinante NTFRS**](c-ntfrssubscriber.md)<br/> |



 

 





