---
title: Atributo NT-Mixed-Domain
description: Indica que o domínio está no modo nativo ou no modo misto. Esse atributo é encontrado no objeto domainDNS (head) para o domínio.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo NT-Mixed-Domain
- Esquema do AD do atributo nTMixedDomain
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39148883e2b5d57157c334854ab7ebdfa61b69ac61d7a0100fc8470b741909c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703026"
---
# <a name="nt-mixed-domain-attribute"></a>Atributo NT-Mixed-Domain

Indica que o domínio está no modo nativo ou no modo misto. Esse atributo é encontrado no objeto domainDNS (head) para o domínio.



| Entrada | Valor |
|-------------------|---------------------------------------|
| CN                | Domínio misto NT                       |
| Ldap-Display-Name | nTMixedDomain                         |
| Tamanho              | 4 bytes. Modo misto 1, modo nativo 0. |
| Privilégio de atualização  | \-                                    |
| Frequência de atualização  | \-                                    |
| Attribute-Id      | 1.2.840.113556.1.4.357                |
| System-Id-Guid    | 3e97891f-8c01-11d0-afda-00c04fd930c9  |
| Syntax            | [**Enumeração**](s-enumeration.md)  |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| Tem valor único       | Verdadeiro                                                                                    |
| É indexado             | Falso                                                                                   |
| No Catálogo Global      | Falso                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Cross-Ref**](c-crossref.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| Tem valor único       | Verdadeiro                                                                                    |
| É indexado             | Falso                                                                                   |
| No Catálogo Global      | Falso                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| É de valor único       | Verdadeiro                                                                                    |
| É indexado             | Falso                                                                                   |
| No catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| É de valor único       | Verdadeiro                                                                                    |
| É indexado             | Falso                                                                                   |
| No catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| É de valor único       | Verdadeiro                                                                                    |
| É indexado             | Falso                                                                                   |
| No catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



 

 





