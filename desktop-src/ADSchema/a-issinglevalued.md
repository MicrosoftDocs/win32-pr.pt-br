---
title: É um atributo de valor único
description: Se for TRUE, esse atributo só poderá armazenar um valor.
ms.assetid: 53dd8dfe-2123-4a61-a346-12abe340ea11
ms.tgt_platform: multiple
keywords:
- É um esquema de AD de atributo de valor único
- Esquema de AD do atributo isSingleValued
topic_type:
- apiref
api_name:
- Is-Single-Valued
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1677a5a9b412e315be8ec773f8d0b1cc54f341622d2129ca7f6f80252cc950a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119303936"
---
# <a name="is-single-valued-attribute"></a>É um atributo de valor único

Se **for true**, esse atributo só poderá armazenar um valor.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | É de valor único                     |
| LDAP-Display-Name | isSingleValued                       |
| Tamanho              | \-                                   |
| Privilégio de atualização  | Administrador de esquema                 |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.2.33                |
| System-ID-GUID    | bf967992-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Boolean**](s-boolean.md)         |



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
| MAPI-Id                | 0x80C1                                                   |
| System-Only            | Verdadeiro                                                     |
| É de valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x80C1                                                   |
| System-Only            | Verdadeiro                                                     |
| É de valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x80C1                                                   |
| System-Only            | Verdadeiro                                                     |
| É de valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Esquema de atributo**](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x80C1                                                   |
| System-Only            | Verdadeiro                                                     |
| Tem valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Esquema de atributo**](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x80C1                                                   |
| System-Only            | Verdadeiro                                                     |
| Tem valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Esquema de atributo**](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x80C1                                                   |
| System-Only            | Verdadeiro                                                     |
| Tem valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Esquema de atributo**](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x80C1                                                   |
| System-Only            | Verdadeiro                                                     |
| Tem valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Esquema de atributo**](c-attributeschema.md)<br/> |



 

 





