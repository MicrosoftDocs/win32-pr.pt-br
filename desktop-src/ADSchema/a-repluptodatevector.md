---
title: Atributo repl-UpToDate-vector
description: Rastreia informações de estado de replicação interna para um NC inteiro. As informações aqui podem ser extraídas em formato público por meio da API DsReplicaGetInfo (). Presente em todos os objetos raiz NC.
ms.assetid: f23d94f8-c31b-447f-98c3-c35a4f5f1d43
ms.tgt_platform: multiple
keywords:
- Repl-UpToDate-esquema de AD do atributo de vetor
- Esquema de AD do atributo replUpToDateVector
topic_type:
- apiref
api_name:
- Repl-UpToDate-Vector
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 413291da92f52e0e6241e6dcfb6ca50303ed5740d370b1f5f900904266a75446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118423727"
---
# <a name="repl-uptodate-vector-attribute"></a>Atributo repl-UpToDate-vector

Rastreia informações de estado de replicação interna para um NC inteiro. As informações aqui podem ser extraídas em formato público por meio da API DsReplicaGetInfo (). Presente em todos os objetos raiz NC.



| Entrada | Valor |
|-------------------|--------------------------------------------------------------------------------|
| CN                | Repl-UpToDate-vector                                                           |
| LDAP-Display-Name | replUpToDateVector                                                             |
| Tamanho              | O comprimento é proporcional ao número de réplicas (passado e presente) do NC. |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                                               |
| Frequência de atualização  | Alterações em resposta a ciclos de replicação de entrada concluídos.                   |
| Attribute-Id      | 1.2.840.113556.1.4.4                                                           |
| System-ID-GUID    | bf967a16-0de6-11d0-a285-00aa003049e2                                           |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md)                          |



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
| Search-Flags           | 0x00000000                      |
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
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
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
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



 

 





