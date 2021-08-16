---
title: Atributo repl-Property-meta-data
description: Rastreia informações de estado de replicação interna para objetos DS. As informações aqui podem ser extraídas em formato público por meio da API pública DsReplicaGetInfo (). Presente em todos os objetos DS.
ms.assetid: 5776208c-8138-4b0a-855a-8bddcbd2e532
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo repl-Property-meta-data
- Esquema de AD do atributo replPropertyMetaData
topic_type:
- apiref
api_name:
- Repl-Property-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dedebf88923d64ba14882a885f74254474664e79756dd7f12fd2e3b02a09545
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117836658"
---
# <a name="repl-property-meta-data-attribute"></a>Atributo repl-Property-meta-data

Rastreia informações de estado de replicação interna para objetos DS. As informações aqui podem ser extraídas em formato público por meio da API pública DsReplicaGetInfo (). Presente em todos os objetos DS.



| Entrada | Valor |
|-------------------|------------------------------------------------------------------------------|
| CN                | Repl-Property-meta-data                                                      |
| LDAP-Display-Name | replPropertyMetaData                                                         |
| Tamanho              | Comprimento é proporcional ao número de atributos replicáveis no objeto. |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                                             |
| Frequência de atualização  | Alterações em resposta a qualquer alteração de replicação no objeto.                |
| Attribute-Id      | 1.2.840.113556.1.4.3                                                         |
| System-ID-GUID    | 281416c0-1968-11d0-a28f-00aa003049e2                                         |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md)                        |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No catálogo global      | Verdadeiro                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No catálogo global      | Verdadeiro                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No catálogo global      | Verdadeiro                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No catálogo global      | Verdadeiro                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No catálogo global      | Verdadeiro                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No catálogo global      | Verdadeiro                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No catálogo global      | Verdadeiro                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



 

 





