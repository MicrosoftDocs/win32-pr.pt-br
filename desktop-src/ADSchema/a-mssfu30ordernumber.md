---
title: msSFU-30-Order-atributo de número
description: Contém um valor que é usado pelo NIS para verificar se o mapa foi alterado.
ms.assetid: b2e83980-2de4-4001-b65a-8073c9258b27
ms.tgt_platform: multiple
keywords:
- msSFU-30-Order-número de atributo do AD Schema
- Esquema de AD do atributo msSFU30OrderNumber
topic_type:
- apiref
api_name:
- msSFU-30-Order-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 995064d10d16849e75da6cc2ab796a443d684dee68af4e1d73dedcf65b8c114c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508856"
---
# <a name="mssfu-30-order-number-attribute"></a>msSFU-30-Order-atributo de número

Contém um valor que é usado pelo NIS para verificar se o mapa foi alterado. Toda vez que os dados armazenados no objeto [**msSFU-30-Domain-info**](c-mssfu30domaininfo.md) são alterados, esse valor é incrementado. Esse valor é usado para rastrear as alterações de dados entre chamadas **ypxfer** .



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | msSFU-30-ordem-número                       |
| LDAP-Display-Name | msSFU30OrderNumber                          |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.6.18.1.308                 |
| System-ID-GUID    | 02625f05-d1ee-4f9f-b366-55266becb95c        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | Verdadeiro                                                           |
| É indexado             | Verdadeiro                                                           |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | \-                                                             |
| Range-Upper            | \-                                                             |
| Search-Flags           | 0x00000001                                                     |
| System-Flags           | 0x00000000                                                     |
| Classes usadas em        | [**msSFU-30-Domain-info**](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | Verdadeiro                                                           |
| É indexado             | Verdadeiro                                                           |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | \-                                                             |
| Range-Upper            | \-                                                             |
| Search-Flags           | 0x00000001                                                     |
| System-Flags           | 0x00000000                                                     |
| Classes usadas em        | [**msSFU-30-Domain-info**](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| É de valor único       | Verdadeiro                                                           |
| É indexado             | Verdadeiro                                                           |
| No catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                   |
| Range-Lower            | \-                                                             |
| Range-Upper            | \-                                                             |
| Search-Flags           | 0x00000001                                                     |
| System-Flags           | 0x00000000                                                     |
| Classes usadas em        | [**msSFU-30-Domain-info**](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------|
| ID do link                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| Tem valor único       | Verdadeiro                                                           |
| É indexado             | Verdadeiro                                                           |
| No Catálogo Global      | Falso                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                   |
| Range-Lower            | \-                                                             |
| Range-Upper            | \-                                                             |
| Search-Flags           | 0x00000001                                                     |
| System-Flags           | 0x00000000                                                     |
| Classes usadas em        | [**msSFU-30-Domain-Info**](c-mssfu30domaininfo.md)<br/> |



 

 





