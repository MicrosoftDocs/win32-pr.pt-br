---
title: ms-DS-User-Password-não-atributo obrigatório
description: Indica se uma senha é necessária para a conta que esse atributo referencia.
ms.assetid: 86779c6f-d05c-409a-afe4-99ebf7c0593e
ms.tgt_platform: multiple
keywords:
- ms-DS-User-Password-não-esquema de atributo do AD obrigatório
- Esquema de AD do atributo ms-DS-UserPasswordNotRequired
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Not-Required
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8ebb439af9a960d2dc0721940d9f4d2ab852b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087121"
---
# <a name="ms-ds-user-password-not-required-attribute"></a>ms-DS-User-Password-não-atributo obrigatório

Indica se uma senha é necessária para a conta que esse atributo referencia. True se uma senha não for necessária; caso contrário, false.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Password-não-obrigatório     |
| LDAP-Display-Name | ms-DS-UserPasswordNotRequired        |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1854              |
| System-ID-GUID    | 8f066172-a25e-4f53-8dcd-0a67d5fb883d |
| Syntax            | [**Boolean**](s-boolean.md)         |



## <a name="implementations"></a>Implementações

-   [**ADAM**](#adam)

## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------|
| ID do link                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| É de valor único       | True                                                              |
| É indexado             | Falso                                                             |
| No catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classes usadas em        | [**ms-DS-Vinculed-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Comentários

No ADAM, esse atributo substitui o sinalizador da [**\_ UF de \_ \_ NOTREQD de publicidade**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) do atributo [**userAccountControl**](a-useraccountcontrol.md) .

 

