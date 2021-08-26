---
title: DNS-Tombstoned atributo
description: True se este objeto tiver sido marcado para exclusão. Esse atributo existe para tornar a pesquisa de registros marcados para exclusão mais fácil e rápida. Os objetos marcados para exclusão são objetos que foram excluídos, mas que ainda não foram removidos do diretório.
ms.assetid: d876a6d7-d5bc-4fe2-af03-1fff3381708f
ms.tgt_platform: multiple
keywords:
- Esquema de DNS-Tombstoned do atributo AD
- Esquema de AD do atributo dNSTombstoned
topic_type:
- apiref
api_name:
- DNS-Tombstoned
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ef8f1b61d8d12fc1725fd695467058ac93277a7aab0977ccaed128a74da79d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077856"
---
# <a name="dns-tombstoned-attribute"></a>DNS-Tombstoned atributo

True se este objeto tiver sido marcado para exclusão. Esse atributo existe para tornar a pesquisa de registros marcados para exclusão mais fácil e rápida. Os objetos marcados para exclusão são objetos que foram excluídos, mas que ainda não foram removidos do diretório.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | DNS-Tombstoned                       |
| LDAP-Display-Name | dNSTombstoned                        |
| Tamanho              | 4 bytes                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.     |
| Frequência de atualização  | Sempre que um objeto é excluído.       |
| Attribute-Id      | 1.2.840.113556.1.4.1414              |
| System-ID-GUID    | d5eb2eb7-be4e-463b-a214-634a44d7392e |
| Syntax            | [**Boolean**](s-boolean.md)         |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| É de valor único       | Verdadeiro                                     |
| É indexado             | Verdadeiro                                     |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| É de valor único       | Verdadeiro                                     |
| É indexado             | Verdadeiro                                     |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| É de valor único       | Verdadeiro                                     |
| É indexado             | Verdadeiro                                     |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| É de valor único       | Verdadeiro                                     |
| É indexado             | Verdadeiro                                     |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| É de valor único       | Verdadeiro                                     |
| É indexado             | Verdadeiro                                     |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| É de valor único       | Verdadeiro                                     |
| É indexado             | Verdadeiro                                     |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> |



 

 





