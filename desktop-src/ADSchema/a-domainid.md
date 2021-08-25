---
title: Atributo de ID de domínio
description: Referência a um domínio associado a uma autoridade de certificação.
ms.assetid: dd2f0822-cf94-485b-8d21-8954dddb81ad
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo de ID de domínio
- Esquema do AD do atributo domainID
topic_type:
- apiref
api_name:
- Domain-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae98294df75cdd2fdd69576629b87dbea8410b17d91ba525024a2a0a43ce7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925966"
---
# <a name="domain-id-attribute"></a>Atributo de ID de domínio

Referência a um domínio associado a uma autoridade de certificação.



| Entrada | Valor |
|-------------------|-----------------------------------------|
| CN                | ID de domínio                               |
| Ldap-Display-Name | domainID                                |
| Tamanho              | \-                                      |
| Privilégio de atualização  | \-                                      |
| Frequência de atualização  | \-                                      |
| Attribute-Id      | 1.2.840.113556.1.4.686                  |
| System-Id-Guid    | 963d2734-48be-11d1-a9c3-0000f80367c1    |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------|
| ID do link                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falso                                                                  |
| Tem valor único       | Verdadeiro                                                                   |
| É indexado             | Falso                                                                  |
| No Catálogo Global      | Falso                                                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------|
| ID do link                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falso                                                                  |
| Tem valor único       | Verdadeiro                                                                   |
| É indexado             | Falso                                                                  |
| No Catálogo Global      | Falso                                                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------|
| ID do link                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falso                                                                  |
| Tem valor único       | Verdadeiro                                                                   |
| É indexado             | Falso                                                                  |
| No Catálogo Global      | Falso                                                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------|
| ID do link                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falso                                                                  |
| É de valor único       | Verdadeiro                                                                   |
| É indexado             | Falso                                                                  |
| No catálogo global      | Falso                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------|
| ID do link                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falso                                                                  |
| É de valor único       | Verdadeiro                                                                   |
| É indexado             | Falso                                                                  |
| No catálogo global      | Falso                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------|
| ID do link                | \-                                                                     |
| MAPI-Id                | \-                                                                     |
| System-Only            | Falso                                                                  |
| É de valor único       | Verdadeiro                                                                   |
| É indexado             | Falso                                                                  |
| No catálogo global      | Falso                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                           |
| Range-Lower            | \-                                                                     |
| Range-Upper            | \-                                                                     |
| Search-Flags           | 0x00000000                                                             |
| System-Flags           | 0x00000010                                                             |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> |



 

 





