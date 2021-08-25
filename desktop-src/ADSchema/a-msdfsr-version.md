---
title: Atributo ms-DFSR-Version
description: Contém o número de versão do serviço de replicação Sistema de Arquivos Distribuído (DFS).
ms.assetid: 2e49aef2-d3a5-43b8-aad8-1cd99ae51ea3
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo ms-DFSR-Version
- Esquema do AD do atributo msDFSR-Version
topic_type:
- apiref
api_name:
- ms-DFSR-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f68a3d2d501c6aab88f6b281e37f9fa9e0c6d7b928dac67c2422fe2069b670ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924656"
---
# <a name="ms-dfsr-version-attribute"></a>Atributo ms-DFSR-Version

Contém o número de versão do serviço de replicação Sistema de Arquivos Distribuído (DFS).



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | ms-DFSR-Version                             |
| Ldap-Display-Name | msDFSR-Version                              |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.6.13.3.1                   |
| System-Id-Guid    | 1a861408-38c3-49ea-ba75-85481a77c655        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                          |
| MAPI-Id                | \-                                                                                                                                          |
| System-Only            | Falso                                                                                                                                       |
| Tem valor único       | Verdadeiro                                                                                                                                        |
| É indexado             | Falso                                                                                                                                       |
| No Catálogo Global      | Falso                                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                |
| Range-Lower            | \-                                                                                                                                          |
| Range-Upper            | \-                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                  |
| System-Flags           | 0x00000000                                                                                                                                  |
| Classes usadas em        | [**ms-DFSR-LocalSettings**](c-msdfsr-localsettings.md)<br/> [**ms-DFSR-ReplicationGroup**](c-msdfsr-replicationgroup.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                          |
| MAPI-Id                | \-                                                                                                                                          |
| System-Only            | Falso                                                                                                                                       |
| Tem valor único       | Verdadeiro                                                                                                                                        |
| É indexado             | Falso                                                                                                                                       |
| No Catálogo Global      | Falso                                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                |
| Range-Lower            | \-                                                                                                                                          |
| Range-Upper            | \-                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                  |
| System-Flags           | 0x00000000                                                                                                                                  |
| Classes usadas em        | [**ms-DFSR-LocalSettings**](c-msdfsr-localsettings.md)<br/> [**ms-DFSR-ReplicationGroup**](c-msdfsr-replicationgroup.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                          |
| MAPI-Id                | \-                                                                                                                                          |
| System-Only            | Falso                                                                                                                                       |
| Tem valor único       | Verdadeiro                                                                                                                                        |
| É indexado             | Falso                                                                                                                                       |
| No Catálogo Global      | Falso                                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                |
| Range-Lower            | \-                                                                                                                                          |
| Range-Upper            | \-                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                  |
| System-Flags           | 0x00000000                                                                                                                                  |
| Classes usadas em        | [**ms-DFSR-LocalSettings**](c-msdfsr-localsettings.md)<br/> [**ms-DFSR-ReplicationGroup**](c-msdfsr-replicationgroup.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                          |
| MAPI-Id                | \-                                                                                                                                          |
| System-Only            | Falso                                                                                                                                       |
| É de valor único       | Verdadeiro                                                                                                                                        |
| É indexado             | Falso                                                                                                                                       |
| No catálogo global      | Falso                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                |
| Range-Lower            | \-                                                                                                                                          |
| Range-Upper            | \-                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                  |
| System-Flags           | 0x00000000                                                                                                                                  |
| Classes usadas em        | [**MS-DFSR-LocalSettings**](c-msdfsr-localsettings.md)<br/> [**MS-DFSR-telereplication**](c-msdfsr-replicationgroup.md)<br/> |



## <a name="remarks"></a>Comentários

O atributo faz parte do suporte ao serviço de Replicação do DFS.

 

 





