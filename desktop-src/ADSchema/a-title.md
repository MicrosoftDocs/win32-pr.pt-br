---
title: Atributo de título
description: Contém o cargo do usuário. Essa propriedade é normalmente usada para indicar o cargo formal, como programador sênior, em vez de classe de ocupação, como programador. Normalmente, ele não é usado para títulos de sufixo, como esq. ou DDS.
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- Atributo de título esquema do AD
- atributo de título esquema do AD
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbb4dae862db9fc363b22647bd5e56a98e9e60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825262"
---
# <a name="title-attribute-ad-schema"></a>Atributo Title (esquema do AD)

Contém o cargo do usuário. Essa propriedade é normalmente usada para indicar o cargo formal, como programador sênior, em vez de classe de ocupação, como programador. Normalmente, ele não é usado para títulos de sufixo, como esq. ou DDS.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------|
| CN                | Título                                                                     |
| LDAP-Display-Name | título                                                                     |
| Tamanho              | \-                                                                        |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                    |
| Frequência de atualização  | Quando o registro do usuário é criado e sempre que o título precisa ser alterado. |
| Attribute-Id      | 2.5.4.12                                                                  |
| System-ID-GUID    | bf967a55-0de6-11d0-a285-00aa003049e2                                      |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                               |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| É de valor único       | True                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| É de valor único       | True                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| É de valor único       | True                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| É de valor único       | True                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| É de valor único       | True                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| É de valor único       | True                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



 

 





