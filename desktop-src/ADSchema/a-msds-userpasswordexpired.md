---
title: Atributo ms-DS-User-Password-Expired
description: Indica se a senha da conta que esse atributo faz referência expirou.
ms.assetid: cab4a2e8-b440-45d2-8da8-9f020ffee08c
ms.tgt_platform: multiple
keywords:
- Ms-DS-User-Password-Expired Attribute AD Schema
- MsDS-UserPassword Schema do AD do atributoExpired
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Expired
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a187f9d0b2be2feeca076d7c7eef82a34ca5827a9d07c76b2d711a5196f84ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425352"
---
# <a name="ms-ds-user-password-expired-attribute"></a>Atributo ms-DS-User-Password-Expired

Indica se a senha da conta que esse atributo faz referência expirou. True se a senha tiver expirado; caso contrário, False.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Password-Expired          |
| Ldap-Display-Name | msDS-UserPasswordExpired             |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1858              |
| System-Id-Guid    | 565c7ab5-e13e-47f6-abb5-de741806f125 |
| Syntax            | [**Boolean**](s-boolean.md)         |



## <a name="implementations"></a>Implementações

-   [**Adam**](#adam)

## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------|
| ID do link                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Tem valor único       | Verdadeiro                                                              |
| É indexado             | Falso                                                             |
| No Catálogo Global      | Falso                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000014                                                        |
| Classes usadas em        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Comentários

No ADAM, esse atributo substitui o sinalizador [**ADS \_ UF PASSWORD \_ \_ EXPIRED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) do [**atributo userAccountControl.**](a-useraccountcontrol.md)

 

