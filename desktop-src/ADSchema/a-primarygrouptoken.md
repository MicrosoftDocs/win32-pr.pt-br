---
title: Atributo Primary-Group-token
description: Um atributo calculado que é usado na recuperação da lista de membros de um grupo, como usuários de domínio. A associação completa desses grupos não é armazenada explicitamente por motivos de dimensionamento.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Grupo de identificadores primários de atributos de token
- Esquema de AD do atributo primaryGroupToken
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b237ab5998ca3f38f2d07128b36d9337c96935d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086865"
---
# <a name="primary-group-token-attribute"></a>Atributo Primary-Group-token

Um atributo calculado que é usado na recuperação da lista de membros de um grupo, como usuários de domínio. A associação completa desses grupos não é armazenada explicitamente por motivos de dimensionamento.



| Entrada | Valor |
|-------------------|--------------------------------------------|
| CN                | Token de grupo primário                        |
| LDAP-Display-Name | primaryGroupToken                          |
| Tamanho              | 4 bytes                                    |
| Privilégio de atualização  | Esse valor é definido pelo sistema.           |
| Frequência de atualização  | Sempre que um grupo primário de objetos é alterado. |
| Attribute-Id      | 1.2.840.113556.1.4.1412                    |
| System-ID-GUID    | c0ed8738-7efd-4481-84d9-66d2db8be369       |
| Syntax            | [**Enumeração**](s-enumeration.md)       |



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
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| É de valor único       | True                                |
| É indexado             | Falso                               |
| No catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| É de valor único       | True                                |
| É indexado             | Falso                               |
| No catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Group**](c-group.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| É de valor único       | True                                |
| É indexado             | Falso                               |
| No catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| É de valor único       | True                                |
| É indexado             | Falso                               |
| No catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| É de valor único       | True                                |
| É indexado             | Falso                               |
| No catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| É de valor único       | True                                |
| É indexado             | Falso                               |
| No catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------|
| ID do link                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| É de valor único       | True                                |
| É indexado             | Falso                               |
| No catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes usadas em        | [**Group**](c-group.md)<br/> |



 

 





