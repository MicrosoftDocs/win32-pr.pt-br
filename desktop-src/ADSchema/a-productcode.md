---
title: Product-Code atributo
description: Esse atributo contém um identificador exclusivo para um aplicativo para uma versão específica do produto, representado como um GUID de cadeia de caracteres, por exemplo, \ 0034; 12345678-1234-1234-1234-123456789012 \ 0034;.
ms.assetid: 1fb50a4c-1a6a-4231-a6b2-92f6bc4a1ead
ms.tgt_platform: multiple
keywords:
- Esquema de Product-Code do atributo AD
- Esquema de AD do atributo productCode
topic_type:
- apiref
api_name:
- Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d527263787b68fbe7ab328fa5d1e91a0b7b9dd2385b29d5e6b0bb4a9fedc0400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681744"
---
# <a name="product-code-attribute"></a>Product-Code atributo

Esse atributo contém um identificador exclusivo para um aplicativo para uma versão específica do produto, representado como um GUID de cadeia de caracteres, por exemplo " {12345678-1234-1234-1234-123456789012} ". As letras usadas neste GUID devem estar em letras maiúsculas. Essa ID deve variar para diferentes versões e idiomas.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Product-Code                                          |
| LDAP-Display-Name | productCode                                           |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | \-                                                    |
| Frequência de atualização  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.818                                |
| System-ID-GUID    | d9e18317-8939-11d1-aebc-0000f80367c1                  |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | Verdadeiro                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | Verdadeiro                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | Verdadeiro                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | Verdadeiro                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | Verdadeiro                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | Verdadeiro                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



 

 





