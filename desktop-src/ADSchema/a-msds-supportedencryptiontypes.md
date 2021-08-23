---
title: Atributo ms-DS-Supported-Encryption-Types
description: Os algoritmos de criptografia com suporte por contas de usuário, computador ou confiança. Observação O KDC usa essas informações ao gerar um tíquete de serviço para essa conta.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- Atributo AD Schema ms-DS-Supported-Encryption-Types
- Atributo AD Schema msDS-SupportedEncryptionTypes
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d092061dfebcea8e9a0e4f4a060010e16102108d1e2e74f05e6df2db706141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544336"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a>Atributo ms-DS-Supported-Encryption-Types

Os algoritmos de criptografia com suporte por contas de usuário, computador ou confiança.

> [!Note]  
> O KDC usa essas informações ao gerar um tíquete de serviço para essa conta. Os serviços e computadores podem atualizar automaticamente esse atributo em suas respectivas contas no Active Directory e, portanto, precisam de acesso de gravação a esse atributo.

 



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-Supported-Encryption-Types     |
| Ldap-Display-Name | msDS-SupportedEncryptionTypes        |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1963              |
| System-Id-Guid    | 20119867-1d04-4ab7-9371-cfc3d5df0afd |
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
| Tem valor único       | Verdadeiro                                                                                   |
| É indexado             | Falso                                                                                  |
| No Catálogo Global      | Falso                                                                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                           |
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
| Tem valor único       | Verdadeiro                                                                                   |
| É indexado             | Falso                                                                                  |
| No Catálogo Global      | Falso                                                                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                           |
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
| Tem valor único       | Verdadeiro                                                                                   |
| É indexado             | Falso                                                                                  |
| No Catálogo Global      | Falso                                                                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





