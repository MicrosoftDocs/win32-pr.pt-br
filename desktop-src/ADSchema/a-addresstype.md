---
title: Address-Type atributo
description: Uma cadeia de caracteres que descreve o formato do endereço do usuário. Os tipos de endereço são mapeados para formatos de endereço. Ou seja, examinando o tipo de endereço de um destinatário, os aplicativos cliente podem determinar como formatar um endereço apropriado para o destinatário.
ms.assetid: ff39b1f5-1844-43e9-a4a5-2b5f7c396f34
ms.tgt_platform: multiple
keywords:
- Esquema de Address-Type do atributo AD
- Esquema do atributo do ADtype
topic_type:
- apiref
api_name:
- Address-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ece3b396d619272c616ff1a959d01efb64ccd46
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105752983"
---
# <a name="address-type-attribute"></a>Address-Type atributo

Uma cadeia de caracteres que descreve o formato do endereço do usuário. Os tipos de endereço são mapeados para formatos de endereço. Ou seja, examinando o tipo de endereço de um destinatário, os aplicativos cliente podem determinar como formatar um endereço apropriado para o destinatário.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
| CN                | Address-Type                                                                                                              |
| LDAP-Display-Name | addressType                                                                                                               |
| Tamanho              | Tipos de endereço: 3COM, ATT, CCMAIL, COMPUSERVE, EX, FAX, MSFAX, MCI, MHS, MS, MSA, MSN, PROFs, SMTP, SNADS, TELEX, X400, X500 |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                                                                                          |
| Frequência de atualização  | Defina quando o objeto é criado.                                                                                           |
| Attribute-Id      | 1.2.840.113556.1.2.350                                                                                                    |
| System-ID-GUID    | 5fd42464-1262-11d0-a060-00aa006c33ed                                                                                      |
| Syntax            | [**Cadeia de caracteres (Teletex)**](s-string-teletex.md)                                                                               |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| É de valor único       | True                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Endereço-modelo**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| É de valor único       | True                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Endereço-modelo**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| É de valor único       | True                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Endereço-modelo**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| É de valor único       | True                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Endereço-modelo**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| É de valor único       | True                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Endereço-modelo**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| É de valor único       | True                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Endereço-modelo**](c-addresstemplate.md)<br/> |



 

 





