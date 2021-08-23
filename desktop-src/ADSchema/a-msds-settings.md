---
title: Atributo ms-DS-Configurações
description: Usado para armazenar configurações para um objeto . Seu uso é determinado exclusivamente pelo proprietário do objeto. É recomendável usá-lo para armazenar pares de nome/valor. Por exemplo, cor azul.
ms.assetid: 44e3a9e2-5528-4328-9cb7-1b6a4a77950a
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo ms-DS-Configurações
- Esquema do AD do atributo msDS-Configurações
topic_type:
- apiref
api_name:
- ms-DS-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd39e64c096049bb39379aa48d97444982e51746808ae59987e4ddcad2de30c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544566"
---
# <a name="ms-ds-settings-attribute"></a>Atributo ms-DS-Configurações

Usado para armazenar configurações para um objeto . Seu uso é determinado exclusivamente pelo proprietário do objeto. É recomendável usá-lo para armazenar pares de nome/valor. Por exemplo, color=blue.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | ms-DS-Configurações                              |
| Ldap-Display-Name | msDS-Configurações                               |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio                        |
| Frequência de atualização  | Cada vez que os valores de configurações são alterados.       |
| Attribute-Id      | 1.2.840.113556.1.4.1697                     |
| System-Id-Guid    | 0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | Falso                                                                                                                     |
| Tem valor único       | Falso                                                                                                                     |
| É indexado             | Falso                                                                                                                     |
| No Catálogo Global      | Falso                                                                                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                              |
| Range-Lower            | \-                                                                                                                        |
| Range-Upper            | \-                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000000                                                                                                                |
| Classes usadas em        | [**Aplicativos Configurações**](c-applicationsettings.md)<br/> [**Ponto de conexão**](c-connectionpoint.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| Tem valor único       | Falso                                                            |
| É indexado             | Falso                                                            |
| No Catálogo Global      | Falso                                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000000                                                       |
| Classes usadas em        | [**Aplicativos Configurações**](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | Falso                                                                                                                     |
| Tem valor único       | Falso                                                                                                                     |
| É indexado             | Falso                                                                                                                     |
| No Catálogo Global      | Falso                                                                                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                              |
| Range-Lower            | \-                                                                                                                        |
| Range-Upper            | \-                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000000                                                                                                                |
| Classes usadas em        | [**Configurações do aplicativo**](c-applicationsettings.md)<br/> [**Ponto de conexão**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | Falso                                                                                                                     |
| É de valor único       | Falso                                                                                                                     |
| É indexado             | Falso                                                                                                                     |
| No catálogo global      | Falso                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                              |
| Range-Lower            | \-                                                                                                                        |
| Range-Upper            | \-                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000000                                                                                                                |
| Classes usadas em        | [**Configurações do aplicativo**](c-applicationsettings.md)<br/> [**Ponto de conexão**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | Falso                                                                                                                     |
| É de valor único       | Falso                                                                                                                     |
| É indexado             | Falso                                                                                                                     |
| No catálogo global      | Falso                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                              |
| Range-Lower            | \-                                                                                                                        |
| Range-Upper            | \-                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000000                                                                                                                |
| Classes usadas em        | [**Configurações do aplicativo**](c-applicationsettings.md)<br/> [**Ponto de conexão**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | Falso                                                                                                                     |
| É de valor único       | Falso                                                                                                                     |
| É indexado             | Falso                                                                                                                     |
| No catálogo global      | Falso                                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                              |
| Range-Lower            | \-                                                                                                                        |
| Range-Upper            | \-                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000000                                                                                                                |
| Classes usadas em        | [**Configurações do aplicativo**](c-applicationsettings.md)<br/> [**Ponto de conexão**](c-connectionpoint.md)<br/> |



 

 





