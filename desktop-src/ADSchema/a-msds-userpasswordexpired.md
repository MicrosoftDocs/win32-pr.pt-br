---
title: atributo ms-DS-User-Password-Expired
description: Indica se a senha da conta a que este atributo faz referência expirou.
ms.assetid: cab4a2e8-b440-45d2-8da8-9f020ffee08c
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-User-Password-Expired
- atributo msDS-UserPasswordExpired do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Expired
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d99143c470e58d1b1cb5e0cbd7e5302618ff0a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104163664"
---
# <a name="ms-ds-user-password-expired-attribute"></a>atributo ms-DS-User-Password-Expired

Indica se a senha da conta a que este atributo faz referência expirou. True se a senha tiver expirado; caso contrário, false.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Password-Expired          |
| LDAP-Display-Name | msDS-UserPasswordExpired             |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1858              |
| System-ID-GUID    | 565c7ab5-e13e-47f6-abb5-de741806f125 |
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
| System-Flags           | 0x00000014                                                        |
| Classes usadas em        | [**ms-DS-Vinculed-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Comentários

No ADAM, esse atributo substitui o sinalizador de [**senha de UF do ADS \_ \_ \_ expirado**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) do atributo [**userAccountControl**](a-useraccountcontrol.md) .

 

