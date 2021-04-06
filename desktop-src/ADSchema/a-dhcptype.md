---
title: atributo de tipo DHCP
description: O tipo de servidor DHCP.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- atributo de AD Schema do tipo DHCP
- atributo dhcptype de AD Schema
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5a5a331ff7298854f4ca070799a05e2a3497f2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919332"
---
# <a name="dhcp-type-attribute"></a>atributo de tipo DHCP

O tipo de servidor DHCP. Esse atributo é definido em todos os objetos de objectClass [**dHCPClass**](c-dhcpclass.md). Seu valor define o tipo de objeto:

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| Entrada | Valor |
|-------------------|--------------------------------------------------------|
| CN                | Tipo de DHCP                                              |
| LDAP-Display-Name | dhcptype                                               |
| Tamanho              | 4 bytes                                                |
| Privilégio de atualização  | Administrador de domínio.                                  |
| Frequência de atualização  | Quando um novo servidor é adicionado ou removido da floresta. |
| Attribute-Id      | 1.2.840.113556.1.4.699                                 |
| System-ID-GUID    | 963d273b-48be-11d1-a9c3-0000f80367c1                   |
| Syntax            | [**Enumeração**](s-enumeration.md)                   |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | True                                         |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | True                                         |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | True                                         |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | True                                         |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | True                                         |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | True                                         |
| É indexado             | True                                         |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Classe DHCP**](c-dhcpclass.md)<br/> |



 

 





