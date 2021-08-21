---
title: Valid-Accesses atributo
description: O tipo de acesso permitido com um direito estendido.
ms.assetid: afb944ec-3b8f-41dd-8987-ed6c71f937ac
ms.tgt_platform: multiple
keywords:
- Esquema de Valid-Accesses do atributo AD
- Esquema de AD do atributo validAccesses
topic_type:
- apiref
api_name:
- Valid-Accesses
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98dcf686bf3f15af8ba2129a0bd0cdbb9c01133b9fc6d4531155a065c07a44fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081290"
---
# <a name="valid-accesses-attribute"></a>Valid-Accesses atributo

O tipo de acesso permitido com um direito estendido.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Valid-Accesses                       |
| LDAP-Display-Name | validAccesses                        |
| Tamanho              | \-                                   |
| Privilégio de atualização  | Criador de objeto                       |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1356              |
| System-ID-GUID    | 4d2fa380-7f54-11d2-992a-0000f87a57d4 |
| Syntax            | [**Enumeração**](s-enumeration.md) |



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
| Range-Lower            | \-                                                              |
| Range-Upper            | \-                                                              |
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
| Range-Lower            | \-                                                              |
| Range-Upper            | \-                                                              |
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
| Range-Lower            | \-                                                              |
| Range-Upper            | \-                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Controle-acesso-à direita**](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------|
| ID do link                | \-                                                              |
| MAPI-Id                | \-                                                              |
| System-Only            | Falso                                                           |
| Tem valor único       | Verdadeiro                                                            |
| É indexado             | Falso                                                           |
| No Catálogo Global      | Falso                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                    |
| Range-Lower            | \-                                                              |
| Range-Upper            | \-                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Control-Access-Right**](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------|
| ID do link                | \-                                                              |
| MAPI-Id                | \-                                                              |
| System-Only            | Falso                                                           |
| Tem valor único       | Verdadeiro                                                            |
| É indexado             | Falso                                                           |
| No Catálogo Global      | Falso                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                    |
| Range-Lower            | \-                                                              |
| Range-Upper            | \-                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Control-Access-Right**](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------|
| ID do link                | \-                                                              |
| MAPI-Id                | \-                                                              |
| System-Only            | Falso                                                           |
| Tem valor único       | Verdadeiro                                                            |
| É indexado             | Falso                                                           |
| No Catálogo Global      | Falso                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                    |
| Range-Lower            | \-                                                              |
| Range-Upper            | \-                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Control-Access-Right**](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------|
| ID do link                | \-                                                              |
| MAPI-Id                | \-                                                              |
| System-Only            | Falso                                                           |
| Tem valor único       | Verdadeiro                                                            |
| É indexado             | Falso                                                           |
| No Catálogo Global      | Falso                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                    |
| Range-Lower            | \-                                                              |
| Range-Upper            | \-                                                              |
| Search-Flags           | 0x00000000                                                      |
| System-Flags           | 0x00000010                                                      |
| Classes usadas em        | [**Control-Access-Right**](c-controlaccessright.md)<br/> |



 

 





