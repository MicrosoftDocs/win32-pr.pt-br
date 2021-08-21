---
title: Rights-Guid atributo
description: O GUID usado para representar um direito estendido dentro de uma entrada de controle de acesso.
ms.assetid: 6f3a654e-fead-41e7-8383-6dade1a2747e
ms.tgt_platform: multiple
keywords:
- Esquema de Rights-Guid do atributo AD
- Esquema de AD do atributo rightsGuid
topic_type:
- apiref
api_name:
- Rights-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057ede64b269e607e9f8e7f914756dd541b7d1d473bc0628c490d5b7fccb618d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681717"
---
# <a name="rights-guid-attribute"></a>Rights-Guid atributo

O GUID usado para representar um direito estendido dentro de uma entrada de controle de acesso.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Rights-Guid                                 |
| LDAP-Display-Name | rightsGuid                                  |
| Tamanho              | 16 bytes                                    |
| Privilégio de atualização  | Esse valor é definido pelo sistema.            |
| Frequência de atualização  | Quando um novo direito estendido é criado.       |
| Attribute-Id      | 1.2.840.113556.1.4.340                      |
| System-ID-GUID    | 8297931c-86d3-11d0-afda-00c04fd930c9        |
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
|------------------------|-----------------------------------------------------------------|
| ID do link                | \-                                                              |
| MAPI-Id                | \-                                                              |
| System-Only            | Falso                                                           |
| É de valor único       | Verdadeiro                                                            |
| É indexado             | Falso                                                           |
| No catálogo global      | Falso                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                    |
| Range-Lower            | 36                                                              |
| Range-Upper            | 36                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Controle-acesso-à direita**](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------|
| ID do link                | \-                                                              |
| MAPI-Id                | \-                                                              |
| System-Only            | Falso                                                           |
| É de valor único       | Verdadeiro                                                            |
| É indexado             | Falso                                                           |
| No catálogo global      | Falso                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                    |
| Range-Lower            | 36                                                              |
| Range-Upper            | 36                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Controle-acesso-à direita**](c-controlaccessright.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------|
| ID do link                | \-                                                              |
| MAPI-Id                | \-                                                              |
| System-Only            | Falso                                                           |
| É de valor único       | Verdadeiro                                                            |
| É indexado             | Falso                                                           |
| No catálogo global      | Falso                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                    |
| Range-Lower            | 36                                                              |
| Range-Upper            | 36                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Controle-acesso-à direita**](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------|
| ID do link                | \-                                                              |
| MAPI-Id                | \-                                                              |
| System-Only            | Falso                                                           |
| É de valor único       | Verdadeiro                                                            |
| É indexado             | Falso                                                           |
| No catálogo global      | Falso                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                    |
| Range-Lower            | 36                                                              |
| Range-Upper            | 36                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Controle-acesso-à direita**](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------|
| ID do link                | \-                                                              |
| MAPI-Id                | \-                                                              |
| System-Only            | Falso                                                           |
| É de valor único       | Verdadeiro                                                            |
| É indexado             | Falso                                                           |
| No catálogo global      | Falso                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                    |
| Range-Lower            | 36                                                              |
| Range-Upper            | 36                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Controle-acesso-à direita**](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------|
| ID do link                | \-                                                              |
| MAPI-Id                | \-                                                              |
| System-Only            | Falso                                                           |
| É de valor único       | Verdadeiro                                                            |
| É indexado             | Falso                                                           |
| No catálogo global      | Falso                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                    |
| Range-Lower            | 36                                                              |
| Range-Upper            | 36                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Controle-acesso-à direita**](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------|
| ID do link                | \-                                                              |
| MAPI-Id                | \-                                                              |
| System-Only            | Falso                                                           |
| É de valor único       | Verdadeiro                                                            |
| É indexado             | Falso                                                           |
| No catálogo global      | Falso                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                    |
| Range-Lower            | 36                                                              |
| Range-Upper            | 36                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Control-Access-Right**](c-controlaccessright.md)<br/> |



 

 





