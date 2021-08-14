---
title: Atributo ms-DS-User-Dont-Expire-Password
description: Indica se a senha da conta que esse atributo referencia expirará.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- Ms-DS-User-Dont-Expire-Password atributo AD Schema
- Esquema do AD do atributo msDS-UserDontExpirePassword
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af661ca1317f7506e5bcdbf611010b0fe4c058d5f1e3f1e5f31b917737a6e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425426"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a>Atributo ms-DS-User-Dont-Expire-Password

Indica se a senha da conta que esse atributo referencia expirará. True se a senha não expirar; caso contrário, False.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Dont-Expire-Password      |
| Ldap-Display-Name | msDS-UserDontExpirePassword          |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1855              |
| System-Id-Guid    | 8788193a-2925-43d9-a221-bb7fff397675 |
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
| System-Flags           | 0x00000010                                                        |
| Classes usadas em        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Comentários

No ADAM, esse atributo substitui o sinalizador [**ADS \_ UF \_ DONT EXPIRE \_ \_ PASSWD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) do [**atributo userAccountControl.**](a-useraccountcontrol.md)

 

