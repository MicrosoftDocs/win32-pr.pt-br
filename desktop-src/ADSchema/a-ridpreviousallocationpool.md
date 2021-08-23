---
title: Atributo RID-Previous-Allocation-pool
description: Contém o pool de RIDs (identificadores relativos) do qual um controlador de domínio se aloca.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- RID-Previous-Allocation-pool de atributos do AD Schema
- Esquema de AD do atributo rIDPreviousAllocationPool
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5199d9fd0f91b94ed6625a8759f3a5acd76a892460c44e3315911350f0ff59f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837356"
---
# <a name="rid-previous-allocation-pool-attribute"></a>Atributo RID-Previous-Allocation-pool

O atributo **RID-Previous-Alloc-pool** contém o pool de RIDs (identificadores relativos) do qual um controlador de domínio se aloca. Esse atributo é um valor de oito bytes que contém um par de inteiros de quatro bytes que representam os valores de início e término do pool de RIDs. O valor inicial está nos quatro bytes inferiores e o valor final está nos quatro bytes superiores.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | RID-anterior-pool de alocação         |
| LDAP-Display-Name | rIDPreviousAllocationPool            |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.372               |
| System-ID-GUID    | 6617188a-8f3c-11d0-afda-00c04fd930c9 |
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
| É de valor único       | Verdadeiro                                   |
| É indexado             | Falso                                  |
| No catálogo global      | Falso                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classes usadas em        | [**RID-definido**](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



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
| System-Flags           | 0x00000011                             |
| Classes usadas em        | [**RID-definido**](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



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
| System-Flags           | 0x00000011                             |
| Classes usadas em        | [**RID-definido**](c-ridset.md)<br/> |



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
| System-Flags           | 0x00000011                             |
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
| System-Flags           | 0x00000011                             |
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
| System-Flags           | 0x00000011                             |
| Classes usadas em        | [**RID-definido**](c-ridset.md)<br/> |



 

 





