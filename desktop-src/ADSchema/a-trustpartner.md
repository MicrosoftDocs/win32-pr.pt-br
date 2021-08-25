---
title: Trust-Partner atributo
description: O nome do domínio com o qual existe uma relação de confiança.
ms.assetid: 0b7c8e78-614b-46dd-8616-40d75b461639
ms.tgt_platform: multiple
keywords:
- Esquema de Trust-Partner do atributo AD
- Esquema de AD do atributo trustPartner
topic_type:
- apiref
api_name:
- Trust-Partner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ce551bbf23c7eec378088a0a8d9a9ced25612e40cae1766c55099bb4e45b31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835436"
---
# <a name="trust-partner-attribute"></a>Trust-Partner atributo

O nome do domínio com o qual existe uma relação de confiança.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Trust-Partner                               |
| LDAP-Display-Name | trustPartner                                |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Esse valor é definido pelo sistema.            |
| Frequência de atualização  | Quando uma nova relação de confiança é criada.                |
| Attribute-Id      | 1.2.840.113556.1.4.133                      |
| System-ID-GUID    | bf967a5d-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Verdadeiro                                                 |
| No catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Verdadeiro                                                 |
| No catálogo global      | Verdadeiro                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | Verdadeiro                                                 |
| É indexado             | Verdadeiro                                                 |
| No catálogo global      | Verdadeiro                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Verdadeiro                                                 |
| No Catálogo Global      | Verdadeiro                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Verdadeiro                                                 |
| No Catálogo Global      | Verdadeiro                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Verdadeiro                                                 |
| No Catálogo Global      | Verdadeiro                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



 

 





