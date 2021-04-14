---
title: Outro atributo-well-known-Objects
description: Contém uma lista de contêineres por GUID e nome diferenciado. Isso permite recuperar um objeto depois que ele é movido usando apenas o GUID e o nome de domínio. Sempre que o objeto for movido, o sistema atualizará automaticamente o nome distinto.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- Outro esquema do AD do atributo de objeto bem conhecido
- Esquema de AD do atributo otherWellKnownObjects
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456261"
---
# <a name="other-well-known-objects-attribute"></a>Outro atributo-well-known-Objects

Contém uma lista de contêineres por GUID e nome diferenciado. Isso permite recuperar um objeto depois que ele é movido usando apenas o GUID e o nome de domínio. Sempre que o objeto for movido, o sistema atualizará automaticamente o nome distinto.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Outros objetos bem conhecidos                                                                                                                                                                                      |
| LDAP-Display-Name | otherWellKnownObjects                                                                                                                                                                                         |
| Tamanho              | Exemplo para recuperar o contêiner de usuários no domínio da Microsoft: LDAP://(WKGUID = a9d1ca15768811d1aded00c04fd8d5cd, DC = Microsoft, DC = com). Observação: colchetes angulares substituídos por parênteses para evitar conflitos XML. |
| Privilégio de atualização  | Administrador de esquema                                                                                                                                                                                          |
| Frequência de atualização  | Sempre que o objeto for movido.                                                                                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1359                                                                                                                                                                                       |
| System-ID-GUID    | 1ea64e5d-ac0f-11d2-90df-00c04fd91ab1                                                                                                                                                                          |
| Syntax            | [**Objeto (DN-binário)**](s-object-dn-binary.md)                                                                                                                                                               |



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
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



 

 





