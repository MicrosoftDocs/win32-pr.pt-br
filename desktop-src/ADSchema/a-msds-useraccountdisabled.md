---
title: Atributo ms-DS-User-Account-Disabled
description: Indica se uma conta está desabilitada ou habilitada.
ms.assetid: 5d6ced7b-ca0f-4afa-b394-e61e80454f3d
ms.tgt_platform: multiple
keywords:
- Ms-DS-User-Account-Disabled attribute AD Schema
- Esquema do AD do atributo msDS-UserAccountDisabled
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Disabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f0744cd835fab641de4f4d3386304a342fe3902fcf1a67b3367dc15b7ee68f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544136"
---
# <a name="ms-ds-user-account-disabled-attribute"></a>Atributo ms-DS-User-Account-Disabled

Indica se uma conta está desabilitada ou habilitada. True se a conta estiver desabilitada; caso contrário, False.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Disabled          |
| Ldap-Display-Name | msDS-UserAccountDisabled             |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1853              |
| System-Id-Guid    | 7c708658-7372-4211-b22b-13a45ffd1d61 |
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

No ADAM, esse atributo substitui o sinalizador [**ADS \_ UF \_ ACCOUNTDISABLE**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) do [**atributo userAccountControl.**](a-useraccountcontrol.md)

 

