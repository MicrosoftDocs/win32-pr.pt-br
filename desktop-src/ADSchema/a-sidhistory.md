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
ms.openlocfilehash: c5c2dbfb3572392bdbed3f13683adc1cbf64b70e061962975a178f8380f55f5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836286"
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
| System-Only            | Verdadeiro                                                         |
| É de valor único       | Falso                                                        |
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
| É de valor único       | Falso                                                        |
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
| É de valor único       | Falso                                                        |
| É indexado             | Verdadeiro                                                         |
| No catálogo global      | Verdadeiro                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
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
| Tem valor único       | Falso                                                        |
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
| Tem valor único       | Falso                                                        |
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
| Tem valor único       | Falso                                                        |
| É indexado             | Verdadeiro                                                         |
| No Catálogo Global      | Verdadeiro                                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes usadas em        | [**Entidade de segurança**](c-securityprincipal.md)<br/> |



 

 





