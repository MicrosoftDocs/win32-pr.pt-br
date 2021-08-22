---
title: Atributo ms-DS-User-Account-Auto-Locked
description: Indica se a conta que esse atributo faz referência foi bloqueada.
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo ms-DS-User-Account-Auto-Locked
- Esquema do AD do atributo ms-DS-UserAccountAutoLocked
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1360b9169d5355ef23caf47fa56a283dc4e5267fb603aa08bd0600f126c69f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119300296"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a>Atributo ms-DS-User-Account-Auto-Locked

Indica se a conta que esse atributo faz referência foi bloqueada. True se a conta estiver bloqueada; caso contrário, False.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Auto-Locked       |
| Ldap-Display-Name | ms-DS-UserAccountAutoLocked          |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1857              |
| System-Id-Guid    | f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d |
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

No ADAM, esse atributo substitui o sinalizador [**\_ ADS UF \_ LOCKOUT**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) do [**atributo userAccountControl.**](a-useraccountcontrol.md)

 

