---
title: Atributo Min-Ticket-Age
description: Esse atributo determina o período mínimo, em horas, que o TGT (tíquete de concessão de tíquete) de um usuário pode ser usado para autenticação Kerberos antes que uma solicitação possa ser feita para renovar o tíquete.
ms.assetid: 91a6a8f2-4d8d-4929-8e8d-ffdaa8b05cbe
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Min-Ticket-Age
- Esquema do AD do atributo minTicketAge
topic_type:
- apiref
api_name:
- Min-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d145bc355693db149a98d5c38c200df2b9785dc6ad37af75c36d18e1add164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118687528"
---
# <a name="min-ticket-age-attribute"></a>Atributo Min-Ticket-Age

Esse atributo determina o período mínimo, em horas, que o TGT (tíquete de concessão de tíquete) de um usuário pode ser usado para autenticação Kerberos antes que uma solicitação possa ser feita para renovar o tíquete.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Idade mínima do tíquete                       |
| Ldap-Display-Name | minTicketAge                         |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.80                |
| System-Id-Guid    | bf9679c4-0de6-11d0-a285-00aa003049e2 |
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
| Tem valor único       | True                                               |
| É indexado             | Falso                                              |
| No Catálogo Global      | Falso                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                       |
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
| Tem valor único       | True                                               |
| É indexado             | Falso                                              |
| No Catálogo Global      | Falso                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                       |
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
| Tem valor único       | True                                               |
| É indexado             | Falso                                              |
| No Catálogo Global      | Falso                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                       |
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



 

 





