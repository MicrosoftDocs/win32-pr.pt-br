---
title: Atributo Last-Set-Time
description: A última vez em que o segredo foi alterado.
ms.assetid: 71245cd4-90d8-4aa1-ad96-d46d6b3a7ad0
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Last-Set-Time
- Esquema do AD do atributo lastSetTime
topic_type:
- apiref
api_name:
- Last-Set-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7349535f4fbf17624b9cfc353627676988cdf4af63c742ad4c764f2d28e8e29b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804246"
---
# <a name="last-set-time-attribute"></a>Atributo Last-Set-Time

A última vez em que o segredo foi alterado. Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 nanossegundos desde 1º de janeiro de 1601 (UTC).



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Hora da última definição                        |
| Ldap-Display-Name | lastSetTime                          |
| Tamanho              | 8 bytes                              |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.53                |
| System-Id-Guid    | bf967998-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| Tem valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No Catálogo Global      | Falso                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Segredo**](c-secret.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| Tem valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No Catálogo Global      | Falso                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Segredo**](c-secret.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| Tem valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No Catálogo Global      | Falso                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Segredo**](c-secret.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| É de valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No catálogo global      | Falso                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Segredo**](c-secret.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| É de valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No catálogo global      | Falso                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Segredo**](c-secret.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| É de valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No catálogo global      | Falso                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Segredo**](c-secret.md)<br/> |



 

 





