---
title: Atributo Last-Update-Sequence
description: Esse atributo contém o número da sequência de atualização para o último item no armazenamento de classes que foi alterado.
ms.assetid: fd434b8d-31b4-45f7-8d8f-048f61cabb92
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Last-Update-Sequence
- Esquema do AD do atributo lastUpdateSequence
topic_type:
- apiref
api_name:
- Last-Update-Sequence
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5ff31db81cbdbc1767c05cb2f4c7d366ad685c39cd873f15d2a113eb5b2dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924686"
---
# <a name="last-update-sequence-attribute"></a>Atributo Last-Update-Sequence

Esse atributo contém o número da sequência de atualização para o último item no armazenamento de classes que foi alterado.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Sequência de última atualização                        |
| Ldap-Display-Name | lastUpdateSequence                          |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.330                      |
| System-Id-Guid    | 7d6c0e9c-7e20-11d0-afd6-00c04fd930c9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                              |
| MAPI-Id                | \-                                                                                                              |
| System-Only            | Falso                                                                                                           |
| Tem valor único       | Verdadeiro                                                                                                            |
| É indexado             | Falso                                                                                                           |
| No Catálogo Global      | Falso                                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                    |
| Range-Lower            | \-                                                                                                              |
| Range-Upper            | \-                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                      |
| System-Flags           | 0x00000010                                                                                                      |
| Classes usadas em        | [**Class-Store**](c-classstore.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                              |
| MAPI-Id                | \-                                                                                                              |
| System-Only            | Falso                                                                                                           |
| Tem valor único       | Verdadeiro                                                                                                            |
| É indexado             | Falso                                                                                                           |
| No Catálogo Global      | Falso                                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                    |
| Range-Lower            | \-                                                                                                              |
| Range-Upper            | \-                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                      |
| System-Flags           | 0x00000010                                                                                                      |
| Classes usadas em        | [**Class-Store**](c-classstore.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                              |
| MAPI-Id                | \-                                                                                                              |
| System-Only            | Falso                                                                                                           |
| Tem valor único       | Verdadeiro                                                                                                            |
| É indexado             | Falso                                                                                                           |
| No Catálogo Global      | Falso                                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                    |
| Range-Lower            | \-                                                                                                              |
| Range-Upper            | \-                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                      |
| System-Flags           | 0x00000010                                                                                                      |
| Classes usadas em        | [**Class-Store**](c-classstore.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                              |
| MAPI-Id                | \-                                                                                                              |
| System-Only            | Falso                                                                                                           |
| É de valor único       | Verdadeiro                                                                                                            |
| É indexado             | Falso                                                                                                           |
| No catálogo global      | Falso                                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                    |
| Range-Lower            | \-                                                                                                              |
| Range-Upper            | \-                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                      |
| System-Flags           | 0x00000010                                                                                                      |
| Classes usadas em        | [**Armazenamento de classe**](c-classstore.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                              |
| MAPI-Id                | \-                                                                                                              |
| System-Only            | Falso                                                                                                           |
| É de valor único       | Verdadeiro                                                                                                            |
| É indexado             | Falso                                                                                                           |
| No catálogo global      | Falso                                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                    |
| Range-Lower            | \-                                                                                                              |
| Range-Upper            | \-                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                      |
| System-Flags           | 0x00000010                                                                                                      |
| Classes usadas em        | [**Armazenamento de classe**](c-classstore.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                              |
| MAPI-Id                | \-                                                                                                              |
| System-Only            | Falso                                                                                                           |
| É de valor único       | Verdadeiro                                                                                                            |
| É indexado             | Falso                                                                                                           |
| No catálogo global      | Falso                                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                    |
| Range-Lower            | \-                                                                                                              |
| Range-Upper            | \-                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                      |
| System-Flags           | 0x00000010                                                                                                      |
| Classes usadas em        | [**Armazenamento de classe**](c-classstore.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> |



 

 





