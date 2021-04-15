---
title: Atributo inicials
description: Contém as iniciais de partes do nome completo do usuário. Isso pode ser usado como a inicial do meio no catálogo de endereços do Windows.
ms.assetid: 220b4448-5276-4c3f-8a1b-217cec06135a
ms.tgt_platform: multiple
keywords:
- Esquema do atributo do AD de iniciais
- Esquema do atributo do AD de iniciais
topic_type:
- apiref
api_name:
- Initials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 946f6c9633c1126a30ae4898274096a54db9a402
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105753658"
---
# <a name="initials-attribute"></a>Atributo inicials

Contém as iniciais de partes do nome completo do usuário. Isso pode ser usado como a inicial do meio no catálogo de endereços do Windows.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Iniciais                                    |
| LDAP-Display-Name | Initials                                    |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.      |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 2.5.4.43                                    |
| System-ID-GUID    | f0f8ff90-1191-11d0-a060-00aa006c33ed        |
| Sintaxe            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------|
| ID do link                | \-                                                                 |
| MAPI-Id                | 0x3A0A                                                             |
| System-Only            | Falso                                                              |
| É de valor único       | True                                                               |
| É indexado             | Falso                                                              |
| No catálogo global      | Falso                                                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 6                                                                  |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| É de valor único       | True                                                                                                                   |
| É indexado             | Falso                                                                                                                  |
| No catálogo global      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| É de valor único       | True                                                                                                                   |
| É indexado             | Falso                                                                                                                  |
| No catálogo global      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| É de valor único       | True                                                                                                                   |
| É indexado             | Falso                                                                                                                  |
| No catálogo global      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| É de valor único       | True                                                                                                                   |
| É indexado             | Falso                                                                                                                  |
| No catálogo global      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| É de valor único       | True                                                                                                                   |
| É indexado             | Falso                                                                                                                  |
| No catálogo global      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





