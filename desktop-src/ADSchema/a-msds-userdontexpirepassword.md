---
title: atributo ms-DS-User-is-expire-Password
description: Indica se a senha da conta que este atributo referenciará expirará.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- ms-DS-User-out-expire-esquema de AD do atributo de senha
- atributo msDS-UserDontExpirePassword do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5c0fa709f549a523d628433ee2b3aa626278e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086918"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a>atributo ms-DS-User-is-expire-Password

Indica se a senha da conta que este atributo referenciará expirará. True se a senha não expirar; caso contrário, false.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-out-expire-Password      |
| LDAP-Display-Name | msDS-UserDontExpirePassword          |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1855              |
| System-ID-GUID    | 8788193a-2925-43d9-a221-bb7fff397675 |
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

No ADAM, esse atributo substitui o sinalizador de passwd da UF do ADS que não [**\_ \_ \_ expira \_**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) o atributo [**userAccountControl**](a-useraccountcontrol.md) .

 

