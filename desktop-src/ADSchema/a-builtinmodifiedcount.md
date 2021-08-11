---
title: Atributo Builtin-Modified-Count
description: O atributo Builtin-Modified-Count é usado para dar suporte à replicação Windows NT domínios 4.0.
ms.assetid: e5a0f299-1e69-4b47-a0b1-e5bcf7bd47eb
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Builtin-Modified-Count
- Esquema do AD do atributo builtinModifiedCount
topic_type:
- apiref
api_name:
- Builtin-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0416f1fe6f75c5b6b8245fa57fe9b277ae2eb2405cbbef7b029bd64d41ad4a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118177890"
---
# <a name="builtin-modified-count-attribute"></a>Atributo Builtin-Modified-Count

O **atributo Builtin-Modified-Count** é usado para dar suporte à replicação Windows NT domínios 4.0.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Contagem de modificações criadas               |
| Ldap-Display-Name | builtinModifiedCount                 |
| Tamanho              | 8 bytes                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.     |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.14                |
| System-Id-Guid    | bf967930-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | True                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | True                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | True                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sam-domínio**](c-samdomain.md)<br/> |



 

 





