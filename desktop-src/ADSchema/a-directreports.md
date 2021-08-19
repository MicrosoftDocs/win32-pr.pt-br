---
title: Atributo de relatórios
description: Contém a lista de usuários que se reportam diretamente ao usuário. Os usuários listados como relatórios são aqueles que têm a propriedade Gerenciador de propriedades definida para esse usuário. Cada item na lista é uma referência vinculada ao objeto que representa o usuário.
ms.assetid: 369fc457-685c-4875-aed3-0a246a219512
ms.tgt_platform: multiple
keywords:
- Atributo do AD de atributos de relatórios
- Esquema de AD do atributo directReports
topic_type:
- apiref
api_name:
- Reports
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60354fc07c5ea8fecada9150aea13308e10a92e1836bd37ea8d398e84f6d0f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049596"
---
# <a name="reports-attribute"></a>Atributo de relatórios

Contém a lista de usuários que se reportam diretamente ao usuário. Os usuários listados como relatórios são aqueles que têm a propriedade Gerenciador de propriedades definida para esse usuário. Cada item na lista é uma referência vinculada ao objeto que representa o usuário.



| Entrada | Valor |
|-------------------|-------------------------------------------------|
| CN                | Relatórios                                         |
| LDAP-Display-Name | directReports                                   |
| Tamanho              | \-                                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                |
| Frequência de atualização  | Sempre que os subordinados diretos de um usuário forem alterados. |
| Attribute-Id      | 1.2.840.113556.1.2.436                          |
| System-ID-GUID    | bf967a1c-0de6-11d0-a285-00aa003049e2            |
| Syntax            | [**Objeto (DS-DN)**](s-object-ds-dn.md)         |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | 43                              |
| MAPI-Id                | 0x800E                          |
| System-Only            | Verdadeiro                            |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | 43                              |
| MAPI-Id                | 0x800E                          |
| System-Only            | Verdadeiro                            |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | 43                              |
| MAPI-Id                | 0x800E                          |
| System-Only            | Verdadeiro                            |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | 43                              |
| MAPI-Id                | 0x800E                          |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Falso                           |
| É indexado             | Falso                           |
| No Catálogo Global      | Falso                           |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | 43                              |
| MAPI-Id                | 0x800E                          |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Falso                           |
| É indexado             | Falso                           |
| No Catálogo Global      | Falso                           |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | 43                              |
| MAPI-Id                | 0x800E                          |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Falso                           |
| É indexado             | Falso                           |
| No Catálogo Global      | Falso                           |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



 

 





