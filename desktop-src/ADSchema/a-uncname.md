---
title: UNC-Name atributo
description: O nome da convenção de nomenização universal para volumes compartilhados e impressoras.
ms.assetid: 967fd0dc-10af-4482-bc2c-1d1dc13dee39
ms.tgt_platform: multiple
keywords:
- UNC-Name atributo AD Schema
- Esquema do AD do atributo uNCName
topic_type:
- apiref
api_name:
- UNC-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6227aaed6ac68c04de1ce8425281674117e11dcb33f8c50db696cff0ea8d8ae8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681591"
---
# <a name="unc-name-attribute"></a>UNC-Name atributo

O nome da convenção de nomenização universal para volumes compartilhados e impressoras.



| Entrada | Valor |
|-------------------|-----------------------------------------------|
| CN                | UNC-Name                                      |
| Ldap-Display-Name | uNCName                                       |
| Tamanho              | \-                                            |
| Privilégio de atualização  | Administrador de domínio                          |
| Frequência de atualização  | Quando novos volumes ou filas de impressão são criados. |
| Attribute-Id      | 1.2.840.113556.1.4.137                        |
| System-Id-Guid    | bf967a64-0de6-11d0-a285-00aa003049e2          |
| Sintaxe            | [**String(Unicode)**](s-string-unicode.md)   |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                |
| Tem valor único       | True                                                                                                                                                 |
| É indexado             | True                                                                                                                                                 |
| No Catálogo Global      | True                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                           |
| Classes usadas em        | [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**Fila de Impressão**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                        |
| MAPI-Id                | \-                                                                                                                                                                                        |
| System-Only            | Falso                                                                                                                                                                                     |
| Tem valor único       | True                                                                                                                                                                                      |
| É indexado             | True                                                                                                                                                                                      |
| No Catálogo Global      | True                                                                                                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                        |
| Search-Flags           | 0x00000001                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                |
| Classes usadas em        | [**FT-Dfs**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**Fila de Impressão**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| Tem valor único       | True                                                                                                                                                                                                                                                                 |
| É indexado             | True                                                                                                                                                                                                                                                                 |
| No Catálogo Global      | True                                                                                                                                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**FT-Dfs**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Fila de Impressão**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| Tem valor único       | True                                                                                                                                                                                                                                                                 |
| É indexado             | True                                                                                                                                                                                                                                                                 |
| No Catálogo Global      | True                                                                                                                                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**FT-Dfs**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Fila de Impressão**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| Tem valor único       | True                                                                                                                                                                                                                                                                 |
| É indexado             | True                                                                                                                                                                                                                                                                 |
| No Catálogo Global      | True                                                                                                                                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**FT-Dfs**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Fila de Impressão**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| Tem valor único       | True                                                                                                                                                                                                                                                                 |
| É indexado             | True                                                                                                                                                                                                                                                                 |
| No Catálogo Global      | True                                                                                                                                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**FT-Dfs**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Fila de Impressão**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



 

 





