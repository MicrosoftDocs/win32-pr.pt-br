---
title: Atributo locale-ID
description: Esse atributo contém uma lista de IDs de localidade com suporte neste aplicativo. Uma ID de localidade representa uma localização geográfica, como um país/região, cidade, município e assim por diante.
ms.assetid: 60629155-2bdf-4080-bb88-c8db749ef954
ms.tgt_platform: multiple
keywords:
- Atributo de ID de localidade esquema do AD
- atributo localeID do esquema do AD
topic_type:
- apiref
api_name:
- Locale-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9764c9c1939281501f82cbfacd60bcc6eec2f698
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086741"
---
# <a name="locale-id-attribute"></a>Atributo locale-ID

Esse atributo contém uma lista de IDs de localidade com suporte neste aplicativo. Uma ID de localidade representa uma localização geográfica, como um país/região, cidade, município e assim por diante.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------|
| CN                | ID da localidade                                                                  |
| LDAP-Display-Name | localeID                                                                   |
| Tamanho              | 4 bytes                                                                    |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                     |
| Frequência de atualização  | Quando o registro de usuário é criado e sempre que a localidade precisa ser alterada. |
| Attribute-Id      | 1.2.840.113556.1.4.58                                                      |
| System-ID-GUID    | bf9679a1-0de6-11d0-a285-00aa003049e2                                       |
| Syntax            | [**Enumeração**](s-enumeration.md)                                       |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| É de valor único       | Falso                                                                                                                                                                 |
| É indexado             | Falso                                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Classes usadas em        | [**Categoria-registro**](c-categoryregistration.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| É de valor único       | Falso                                                                                                                                                                 |
| É indexado             | Falso                                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Classes usadas em        | [**Categoria-registro**](c-categoryregistration.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| É de valor único       | Falso                                                                                                                                                                 |
| É indexado             | Falso                                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Classes usadas em        | [**Categoria-registro**](c-categoryregistration.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| É de valor único       | Falso                                                                                                                                                                 |
| É indexado             | Falso                                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Classes usadas em        | [**Categoria-registro**](c-categoryregistration.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| É de valor único       | Falso                                                                                                                                                                 |
| É indexado             | Falso                                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Classes usadas em        | [**Categoria-registro**](c-categoryregistration.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| É de valor único       | Falso                                                                                                                                                                 |
| É indexado             | Falso                                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Classes usadas em        | [**Categoria-registro**](c-categoryregistration.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





