---
title: Atributo Max-ticket-age
description: Esse atributo determina a quantidade máxima de tempo, em horas, que o tíquete de concessão de tíquete (TGT) de um usuário pode ser usado para a finalidade da autenticação Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo Max-ticket-age
- Esquema de AD do atributo maxTicketAge
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645361"
---
# <a name="max-ticket-age-attribute"></a>Atributo Max-ticket-age

Esse atributo determina a quantidade máxima de tempo, em horas, que o tíquete de concessão de tíquete (TGT) de um usuário pode ser usado para a finalidade da autenticação Kerberos. Quando o TGT de um usuário expira, um novo deve ser solicitado ou o existente deve ser renovado. Por padrão, essa configuração é definida como 10 horas no objeto de Política de Grupo de domínio padrão (GPO).



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Duração máxima de tíquetes                       |
| LDAP-Display-Name | maxTicketAge                         |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.77                |
| System-ID-GUID    | bf9679be-0de6-11d0-a285-00aa003049e2 |
| Sintaxe            | [**Intervalo**](s-interval.md)       |



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



 

 





