---
title: Trust-Attributes atributo
description: Esse atributo armazena os atributos de confiança para um domínio confiável.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Esquema de Trust-Attributes do atributo AD
- Esquema de AD do atributo trustattributes
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645495"
---
# <a name="trust-attributes-attribute"></a>Trust-Attributes atributo

Esse atributo armazena os atributos de confiança para um domínio confiável. Os valores de atributo possíveis são os seguintes:

-   Atributo de confiança \_ \_ não \_ transitiva desabilite transitividade.
-   A \_ relação \_ \_ de confiança pai da árvore de atributos de confiança está definida como pai da árvore organizacional.
-   Confiança \_ raiz da árvore de atributos de confiança \_ \_ definida como outra raiz da árvore na floresta.
-   O \_ atributo de confiança \_ somente o \_ link confiável é válido somente para o cliente de upLevel.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Trust-Attributes                     |
| LDAP-Display-Name | trustattributes                      |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.470               |
| System-ID-GUID    | 80a67e5a-9f22-11d0-afdd-00c04fd930c9 |
| Syntax            | [**Enumeração**](s-enumeration.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | True                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | True                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | True                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | True                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | True                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | True                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | True                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | True                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | True                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| É de valor único       | True                                                 |
| É indexado             | Falso                                                |
| No catálogo global      | True                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



 

 





