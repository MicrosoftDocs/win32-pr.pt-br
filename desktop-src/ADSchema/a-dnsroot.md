---
title: Dns-Root atributo
description: O nome de domínio DNS superior atribuído a uma partição de domínio/diretório.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Esquema de Dns-Root do atributo AD
- Esquema de AD do atributo dnsRoot
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755736"
---
# <a name="dns-root-attribute"></a>Dns-Root atributo

O nome de domínio DNS superior atribuído a uma partição de domínio/diretório. Isso é definido em um objeto crossRef e é usado, entre outras coisas, para a geração de referência. Ao pesquisar uma árvore de domínio inteira, a pesquisa deve ser iniciada no objeto Dns-Root. Esse atributo pode ter valores múltiplos e, nesse caso, várias referências são geradas.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Dns-Root                                    |
| LDAP-Display-Name | dnsRoot                                     |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Esse valor é definido pelo sistema.            |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.28                       |
| System-ID-GUID    | bf967959-0de6-11d0-a285-00aa003049e2        |
| Sintaxe            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



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
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| É de valor único       | Falso                                      |
| É indexado             | True                                       |
| No catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| É de valor único       | Falso                                      |
| É indexado             | True                                       |
| No catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| É de valor único       | Falso                                      |
| É indexado             | True                                       |
| No catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| É de valor único       | Falso                                      |
| É indexado             | True                                       |
| No catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| É de valor único       | Falso                                      |
| É indexado             | True                                       |
| No catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| É de valor único       | Falso                                      |
| É indexado             | True                                       |
| No catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------|
| ID do link                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| É de valor único       | Falso                                      |
| É indexado             | True                                       |
| No catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> |



 

 





