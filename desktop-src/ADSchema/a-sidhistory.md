---
title: SID-History atributo
description: Contém os SIDs anteriores usados para o objeto se o objeto foi movido de outro domínio.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- Esquema de SID-History do atributo AD
- Esquema do AD do atributo sIDHistory
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456174"
---
# <a name="sid-history-attribute"></a>SID-History atributo

Contém os SIDs anteriores usados para o objeto se o objeto foi movido de outro domínio. Sempre que um objeto é movido de um domínio para outro, um novo SID é criado e esse novo SID torna-se o objectSid. O SID anterior é adicionado à propriedade sIDHistory.



| Entrada | Valor |
|-------------------|------------------------------------------------|
| CN                | SID-History                                    |
| LDAP-Display-Name | sIDHistory                                     |
| Tamanho              | \-                                             |
| Privilégio de atualização  | Esse valor é definido pelo sistema.               |
| Frequência de atualização  | Cada vez que o objeto é movido para um novo domínio. |
| Attribute-Id      | 1.2.840.113556.1.4.609                         |
| System-ID-GUID    | 17eb4278-d167-11d0-b002-0000f80367c1           |
| Syntax            | [**Cadeia de caracteres (SID)**](s-string-sid.md)            |



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
| System-Only            | True                                                         |
| É de valor único       | Falso                                                        |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
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
| É de valor único       | Falso                                                        |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
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
| É de valor único       | Falso                                                        |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Falso                                                        |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Falso                                                        |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Falso                                                        |
| É indexado             | True                                                         |
| No catálogo global      | True                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> |



 

 





