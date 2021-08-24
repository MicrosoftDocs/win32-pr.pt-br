---
title: Server-State atributo
description: Indica se o servidor está habilitado ou desabilitado.
ms.assetid: e062cbcf-c845-4dfd-9e9b-e21079276a3c
ms.tgt_platform: multiple
keywords:
- Esquema de Server-State do atributo AD
- Esquema de AD do atributo ServerState
topic_type:
- apiref
api_name:
- Server-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 186f6c3da7371c82f7771261adbf09814ad16481a97050753b23ea8b3b5226cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836721"
---
# <a name="server-state-attribute"></a>Server-State atributo

Indica se o servidor está habilitado ou desabilitado. Um valor de 1 indica que o servidor está habilitado. Um valor de 2 indica que o servidor está desabilitado. Todos os outros valores são inválidos.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Server-State                         |
| LDAP-Display-Name | serverState                          |
| Tamanho              | \-                                   |
| Privilégio de atualização  | Esse valor é definido pelo sistema.     |
| Frequência de atualização  | Quando a política para um usuário é alterada.  |
| Attribute-Id      | 1.2.840.113556.1.4.154               |
| System-ID-GUID    | bf967a34-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| É de valor único       | Verdadeiro                                                  |
| É indexado             | Falso                                                 |
| No catálogo global      | Falso                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000011                                            |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| É de valor único       | Verdadeiro                                                  |
| É indexado             | Falso                                                 |
| No catálogo global      | Falso                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000011                                            |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| É de valor único       | Verdadeiro                                                  |
| É indexado             | Falso                                                 |
| No catálogo global      | Falso                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000011                                            |
| Classes usadas em        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Tem valor único       | Verdadeiro                                                  |
| É indexado             | Falso                                                 |
| No Catálogo Global      | Falso                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000011                                            |
| Classes usadas em        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Tem valor único       | Verdadeiro                                                  |
| É indexado             | Falso                                                 |
| No Catálogo Global      | Falso                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000011                                            |
| Classes usadas em        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Tem valor único       | Verdadeiro                                                  |
| É indexado             | Falso                                                 |
| No Catálogo Global      | Falso                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000011                                            |
| Classes usadas em        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





