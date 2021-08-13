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
ms.openlocfilehash: eec2ce0ff9651350803a05b3b3bf3dda663419c9948617b706688bf78057ad72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118688483"
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
| Sintaxe            | [**Cadeia de caracteres (Teletex)**](s-string-teletex.md)                                                                               |



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
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Modelo de endereço**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Tem valor único       | True                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Modelo de endereço**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Tem valor único       | True                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Modelo de endereço**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Tem valor único       | True                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Modelo de endereço**](c-addresstemplate.md)<br/> |



 

 





