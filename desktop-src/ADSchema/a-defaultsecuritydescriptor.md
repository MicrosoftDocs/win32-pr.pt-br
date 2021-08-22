---
title: Padrão-atributo de descritor de segurança
description: O descritor de segurança a ser atribuído ao objeto quando ele é criado pela primeira vez.
ms.assetid: 22575883-2ef3-492b-9868-1eb350c4f547
ms.tgt_platform: multiple
keywords:
- Padrão-Security-Descriptor atributo AD Schema
- Esquema de AD do atributo defaultSecurityDescriptor
topic_type:
- apiref
api_name:
- Default-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71610e0f970962e8145808d3e4038306dc955ea631f07112b8eb4b57c13e5f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509066"
---
# <a name="default-security-descriptor-attribute"></a>Padrão-atributo de descritor de segurança

O descritor de segurança a ser atribuído ao objeto quando ele é criado pela primeira vez.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Padrão-descritor de segurança                 |
| LDAP-Display-Name | defaultSecurityDescriptor                   |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de esquema                        |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.224                      |
| System-ID-GUID    | 807a6d30-1669-11d0-a064-00aa006c33ed        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



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
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| É de valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| É de valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| É de valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Tem valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Tem valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Tem valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Tem valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



 

 





