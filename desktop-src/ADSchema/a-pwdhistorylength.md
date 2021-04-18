---
title: Pwd-histórico-tamanho do atributo
description: O número de senhas antigas a serem salvas.
ms.assetid: 6440620d-9e77-411a-ab96-f8e979262bec
ms.tgt_platform: multiple
keywords:
- Pwd-histórico-tamanho do esquema de atributo do AD
- Esquema de AD do atributo pwdHistoryLength
topic_type:
- apiref
api_name:
- Pwd-History-Length
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899c486914db31dcd8a07b18c6cb6b5842e0ab00
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104369948"
---
# <a name="pwd-history-length-attribute"></a>Pwd-histórico-tamanho do atributo

O número de senhas antigas a serem salvas.



| Entrada | Valor |
|-------------------|------------------------------------------|
| CN                | Pwd-tamanho do histórico                       |
| LDAP-Display-Name | pwdHistoryLength                         |
| Tamanho              | 4 bytes                                  |
| Privilégio de atualização  | Administrador de domínio                     |
| Frequência de atualização  | Quando a política de conta precisa ser alterada. |
| Attribute-Id      | 1.2.840.113556.1.4.95                    |
| System-ID-GUID    | bf967a09-0de6-11d0-a285-00aa003049e2     |
| Syntax            | [**Enumeração**](s-enumeration.md)     |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



 

 





