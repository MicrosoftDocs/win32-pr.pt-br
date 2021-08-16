---
title: atributo ms-DFSR-DfsPath
description: Contém o caminho completo do link Sistema de Arquivos Distribuído (DFS) associado.
ms.assetid: bd596110-b156-4640-a6d0-ace9e4e30909
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DFSR-DfsPath
- Esquema de AD do atributo msDFSR-DfsPath
topic_type:
- apiref
api_name:
- ms-DFSR-DfsPath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a8f1e1ae9f9baeaa134737d5f6b84777f99c283f7f7013828483b2e6751b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960965"
---
# <a name="ms-dfsr-dfspath-attribute"></a>atributo ms-DFSR-DfsPath

Contém o caminho completo do link Sistema de Arquivos Distribuído (DFS) associado para suporte ao serviço Replicação do DFS.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | MS-DFSR-DfsPath                             |
| LDAP-Display-Name | msDFSR-DfsPath                              |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.6.13.3.21                  |
| System-ID-GUID    | 2cc903e2-398c-443b-ac86-ff6b01eac7ba        |
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
| É indexado             | Verdadeiro                                                         |
| No catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 32767                                                        |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000000                                                   |
| Classes usadas em        | [**MS-DFSR-Contentset**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Verdadeiro                                                         |
| É indexado             | Verdadeiro                                                         |
| No catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 32767                                                        |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000000                                                   |
| Classes usadas em        | [**MS-DFSR-Contentset**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| É de valor único       | Verdadeiro                                                         |
| É indexado             | Verdadeiro                                                         |
| No catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 32767                                                        |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000000                                                   |
| Classes usadas em        | [**ms-DFSR-ContentSet**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------------------|
| ID do link                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Tem valor único       | Verdadeiro                                                         |
| É indexado             | Verdadeiro                                                         |
| No Catálogo Global      | Falso                                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 32767                                                        |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000000                                                   |
| Classes usadas em        | [**ms-DFSR-ContentSet**](c-msdfsr-contentset.md)<br/> |



## <a name="remarks"></a>Comentários

O **atributo ms-DFSR-DfsPath** faz parte do suporte ao serviço de replicação Sistema de Arquivos Distribuído (DFS).

 

 





