---
title: Atributo admin-MultiSelect-Property-Pages
description: Esse é um atributo COM vários valores cujos são um número que representa a ordem na qual as páginas são adicionadas e um GUID de um objeto COM que implementa páginas de propriedades de seleção múltipla para o snap-in usuários e computadores do AD.
ms.assetid: b2b4aafe-ac2d-44b3-80eb-910ba9852bb0
ms.tgt_platform: multiple
keywords:
- Administrador-MultiSelect-Property-Pages atributo AD Schema
- Esquema de AD do atributo adminMultiselectPropertyPages
topic_type:
- apiref
api_name:
- Admin-Multiselect-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed42d2383d194ca417a381da8ef0e849b4d4b6b93665fd7d360df2829f7e0d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118688390"
---
# <a name="admin-multiselect-property-pages-attribute"></a>Atributo admin-MultiSelect-Property-Pages

Esse é um atributo COM vários valores cujos são um número que representa a ordem na qual as páginas são adicionadas e um GUID de um objeto COM que implementa páginas de propriedades de seleção múltipla para o snap-in usuários e computadores do AD.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Admin – MultiSelect-Property-Pages                                                                                                            |
| LDAP-Display-Name | adminMultiselectPropertyPages                                                                                                               |
| Tamanho              | 40 bytes                                                                                                                                    |
| Privilégio de atualização  | Administrador de domínio                                                                                                                        |
| Frequência de atualização  | isso só será atualizado se um serviço, como Exchange ou Terminal Server estiver instalado, que implemente suas próprias páginas de propriedades de seleção múltipla. |
| Attribute-Id      | 1.2.840.113556.1.4.1690                                                                                                                     |
| System-ID-GUID    | 18f9b67d-5ac6-4b3b-97db-d0a406afb7ba                                                                                                        |
| Sintaxe            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                                                                                 |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| ID do link                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| É de valor único       | Falso                                                      |
| É indexado             | Falso                                                      |
| No catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes usadas em        | [**Especificador de exibição**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| ID do link                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| É de valor único       | Falso                                                      |
| É indexado             | Falso                                                      |
| No catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes usadas em        | [**Especificador de exibição**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| ID do link                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| É de valor único       | Falso                                                      |
| É indexado             | Falso                                                      |
| No catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes usadas em        | [**Especificador de exibição**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| ID do link                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Tem valor único       | Falso                                                      |
| É indexado             | Falso                                                      |
| No Catálogo Global      | Falso                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes usadas em        | [**Especificador de exibição**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| ID do link                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Tem valor único       | Falso                                                      |
| É indexado             | Falso                                                      |
| No Catálogo Global      | Falso                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes usadas em        | [**Especificador de exibição**](c-displayspecifier.md)<br/> |



 

 





