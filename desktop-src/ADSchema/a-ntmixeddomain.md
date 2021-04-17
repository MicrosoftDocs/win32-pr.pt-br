---
title: NT-Mixed-atributo de domínio
description: Indica que o domínio está no modo nativo ou misto. Esse atributo é encontrado no objeto domainDNS (cabeçalho) do domínio.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- Esquema do AD de atributos de domínio do NT-Mixed-
- Esquema de AD do atributo nTMixedDomain
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d73291f392141b80ca8916b86fffa0055226c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105749145"
---
# <a name="nt-mixed-domain-attribute"></a>NT-Mixed-atributo de domínio

Indica que o domínio está no modo nativo ou misto. Esse atributo é encontrado no objeto domainDNS (cabeçalho) do domínio.



| Entrada | Valor |
|-------------------|---------------------------------------|
| CN                | NT-Mixed-Domain                       |
| LDAP-Display-Name | nTMixedDomain                         |
| Tamanho              | 4 bytes. Modo misto 1, modo nativo 0. |
| Privilégio de atualização  | \-                                    |
| Frequência de atualização  | \-                                    |
| Attribute-Id      | 1.2.840.113556.1.4.357                |
| System-ID-GUID    | 3e97891f-8c01-11d0-afda-00c04fd930c9  |
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
| É de valor único       | True                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| É de valor único       | True                                                                                    |
| É indexado             | Falso                                                                                   |
| No catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| É de valor único       | True                                                                                    |
| É indexado             | Falso                                                                                   |
| No catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                            |
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
| É de valor único       | True                                                                                    |
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
| É de valor único       | True                                                                                    |
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
| É de valor único       | True                                                                                    |
| É indexado             | Falso                                                                                   |
| No catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



 

 





