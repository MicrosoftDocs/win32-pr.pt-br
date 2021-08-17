---
title: atributo ms-DFSR-DirectoryFilter
description: Contém a cadeia de caracteres de filtro que é aplicada aos diretórios.
ms.assetid: baea6575-80d3-4f69-8e98-47f4a5941388
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DFSR-DirectoryFilter
- Esquema de AD do atributo msDFSR-DirectoryFilter
topic_type:
- apiref
api_name:
- ms-DFSR-DirectoryFilter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7978db7c7dbdb478574a05c5ca3622a1043c7acd85b967ccf813a3a1b6a65899
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118685862"
---
# <a name="ms-dfsr-directoryfilter-attribute"></a>atributo ms-DFSR-DirectoryFilter

Contém a cadeia de caracteres de filtro que é aplicada aos diretórios.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | MS-DFSR-DirectoryFilter                     |
| LDAP-Display-Name | msDFSR-DirectoryFilter                      |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.6.13.3.13                  |
| System-ID-GUID    | 93c7b477-1f2e-4b40-b7bf-007e8d038ccf        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Verdadeiro                                                         |
| É indexado             | Falso                                                        |
| No catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 32767                                                        |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x00000000                                                   |
| Classes usadas em        | [**MS-DFSR-Contentset**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | Falso                                                                                                                                 |
| É de valor único       | Verdadeiro                                                                                                                                  |
| É indexado             | Falso                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                          |
| Range-Lower            | 0                                                                                                                                     |
| Range-Upper            | 32767                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Classes usadas em        | [**MS-DFSR-telereplication**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-Contentset**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | Falso                                                                                                                                 |
| É de valor único       | Verdadeiro                                                                                                                                  |
| É indexado             | Falso                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                          |
| Range-Lower            | 0                                                                                                                                     |
| Range-Upper            | 32767                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Classes usadas em        | [**ms-DFSR-ReplicationGroup**](c-msdfsr-replicationgroup.md)<br/> [**ms-DFSR-ContentSet**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | Falso                                                                                                                                 |
| Tem valor único       | Verdadeiro                                                                                                                                  |
| É indexado             | Falso                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                          |
| Range-Lower            | 0                                                                                                                                     |
| Range-Upper            | 32767                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Classes usadas em        | [**ms-DFSR-ReplicationGroup**](c-msdfsr-replicationgroup.md)<br/> [**ms-DFSR-ContentSet**](c-msdfsr-contentset.md)<br/> |



## <a name="remarks"></a>Comentários

O **atributo ms-DFSR-DirectoryFilter** faz parte do suporte ao serviço de replicação Sistema de Arquivos Distribuído (DFS).

 

 





