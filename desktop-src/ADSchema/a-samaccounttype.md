---
title: SAM-atributo de tipo de conta
description: Esse atributo contém informações sobre cada objeto de tipo de conta.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- SAM-tipo de conta do atributo AD Schema
- Esquema de AD do atributo sAMAccountType
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132532af58eafa4950f049fb08ff7a4235cb49ac2b1f62fc832e308e7ab6d31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118423383"
---
# <a name="sam-account-type-attribute"></a>SAM-atributo de tipo de conta

Esse atributo contém informações sobre cada objeto de tipo de conta. Você pode enumerar uma lista de tipos de conta ou pode usar a API de informações de exibição para criar uma lista. Como computadores, contas de usuário normais e contas de confiança também podem ser enumerados como objetos de usuário, os valores dessas contas devem ser um intervalo contíguo.

Os valores possíveis para esse atributo são os seguintes:

-   \_Objeto de domínio Sam \_ 0x0
-   \_Objeto de grupo Sam \_ 0x10000000
-   SAM \_ \_ objeto de \_ grupo não segurança \_ 0x10000001
-   \_Objeto de alias Sam \_ 0x20000000
-   \_Objeto de \_ alias de não segurança Sam \_ \_ 0x20000001
-   \_Objeto de usuário Sam \_ 0x30000000
-   \_Conta de usuário normal do Sam \_ \_ 0x30000000
-   0x30000001 da conta do \_ computador Sam \_
-   \_0x30000002 de \_ conta confiável Sam
-   \_Grupo básico do aplicativo Sam \_ \_ 0x40000000
-   \_Grupo de consulta do aplicativo Sam \_ \_ 0x40000001
-   \_Tipo de conta Sam máx. \_ \_ 0x7FFFFFFF



| Entrada | Valor |
|-------------------|-----------------------------------------------------------------|
| CN                | SAM-tipo de conta                                                |
| LDAP-Display-Name | sAMAccountType                                                  |
| Tamanho              | \-                                                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                                |
| Frequência de atualização  | Isso é definido pelo sistema operacional quando o objeto é criado. |
| Attribute-Id      | 1.2.840.113556.1.4.302                                          |
| System-ID-GUID    | 6e7b626c-64f2-11d0-afd2-00c04fd930c9                            |
| Syntax            | [**Enumeração**](s-enumeration.md)                            |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Verdadeiro                                                         |
| É indexado             | Verdadeiro                                                         |
| No catálogo global      | Verdadeiro                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Verdadeiro                                                         |
| É indexado             | Verdadeiro                                                         |
| No catálogo global      | Verdadeiro                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Verdadeiro                                                         |
| É indexado             | Verdadeiro                                                         |
| No Catálogo Global      | Verdadeiro                                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Tem valor único       | Verdadeiro                                                         |
| É indexado             | Verdadeiro                                                         |
| No Catálogo Global      | Verdadeiro                                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Tem valor único       | Verdadeiro                                                         |
| É indexado             | Verdadeiro                                                         |
| No Catálogo Global      | Verdadeiro                                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Tem valor único       | Verdadeiro                                                         |
| É indexado             | Verdadeiro                                                         |
| No Catálogo Global      | Verdadeiro                                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> |



 

 





