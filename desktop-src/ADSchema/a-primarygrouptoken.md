---
title: Atributo Primary-Group-Token
description: Um atributo computado que é usado para recuperar a lista de associação de um grupo, como Usuários de Domínio. A associação completa desses grupos não é armazenada explicitamente por motivos de dimensionamento.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Primary-Group-Token
- Esquema do AD do atributo primaryGroupToken
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd83e89a25a81f6d62207e48053fff5cafd279e29b482a9b80cb02de580ad3fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065916"
---
# <a name="primary-group-token-attribute"></a>Atributo Primary-Group-Token

Um atributo computado que é usado para recuperar a lista de associação de um grupo, como Usuários de Domínio. A associação completa desses grupos não é armazenada explicitamente por motivos de dimensionamento.



| Entrada | Valor |
|-------------------|--------------------------------------------|
| CN                | Primary-Group-Token                        |
| Ldap-Display-Name | primaryGroupToken                          |
| Tamanho              | 4 bytes                                    |
| Privilégio de atualização  | Esse valor é definido pelo sistema.           |
| Frequência de atualização  | Sempre que um grupo primário de objetos é mudar. |
| Attribute-Id      | 1.2.840.113556.1.4.1412                    |
| System-Id-Guid    | c0ed8738-7efd-4481-84d9-66d2db8be369       |
| Syntax            | [**Enumeração**](s-enumeration.md)       |



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
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadeiro                                |
| Tem valor único       | Verdadeiro                                |
| É indexado             | Falso                               |
| No Catálogo Global      | Falso                               |
| Descritor de segurança NT | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadeiro                                |
| Tem valor único       | Verdadeiro                                |
| É indexado             | Falso                               |
| No Catálogo Global      | Falso                               |
| Descritor de segurança NT | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadeiro                                |
| Tem valor único       | Verdadeiro                                |
| É indexado             | Falso                               |
| No Catálogo Global      | Falso                               |
| Descritor de segurança NT | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadeiro                                |
| Tem valor único       | Verdadeiro                                |
| É indexado             | Falso                               |
| No Catálogo Global      | Falso                               |
| Descritor de segurança NT | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadeiro                                |
| Tem valor único       | Verdadeiro                                |
| É indexado             | Falso                               |
| No Catálogo Global      | Falso                               |
| Descritor de segurança NT | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadeiro                                |
| Tem valor único       | Verdadeiro                                |
| É indexado             | Falso                               |
| No Catálogo Global      | Falso                               |
| Descritor de segurança NT | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadeiro                                |
| Tem valor único       | Verdadeiro                                |
| É indexado             | Falso                               |
| No Catálogo Global      | Falso                               |
| Descritor de segurança NT | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Grupo**](c-group.md)<br/> |



 

 





