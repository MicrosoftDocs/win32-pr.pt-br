---
title: atributo de caixa de Office
description: O número da caixa Post Office deste objeto.
ms.assetid: e782271a-2f79-42af-9c62-5723917a6f47
ms.tgt_platform: multiple
keywords:
- esquema do AD de atributo de caixa Office
- Esquema de AD do atributo postOfficeBox
topic_type:
- apiref
api_name:
- Post-Office-Box
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f86bd2f1ae357485c00af2da52cf26fa4b5d8f67d1020fe9fa3e204a48a9e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065972"
---
# <a name="post-office-box-attribute"></a>atributo de caixa de Office

O número da caixa Post Office deste objeto.



| Entrada | Valor |
|-------------------|-----------------------------------------------------------------------------|
| CN                | caixa de Office                                                             |
| LDAP-Display-Name | postOfficeBox                                                               |
| Tamanho              | \-                                                                          |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                      |
| Frequência de atualização  | Quando o registro do usuário é criado e sempre que o endereço precisa ser alterado. |
| Attribute-Id      | 2.5.4.18                                                                    |
| System-ID-GUID    | bf9679fb-0de6-11d0-a285-00aa003049e2                                        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                 |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                          |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                           |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                           |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                           |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                               |
| MAPI-Id                | 0x3A2B                                                                                                           |
| System-Only            | Falso                                                                                                            |
| Tem valor único       | Falso                                                                                                            |
| É indexado             | Falso                                                                                                            |
| No Catálogo Global      | Falso                                                                                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 40                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Tem valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| No Catálogo Global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Tem valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| No Catálogo Global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Tem valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| No Catálogo Global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Tem valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| No Catálogo Global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





