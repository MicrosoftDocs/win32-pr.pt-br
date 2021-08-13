---
title: Atributo ms-DS-User-Encrypted-Text-Password-Allowed
description: Indica se o Active Directory armazenará a senha no formato de criptografia reversível.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- Ms-DS-User-Encrypted-Text-Password-Allowed attribute AD Schema
- ms-DS-UserEncryptedTextPasswordAllowed attribute AD Schema
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fc10b3facce4bef7cc5ff73abe9e901f67171dc2615b79c62355ac61a7c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118686997"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a>Atributo ms-DS-User-Encrypted-Text-Password-Allowed

Indica se o Active Directory armazenará a senha no formato de criptografia reversível. True se a senha for armazenada no formato de criptografia reversível; caso contrário, False.

> [!Note]  
> Esse atributo não é usado pelo [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) e só está incluído para a conclusão/paridade com userAccountControl. AD LDS não armazena senhas com criptografia reversível, independentemente do valor desse atributo em um determinado objeto ou na política de segurança do computador referente à criptografia reversível no próprio computador.

 



| Entrada | Valor |
|-------------------|--------------------------------------------|
| CN                | ms-DS-User-Encrypted-Text-Password-Allowed |
| Ldap-Display-Name | ms-DS-UserEncryptedTextPasswordAllowed     |
| Tamanho              | \-                                         |
| Privilégio de atualização  | \-                                         |
| Frequência de atualização  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.1856                    |
| System-Id-Guid    | 5a87c7f2-93c5-454c-a8c5-8cb09613292e       |
| Sintaxe            | [**Boolean**](s-boolean.md)               |



## <a name="implementations"></a>Implementações

-   [**Adam**](#adam)

## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------|
| ID do link                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Tem valor único       | True                                                              |
| É indexado             | Falso                                                             |
| No Catálogo Global      | Falso                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classes usadas em        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Comentários

No ADAM, esse atributo substitui o sinalizador [**ADS \_ UF \_ ENCRYPTED TEXT PASSWORD \_ \_ \_ ALLOWED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) do [**atributo userAccountControl.**](a-useraccountcontrol.md)

 

