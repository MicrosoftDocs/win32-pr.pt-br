---
title: Atributo de palavras-chave
description: Uma lista de palavras-chave que podem ser usadas para localizar um determinado ponto de conexão.
ms.assetid: 24297ebf-8d32-4b22-9dd9-b26bce675118
ms.tgt_platform: multiple
keywords:
- Atributo do AD de atributos de palavras-chave
- atributo do AD de atributos de palavras-chave
topic_type:
- apiref
api_name:
- Keywords
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5c1fba475505ee03cda4813f90a28d1c91fb69
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645477"
---
# <a name="keywords-attribute"></a>Atributo de palavras-chave

Uma lista de palavras-chave que podem ser usadas para localizar um determinado ponto de conexão.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Palavras-chave                                    |
| LDAP-Display-Name | palavras-chave                                    |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.48                       |
| System-ID-GUID    | bf967993-0de6-11d0-a285-00aa003049e2        |
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
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | Falso                                                    |
| É de valor único       | Falso                                                    |
| É indexado             | True                                                     |
| No catálogo global      | True                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 256                                                      |
| Search-Flags           | 0x00000001                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Ponto de conexão**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                   |
| É indexado             | True                                                                                                                                                                                                                                                                                    |
| No catálogo global      | True                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Ponto de conexão**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-app-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                       |
| MAPI-Id                | \-                                                                                                                       |
| System-Only            | Falso                                                                                                                    |
| É de valor único       | Falso                                                                                                                    |
| É indexado             | True                                                                                                                     |
| No catálogo global      | True                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                             |
| Range-Lower            | 1                                                                                                                        |
| Range-Upper            | 256                                                                                                                      |
| Search-Flags           | 0x00000001                                                                                                               |
| System-Flags           | 0x00000010                                                                                                               |
| Classes usadas em        | [**ms-DS-Service-Connection-Point-publication-Service**](c-msds-serviceconnectionpointpublicationservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                   |
| É indexado             | True                                                                                                                                                                                                                                                                                    |
| No catálogo global      | True                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Ponto de conexão**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-app-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                   |
| É indexado             | True                                                                                                                                                                                                                                                                                    |
| No catálogo global      | True                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Ponto de conexão**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-app-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                   |
| É indexado             | True                                                                                                                                                                                                                                                                                    |
| No catálogo global      | True                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Ponto de conexão**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-app-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                   |
| É indexado             | True                                                                                                                                                                                                                                                                                    |
| No catálogo global      | True                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Ponto de conexão**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-app-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



 

 





