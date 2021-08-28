---
title: NETBIOS-Name atributo
description: O nome do objeto a ser usado em NetBIOS.
ms.assetid: 03cbfa61-b747-4f3e-9bf5-17fd6da2e7be
ms.tgt_platform: multiple
keywords:
- NETBIOS-Name atributo AD Schema
- Esquema do AD do atributo nETBIOSName
topic_type:
- apiref
api_name:
- NETBIOS-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e5b7b28237facd30fb6fbfbcfc8f20f93699a8e8ab548889150250b38be4f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118424087"
---
# <a name="netbios-name-attribute"></a>NETBIOS-Name atributo

O nome do objeto a ser usado em NetBIOS.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | NETBIOS-Name                                |
| Ldap-Display-Name | nETBIOSName                                 |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio                        |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.87                       |
| System-Id-Guid    | bf9679d8-0de6-11d0-a285-00aa003049e2        |
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
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| Tem valor único       | Verdadeiro                                                                                    |
| É indexado             | Verdadeiro                                                                                    |
| No Catálogo Global      | Falso                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Cross-Ref**](c-crossref.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| Tem valor único       | Verdadeiro                                                                                    |
| É indexado             | Verdadeiro                                                                                    |
| No Catálogo Global      | Falso                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Cross-Ref**](c-crossref.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------|
| ID do link                | \-                                                                               |
| MAPI-Id                | \-                                                                               |
| System-Only            | Falso                                                                            |
| Tem valor único       | Verdadeiro                                                                             |
| É indexado             | Verdadeiro                                                                             |
| No Catálogo Global      | Falso                                                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                     |
| Range-Lower            | 1                                                                                |
| Range-Upper            | 16                                                                               |
| Search-Flags           | 0x00000001                                                                       |
| System-Flags           | 0x00000010                                                                       |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| É de valor único       | Verdadeiro                                                                                    |
| É indexado             | Verdadeiro                                                                                    |
| No catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| É de valor único       | Verdadeiro                                                                                    |
| É indexado             | Verdadeiro                                                                                    |
| No catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| É de valor único       | Verdadeiro                                                                                    |
| É indexado             | Verdadeiro                                                                                    |
| No catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Referência cruzada**](c-crossref.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| É de valor único       | Verdadeiro                                                                                    |
| É indexado             | Verdadeiro                                                                                    |
| No catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | 1                                                                                       |
| Range-Upper            | 16                                                                                      |
| Search-Flags           | 0x00000001                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes usadas em        | [**Cross-Ref**](c-crossref.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> |



 

 





