---
title: Atributo SAM-Account-Type
description: Esse atributo contém informações sobre cada objeto de tipo de conta.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo SAM-Account-Type
- Esquema do AD do atributo sAMAccountType
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
# <a name="sam-account-type-attribute"></a>Atributo SAM-Account-Type

Esse atributo contém informações sobre cada objeto de tipo de conta. Você pode enumerar uma lista de tipos de conta ou usar a API exibir informações para criar uma lista. Como computadores, contas de usuário normais e contas de confiança também podem ser enumerados como objetos de usuário, os valores dessas contas devem ser um intervalo contíguo.

Os valores possíveis para esse atributo são os seguintes:

-   OBJETO \_ DE DOMÍNIO SAM \_ 0X0
-   OBJETOS \_ DE GRUPO SAM \_ 0X10000000
-   OBJETO \_ SAM NON SECURITY GROUP \_ \_ \_ 0X10000001
-   OBJETO \_ ALIAS \_ SAM 0x20000000
-   OBJETO SAM \_ NON \_ SECURITY ALIAS \_ \_ 0X20000001
-   OBJETO \_ DE USUÁRIO SAM \_ 0x30000000
-   CONTA DE USUÁRIO NORMAL DO SAM \_ \_ \_ 0X30000000
-   Conta \_ DE COMPUTADOR SAM \_ 0x30000001
-   CONTA \_ CONFIÁVEL \_ SAM 0X30000002
-   GRUPO BÁSICO DO APLICATIVO SAM \_ \_ \_ 0X40000000
-   GRUPO DE CONSULTAS DO APLICATIVO SAM \_ \_ \_ 0X40000001
-   TIPO DE CONTA SAM \_ \_ MAX \_ 0x7fffffff



| Entrada | Valor |
|-------------------|-----------------------------------------------------------------|
| CN                | Tipo de conta SAM                                                |
| Ldap-Display-Name | sAMAccountType                                                  |
| Tamanho              | \-                                                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                                |
| Frequência de atualização  | Isso é definido pelo sistema operacional quando o objeto é criado. |
| Attribute-Id      | 1.2.840.113556.1.4.302                                          |
| System-Id-Guid    | 6e7b626c-64f2-11d0-afd2-00c04fd930c9                            |
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
| Tem valor único       | Verdadeiro                                                         |
| É indexado             | Verdadeiro                                                         |
| No Catálogo Global      | Verdadeiro                                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



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



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



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



 

 





