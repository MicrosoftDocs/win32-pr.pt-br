---
title: Atributo RID-Allocation-Pool
description: Um pool que foi pré-buscado para uso pelo gerenciador RID quando o RID-Previous-Allocation-Pool foi usado.
ms.assetid: 6d49b497-322f-424c-badc-4801f51481f3
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo RID-Allocation-Pool
- Esquema do AD do atributo rIDAllocationPool
topic_type:
- apiref
api_name:
- RID-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce6ff101ca49e8d2ffafdb31f2d05cf1cb2371ee3336525ab31318925d349805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837376"
---
# <a name="rid-allocation-pool-attribute"></a>Atributo RID-Allocation-Pool

Um pool que foi pré-buscado para uso pelo gerenciador RID quando o RID-Previous-Allocation-Pool foi usado.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | RID-Allocation-Pool                  |
| Ldap-Display-Name | rIDAllocationPool                    |
| Tamanho              | 8 bytes                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.     |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.371               |
| System-Id-Guid    | 66171889-8f3c-11d0-afda-00c04fd930c9 |
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
|------------------------|----------------------------------------|
| ID do link                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadeiro                                   |
| Tem valor único       | Verdadeiro                                   |
| É indexado             | Falso                                  |
| No Catálogo Global      | Falso                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classes usadas em        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------|
| ID do link                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadeiro                                   |
| Tem valor único       | Verdadeiro                                   |
| É indexado             | Falso                                  |
| No Catálogo Global      | Falso                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classes usadas em        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------|
| ID do link                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadeiro                                   |
| Tem valor único       | Verdadeiro                                   |
| É indexado             | Falso                                  |
| No Catálogo Global      | Falso                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classes usadas em        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------|
| ID do link                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadeiro                                   |
| É de valor único       | Verdadeiro                                   |
| É indexado             | Falso                                  |
| No catálogo global      | Falso                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classes usadas em        | [**RID-definido**](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------|
| ID do link                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadeiro                                   |
| É de valor único       | Verdadeiro                                   |
| É indexado             | Falso                                  |
| No catálogo global      | Falso                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classes usadas em        | [**RID-definido**](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------|
| ID do link                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Verdadeiro                                   |
| É de valor único       | Verdadeiro                                   |
| É indexado             | Falso                                  |
| No catálogo global      | Falso                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classes usadas em        | [**RID-definido**](c-ridset.md)<br/> |



 

 





