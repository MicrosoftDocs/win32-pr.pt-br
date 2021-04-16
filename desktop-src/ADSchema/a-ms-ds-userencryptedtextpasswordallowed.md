---
title: ms-DS-User-Encrypted-texto-Password-atributo permitido
description: Indica se Active Directory irá armazenar a senha no formato de criptografia reversível.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- ms-DS-User-Encrypted-text-password-esquema de atributo do AD permitido
- Esquema de AD do atributo ms-DS-UserEncryptedTextPasswordAllowed
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456133"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a>ms-DS-User-Encrypted-texto-Password-atributo permitido

Indica se Active Directory irá armazenar a senha no formato de criptografia reversível. True se a senha for armazenada no formato de criptografia reversível; caso contrário, false.

> [!Note]  
> Esse atributo não é usado pelo [Serviços AD LDS](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) e é incluído apenas para fins de integridade/paridade com userAccountControl. AD LDS não armazena senhas com criptografia reversível, independentemente do valor desse atributo em qualquer objeto ou política de segurança de computador pertencente à criptografia reversível no próprio computador.

 



| Entrada | Valor |
|-------------------|--------------------------------------------|
| CN                | ms-DS-User-Encrypted-texto-senha-permitido |
| LDAP-Display-Name | ms-DS-UserEncryptedTextPasswordAllowed     |
| Tamanho              | \-                                         |
| Privilégio de atualização  | \-                                         |
| Frequência de atualização  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.1856                    |
| System-ID-GUID    | 5a87c7f2-93c5-454c-a8c5-8cb09613292e       |
| Syntax            | [**Boolean**](s-boolean.md)               |



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

No ADAM, esse atributo substitui o [**sinalizador \_ \_ permitido pela \_ \_ senha de \_ texto criptografado da UF do ADS**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) do atributo [**userAccountControl**](a-useraccountcontrol.md) .

 

