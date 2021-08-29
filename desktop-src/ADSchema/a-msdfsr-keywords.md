---
title: Atributo ms-DFSR-Keywords
description: Contém as palavras-chave definidas pelo usuário.
ms.assetid: 0721c939-3cbc-440f-a13e-f9919ce62471
ms.tgt_platform: multiple
keywords:
- Atributo ms-DFSR-Keywords Esquema do AD
- Atributo msDFSR-Keywords Esquema do AD
topic_type:
- apiref
api_name:
- ms-DFSR-Keywords
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2975203ccf1d95b29a117360a2394f1c7f9b35fc999eec30c2cae7774a5673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960935"
---
# <a name="ms-dfsr-keywords-attribute"></a>Atributo ms-DFSR-Keywords

Contém as palavras-chave definidas pelo usuário.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | palavras-chave ms-DFSR                            |
| Ldap-Display-Name | Palavras-chave msDFSR                             |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.6.13.3.15                  |
| System-Id-Guid    | 048b4692-6227-4b67-a074-c4437083e14b        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No Catálogo Global      | Falso                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | 0                                                                                                                 |
| Range-Upper            | 32767                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000000                                                                                                        |
| Classes usadas em        | [**ms-DFSR-Member**](c-msdfsr-member.md)<br/> [**ms-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No Catálogo Global      | Falso                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | 0                                                                                                                 |
| Range-Upper            | 32767                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000000                                                                                                        |
| Classes usadas em        | [**ms-DFSR-Member**](c-msdfsr-member.md)<br/> [**ms-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Tem valor único       | Verdadeiro                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No Catálogo Global      | Falso                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | 0                                                                                                                 |
| Range-Upper            | 32767                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000000                                                                                                        |
| Classes usadas em        | [**MS-DFSR-Member**](c-msdfsr-member.md)<br/> [**MS-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| É de valor único       | Verdadeiro                                                                                                              |
| É indexado             | Falso                                                                                                             |
| No catálogo global      | Falso                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                      |
| Range-Lower            | 0                                                                                                                 |
| Range-Upper            | 32767                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000000                                                                                                        |
| Classes usadas em        | [**MS-DFSR-Member**](c-msdfsr-member.md)<br/> [**MS-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="remarks"></a>Comentários

O atributo **MS-DFSR-Keywords** faz parte do suporte ao serviço de replicação do sistema de arquivos distribuído (DFS).

 

 





