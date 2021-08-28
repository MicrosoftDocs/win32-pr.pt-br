---
title: Atributo Pwd-History-Length
description: O número de senhas antigas a salvar.
ms.assetid: 6440620d-9e77-411a-ab96-f8e979262bec
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Pwd-History-Length
- Esquema do AD do atributo pwdHistoryLength
topic_type:
- apiref
api_name:
- Pwd-History-Length
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9c2c5011b2c497e8b6ed69015dd7dd16fbd2bf979d199674dd6ccbb2a67b81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960095"
---
# <a name="pwd-history-length-attribute"></a>Atributo Pwd-History-Length

O número de senhas antigas a salvar.



| Entrada | Valor |
|-------------------|------------------------------------------|
| CN                | Pwd-History-Length                       |
| Ldap-Display-Name | pwdHistoryLength                         |
| Tamanho              | 4 bytes                                  |
| Privilégio de atualização  | Administrador de domínio                     |
| Frequência de atualização  | Quando a política de conta precisa ser mudada. |
| Attribute-Id      | 1.2.840.113556.1.4.95                    |
| System-Id-Guid    | bf967a09-0de6-11d0-a285-00aa003049e2     |
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
| Tem valor único       | Verdadeiro                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Tem valor único       | Verdadeiro                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Tem valor único       | Verdadeiro                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
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
| É de valor único       | Verdadeiro                                                                                                                                                  |
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
| É de valor único       | Verdadeiro                                                                                                                                                  |
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
| É de valor único       | Verdadeiro                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



 

 





