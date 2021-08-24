---
title: Network-Address atributo
description: O endereço TCP/IP de um segmento de rede. Também chamado de endereço de sub-rede.
ms.assetid: caccb00f-8418-43b8-87c7-7ccb7e2ee51d
ms.tgt_platform: multiple
keywords:
- Network-Address atributo AD Schema
- networkAddress attribute AD Schema
topic_type:
- apiref
api_name:
- Network-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aecb62701350c0a954a23dc403a314331920810b0b6778f90099c600ca738a60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704756"
---
# <a name="network-address-attribute"></a>Network-Address atributo

O endereço TCP/IP de um segmento de rede. Também chamado de endereço de sub-rede.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Network-Address                             |
| Ldap-Display-Name | networkAddress                              |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.2.459                      |
| System-Id-Guid    | bf9679d9-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Teletex)**](s-string-teletex.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                             |
| Tem valor único       | Falso                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                             |
| No Catálogo Global      | Falso                                                                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Classe DHCP**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                             |
| Tem valor único       | Falso                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                             |
| No Catálogo Global      | Falso                                                                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Classe DHCP**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | 0x8170                                   |
| System-Only            | Falso                                    |
| Tem valor único       | Falso                                    |
| É indexado             | Falso                                    |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | 0                                        |
| Range-Upper            | 256                                      |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000000                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                             |
| É de valor único       | Falso                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                             |
| No catálogo global      | Falso                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Classe DHCP**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                             |
| É de valor único       | Falso                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                             |
| No catálogo global      | Falso                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Classe DHCP**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                             |
| É de valor único       | Falso                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                             |
| No catálogo global      | Falso                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Classe DHCP**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                |
| MAPI-Id                | 0x8170                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                             |
| É de valor único       | Falso                                                                                                                                                             |
| É indexado             | Falso                                                                                                                                                             |
| No catálogo global      | Falso                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                      |
| Range-Lower            | 0                                                                                                                                                                 |
| Range-Upper            | 256                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                        |
| System-Flags           | 0x00000000                                                                                                                                                        |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Classe DHCP**](c-dhcpclass.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





