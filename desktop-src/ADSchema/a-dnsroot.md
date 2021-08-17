---
title: Dns-Root atributo
description: O nome de domínio DNS mais alto atribuído a uma partição de domínio/diretório.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Dns-Root atributo AD Schema
- Esquema do AD do atributo dnsRoot
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f87acecb86fcd8ca8af4bbc2917dbe5381deaf4e5722a5803d31f186e57e04d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961575"
---
# <a name="dns-root-attribute"></a>Dns-Root atributo

O nome de domínio DNS mais alto atribuído a uma partição de domínio/diretório. Isso é definido em um objeto crossRef e é usado, entre outras coisas, para geração de indicação. Ao pesquisar por uma árvore de domínio inteira, a pesquisa deve ser iniciada no Dns-Root objeto . Esse atributo pode ter vários valores, caso em que várias indicações são geradas.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Dns-Root                                    |
| Ldap-Display-Name | Dnsroot                                     |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Esse valor é definido pelo sistema.            |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.28                       |
| System-Id-Guid    | bf967959-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Tem valor único       | Falso                                      |
| É indexado             | Verdadeiro                                       |
| No Catálogo Global      | Falso                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Cross-Ref**](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Tem valor único       | Falso                                      |
| É indexado             | Verdadeiro                                       |
| No Catálogo Global      | Falso                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Cross-Ref**](c-crossref.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Tem valor único       | Falso                                      |
| É indexado             | Verdadeiro                                       |
| No Catálogo Global      | Falso                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Cross-Ref**](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Tem valor único       | Falso                                      |
| É indexado             | Verdadeiro                                       |
| No Catálogo Global      | Falso                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Cross-Ref**](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Tem valor único       | Falso                                      |
| É indexado             | Verdadeiro                                       |
| No Catálogo Global      | Falso                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Cross-Ref**](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Tem valor único       | Falso                                      |
| É indexado             | Verdadeiro                                       |
| No Catálogo Global      | Falso                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Cross-Ref**](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Tem valor único       | Falso                                      |
| É indexado             | Verdadeiro                                       |
| No Catálogo Global      | Falso                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Cross-Ref**](c-crossref.md)<br/> |



 

 





