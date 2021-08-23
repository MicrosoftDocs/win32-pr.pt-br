---
title: Atributo Domain-Policy-Object
description: Referência ao objeto de política que define a política de Autoridade de Segurança Local para o domínio do host.
ms.assetid: f4f6281d-de83-48a3-9213-565e40041fc4
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Domain-Policy-Object
- Esquema do AD do atributo domainPolicyObject
topic_type:
- apiref
api_name:
- Domain-Policy-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c50a2bc131360bc318a36bee7e5715f53198a89878d1906ded480de2117084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544926"
---
# <a name="domain-policy-object-attribute"></a>Atributo Domain-Policy-Object

Referência ao objeto de política que define a política de Autoridade de Segurança Local para o domínio do host.



| Entrada | Valor |
|-------------------|-----------------------------------------|
| CN                | Domain-Policy-Object                    |
| Ldap-Display-Name | domainPolicyObject                      |
| Tamanho              | \-                                      |
| Privilégio de atualização  | \-                                      |
| Frequência de atualização  | \-                                      |
| Attribute-Id      | 1.2.840.113556.1.4.32                   |
| System-Id-Guid    | bf96795d-0de6-11d0-a285-00aa003049e2    |
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
|------------------------|---------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                  |
| MAPI-Id                | \-                                                                                                                  |
| System-Only            | Falso                                                                                                               |
| Tem valor único       | Verdadeiro                                                                                                                |
| É indexado             | Falso                                                                                                               |
| No Catálogo Global      | Falso                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                        |
| Range-Lower            | \-                                                                                                                  |
| Range-Upper            | \-                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                          |
| System-Flags           | 0x00000010                                                                                                          |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                  |
| MAPI-Id                | \-                                                                                                                  |
| System-Only            | Falso                                                                                                               |
| Tem valor único       | Verdadeiro                                                                                                                |
| É indexado             | Falso                                                                                                               |
| No Catálogo Global      | Falso                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                        |
| Range-Lower            | \-                                                                                                                  |
| Range-Upper            | \-                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                          |
| System-Flags           | 0x00000010                                                                                                          |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                  |
| MAPI-Id                | \-                                                                                                                  |
| System-Only            | Falso                                                                                                               |
| Tem valor único       | Verdadeiro                                                                                                                |
| É indexado             | Falso                                                                                                               |
| No Catálogo Global      | Falso                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                        |
| Range-Lower            | \-                                                                                                                  |
| Range-Upper            | \-                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                          |
| System-Flags           | 0x00000010                                                                                                          |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                  |
| MAPI-Id                | \-                                                                                                                  |
| System-Only            | Falso                                                                                                               |
| É de valor único       | Verdadeiro                                                                                                                |
| É indexado             | Falso                                                                                                               |
| No catálogo global      | Falso                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                        |
| Range-Lower            | \-                                                                                                                  |
| Range-Upper            | \-                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                          |
| System-Flags           | 0x00000010                                                                                                          |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                  |
| MAPI-Id                | \-                                                                                                                  |
| System-Only            | Falso                                                                                                               |
| É de valor único       | Verdadeiro                                                                                                                |
| É indexado             | Falso                                                                                                               |
| No catálogo global      | Falso                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                        |
| Range-Lower            | \-                                                                                                                  |
| Range-Upper            | \-                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                          |
| System-Flags           | 0x00000010                                                                                                          |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                  |
| MAPI-Id                | \-                                                                                                                  |
| System-Only            | Falso                                                                                                               |
| É de valor único       | Verdadeiro                                                                                                                |
| É indexado             | Falso                                                                                                               |
| No catálogo global      | Falso                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                        |
| Range-Lower            | \-                                                                                                                  |
| Range-Upper            | \-                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                          |
| System-Flags           | 0x00000010                                                                                                          |
| Classes usadas em        | [**Autoridade de certificação**](c-certificationauthority.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



 

 





