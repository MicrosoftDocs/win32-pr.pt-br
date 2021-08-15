---
title: Atributo System-May-Contain
description: A lista de atributos opcionais para uma classe. A lista de atributos só pode ser modificada pelo sistema.
ms.assetid: b2fbeb64-d147-4c1a-a609-4f16327609ce
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo System-May-Contain
- Esquema do AD do atributo systemMayContain
topic_type:
- apiref
api_name:
- System-May-Contain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62b537cc08c156e16304a49cc8782d7ca8fd54341a0b24f235a895a765a45671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081370"
---
# <a name="system-may-contain-attribute"></a>Atributo System-May-Contain

A lista de atributos opcionais para uma classe. A lista de atributos só pode ser modificada pelo sistema.



| Entrada | Valor |
|-------------------|------------------------------------------------------------------------------|
| CN                | System-May-Contain                                                           |
| Ldap-Display-Name | systemMayContain                                                             |
| Tamanho              | \-                                                                           |
| Privilégio de atualização  | Administrador de esquema                                                         |
| Frequência de atualização  | Quando a classe é criada ou um novo atributo opcional é adicionado à classe . |
| Attribute-Id      | 1.2.840.113556.1.4.196                                                       |
| System-Id-Guid    | bf967a44-0de6-11d0-a285-00aa003049e2                                         |
| Syntax            | [**String(Object-Identifier)**](s-string-object-identifier.md)              |



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
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Verdadeiro                                             |
| Tem valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Verdadeiro                                             |
| Tem valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Verdadeiro                                             |
| Tem valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Verdadeiro                                             |
| É de valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Verdadeiro                                             |
| É de valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Verdadeiro                                             |
| É de valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Verdadeiro                                             |
| É de valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**Esquema de classe**](c-classschema.md)<br/> |



 

 





