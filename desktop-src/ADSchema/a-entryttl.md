---
title: Atributo entry-TTL
description: Esse atributo operacional é mantido pelo servidor e parece estar presente em cada entrada dinâmica.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Entry-TTL
- Esquema do AD do atributo entryTTL
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcd3e06304824ba51431b00b6a5b90d24d7719194dd84974470a101d5f6a1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961555"
---
# <a name="entry-ttl-attribute"></a>Atributo entry-TTL

Esse atributo operacional é mantido pelo servidor e parece estar presente em cada entrada dinâmica. O atributo não está presente quando a entrada não contém a classe de objeto dynamicObject. O valor desse atributo é o tempo, em segundos, que a entrada continuará a existir antes de desaparecer do diretório. Na ausência de operações de "atualização" intermediárias, os valores retornados pela leitura do atributo em duas pesquisas sucessivas têm a garantia de que não serão desatribuir. O menor valor permitido é 0, indicando que a entrada pode desaparecer sem aviso. O atributo é marcado como NO-USER-MODIFICATION porque só pode ser alterado usando a operação de atualização.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Entry-TTL                                   |
| Ldap-Display-Name | entryTTL                                    |
| Tamanho              | 4 bytes. Máximo = 1 ano, padrão = 1 dia. |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.3.6.1.4.1.1466.101.119.3                  |
| System-Id-Guid    | d213decc-d81a-4384-aac2-dcfcfd631cf8        |
| Syntax            | [**Enumeração**](s-enumeration.md)        |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No Catálogo Global      | Falso                                                |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes usadas em        | [**Objeto dinâmico**](c-dynamicobject.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No Catálogo Global      | Falso                                                |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes usadas em        | [**Objeto dinâmico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No Catálogo Global      | Falso                                                |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes usadas em        | [**Objeto dinâmico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes usadas em        | [**Objeto dinâmico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes usadas em        | [**Objeto dinâmico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classes usadas em        | [**Objeto dinâmico**](c-dynamicobject.md)<br/> |



 

 





