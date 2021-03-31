---
title: Atributo min-ticket-age
description: Esse atributo determina o período de tempo mínimo, em horas, que o tíquete de concessão de tíquete (TGT) de um usuário pode ser usado para autenticação Kerberos antes que uma solicitação possa ser feita para renovar o tíquete.
ms.assetid: 91a6a8f2-4d8d-4929-8e8d-ffdaa8b05cbe
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo min-ticket-age
- Esquema de AD do atributo minTicketAge
topic_type:
- apiref
api_name:
- Min-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc43277bb3750ee0e759baa4348e85ef826ce010
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086729"
---
# <a name="min-ticket-age-attribute"></a>Atributo min-ticket-age

Esse atributo determina o período de tempo mínimo, em horas, que o tíquete de concessão de tíquete (TGT) de um usuário pode ser usado para autenticação Kerberos antes que uma solicitação possa ser feita para renovar o tíquete.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Duração mínima de tíquetes                       |
| LDAP-Display-Name | minTicketAge                         |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.80                |
| System-ID-GUID    | bf9679c4-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|----------------------------------------------------|
| ID do link                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| É de valor único       | True                                               |
| É indexado             | Falso                                              |
| No catálogo global      | Falso                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------|
| ID do link                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| É de valor único       | True                                               |
| É indexado             | Falso                                              |
| No catálogo global      | Falso                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------|
| ID do link                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| É de valor único       | True                                               |
| É indexado             | Falso                                              |
| No catálogo global      | Falso                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------|
| ID do link                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| É de valor único       | True                                               |
| É indexado             | Falso                                              |
| No catálogo global      | Falso                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------|
| ID do link                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| É de valor único       | True                                               |
| É indexado             | Falso                                              |
| No catálogo global      | Falso                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------|
| ID do link                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| É de valor único       | True                                               |
| É indexado             | Falso                                              |
| No catálogo global      | Falso                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> |



 

 





