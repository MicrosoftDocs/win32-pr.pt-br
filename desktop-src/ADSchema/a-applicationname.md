---
title: Application-Name atributo
description: O nome do aplicativo.
ms.assetid: ebcbae00-04bd-40be-b256-8e27611eee22
ms.tgt_platform: multiple
keywords:
- Esquema de Application-Name do atributo AD
- Esquema de AD do atributo applicationName
topic_type:
- apiref
api_name:
- Application-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248c852919b934c219fe7037e06ab46b2921594b8dd91239a1d536788e3276f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178025"
---
# <a name="application-name-attribute"></a>Application-Name atributo

O nome do aplicativo.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Nome do aplicativo                            |
| LDAP-Display-Name | applicationName                             |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio                        |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.218                      |
| System-ID-GUID    | dd712226-10e4-11d0-a05f-00aa006c33ed        |
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
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falso                                                                                                                                      |
| É de valor único       | True                                                                                                                                       |
| É indexado             | Falso                                                                                                                                      |
| No catálogo global      | Falso                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                               |
| Range-Lower            | 1                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Classes usadas em        | [**Configurações do aplicativo**](c-applicationsettings.md)<br/> [**aplicativo-Configurações de Site**](c-applicationsitesettings.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falso                                                                                                                                      |
| É de valor único       | True                                                                                                                                       |
| É indexado             | Falso                                                                                                                                      |
| No catálogo global      | Falso                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                               |
| Range-Lower            | 1                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Classes usadas em        | [**Configurações do aplicativo**](c-applicationsettings.md)<br/> [**aplicativo-Configurações de Site**](c-applicationsitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falso                                                                                                                                      |
| É de valor único       | True                                                                                                                                       |
| É indexado             | Falso                                                                                                                                      |
| No catálogo global      | Falso                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                               |
| Range-Lower            | 1                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Classes usadas em        | [**Aplicativos Configurações**](c-applicationsettings.md)<br/> [**Application-Site-Configurações**](c-applicationsitesettings.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falso                                                                                                                                      |
| Tem valor único       | True                                                                                                                                       |
| É indexado             | Falso                                                                                                                                      |
| No Catálogo Global      | Falso                                                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | 1                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Classes usadas em        | [**Aplicativos Configurações**](c-applicationsettings.md)<br/> [**Application-Site-Configurações**](c-applicationsitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falso                                                                                                                                      |
| Tem valor único       | True                                                                                                                                       |
| É indexado             | Falso                                                                                                                                      |
| No Catálogo Global      | Falso                                                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | 1                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Classes usadas em        | [**Aplicativos Configurações**](c-applicationsettings.md)<br/> [**Application-Site-Configurações**](c-applicationsitesettings.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                         |
| System-Only            | Falso                                                                                                                                      |
| Tem valor único       | True                                                                                                                                       |
| É indexado             | Falso                                                                                                                                      |
| No Catálogo Global      | Falso                                                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | 1                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Classes usadas em        | [**Aplicativos Configurações**](c-applicationsettings.md)<br/> [**Application-Site-Configurações**](c-applicationsitesettings.md)<br/> |



 

 





