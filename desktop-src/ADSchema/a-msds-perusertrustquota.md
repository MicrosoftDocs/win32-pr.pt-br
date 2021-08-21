---
title: Atributo MS-DS-per-user-Trust-quota
description: Usado para impor uma cota por usuário para criar Trusted-Domain objetos que são autorizados pelo direito de acesso de novo controle, criar-entrada-floresta-Trust.
ms.assetid: 3b198b24-5282-4d13-8d35-88f34c11ce94
ms.tgt_platform: multiple
keywords:
- Esquema do AD de atributos do MS-DS-per-user-Trust-quota
- atributo msDS-PerUserTrustQuota do AD Schema
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fc51a6e3e3e9f3d14534487590985197ed7c97fbca8bc1042108bfcdba97530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425822"
---
# <a name="ms-ds-per-user-trust-quota-attribute"></a>Atributo MS-DS-per-user-Trust-quota

Usado para impor uma cota por usuário para criar Trusted-Domain objetos que são autorizados pelo direito de acesso de novo controle, criar-entrada-floresta-Trust. Esse atributo limita o número de objetos Trusted-Domain que podem ser criados por um único usuário não administrador.



| Entrada | Valor |
|-------------------|-------------------------------------------|
| CN                | MS-DS-por usuário-Trust-quota                |
| LDAP-Display-Name | msDS-PerUserTrustQuota                    |
| Tamanho              | \-                                        |
| Privilégio de atualização  | Administrador de domínio                      |
| Frequência de atualização  | Na criação da floresta e raramente depois disso. |
| Attribute-Id      | 1.2.840.113556.1.4.1788                   |
| System-ID-GUID    | d161adf0-ca24-4993-a3aa-8b2c981302e8      |
| Syntax            | [**Enumeração**](s-enumeration.md)      |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| É de valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Domínio Sam**](c-samdomain.md)<br/> |



 

 





