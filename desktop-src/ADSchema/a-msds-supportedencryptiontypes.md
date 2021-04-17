---
title: ms-DS-supported-atributo de tipos de criptografia
description: Os algoritmos de criptografia com suporte do usuário, computador ou contas de confiança. Observe que o KDC usa essas informações ao gerar um tíquete de serviço para essa conta.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- ms-DS-supported-tipo de criptografia-esquema do AD Schema
- atributo msDS-SupportedEncryptionTypes do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105769103"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a>ms-DS-supported-atributo de tipos de criptografia

Os algoritmos de criptografia com suporte do usuário, computador ou contas de confiança.

> [!Note]  
> O KDC usa essas informações ao gerar um tíquete de serviço para essa conta. Os serviços e computadores podem atualizar automaticamente esse atributo em suas respectivas contas no Active Directory e, portanto, precisam de acesso de gravação a esse atributo.

 



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-supported-tipos de criptografia     |
| LDAP-Display-Name | msDS-SupportedEncryptionTypes        |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1963              |
| System-ID-GUID    | 20119867-1d04-4ab7-9371-cfc3d5df0afd |
| Syntax            | [**Enumeração**](s-enumeration.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Falso                                                                                  |
| É de valor único       | True                                                                                   |
| É indexado             | Falso                                                                                  |
| No catálogo global      | Falso                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Falso                                                                                  |
| É de valor único       | True                                                                                   |
| É indexado             | Falso                                                                                  |
| No catálogo global      | Falso                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Falso                                                                                  |
| É de valor único       | True                                                                                   |
| É indexado             | Falso                                                                                  |
| No catálogo global      | Falso                                                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





