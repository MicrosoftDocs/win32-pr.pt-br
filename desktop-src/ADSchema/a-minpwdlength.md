---
title: Atributo Min-Pwd-Length
description: O número mínimo de caracteres que uma senha deve conter.
ms.assetid: f1bd7b0c-cb78-4b03-88fe-dbdf472dab06
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Min-Pwd-Length
- Esquema do AD do atributo minPwdLength
topic_type:
- apiref
api_name:
- Min-Pwd-Length
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b217beb1f55d37157d09f54819859af105a42d7959da511209d5e540ef238e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118687538"
---
# <a name="min-pwd-length-attribute"></a>Atributo Min-Pwd-Length

O número mínimo de caracteres que uma senha deve conter.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Min-Pwd-Length                       |
| Ldap-Display-Name | minPwdLength                         |
| Tamanho              | \-                                   |
| Privilégio de atualização  | Administrador de domínio                 |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.79                |
| System-Id-Guid    | bf9679c3-0de6-11d0-a285-00aa003049e2 |
| Sintaxe            | [**Enumeração**](s-enumeration.md) |



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
| Tem valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Tem valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Tem valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
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
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
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
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
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
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



 

 





