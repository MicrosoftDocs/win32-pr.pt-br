---
title: ms-DS-User-Account-atributo bloqueado automaticamente
description: Indica se a conta que este atributo referencia foi bloqueada.
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- ms-DS-User-Account-esquema de atributos do atributo bloqueado automaticamente
- Esquema de AD do atributo ms-DS-UserAccountAutoLocked
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6623a1b348af14fecc8dab41a44439bf2d745bf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104009856"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a>ms-DS-User-Account-atributo bloqueado automaticamente

Indica se a conta que este atributo referencia foi bloqueada. True se a conta estiver bloqueada; caso contrário, false.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Locked automaticamente       |
| LDAP-Display-Name | ms-DS-UserAccountAutoLocked          |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1857              |
| System-ID-GUID    | f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d |
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

No ADAM, esse atributo substitui o sinalizador de [**\_ \_ bloqueio da UF do ADS**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) do atributo [**userAccountControl**](a-useraccountcontrol.md) .

 

