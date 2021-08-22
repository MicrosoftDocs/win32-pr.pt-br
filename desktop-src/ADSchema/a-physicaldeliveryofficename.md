---
title: atributo físico-Delivery-Office-Name
description: Contém o local do escritório no local de negócios do usuário.
ms.assetid: a6be61bf-9a9a-4b97-bdf8-894c173efadd
ms.tgt_platform: multiple
keywords:
- atributo de anúncio Physical-Delivery-Office-Name
- Esquema de AD do atributo physicalDeliveryOfficeName
topic_type:
- apiref
api_name:
- Physical-Delivery-Office-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a574c7214f18d9cef46a64885ca2855fdaf3227a9dece159458d5f1cb07d8b7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647766"
---
# <a name="physical-delivery-office-name-attribute"></a>atributo físico-Delivery-Office-Name

Contém o local do escritório no local de negócios do usuário.



| Entrada | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| CN                | físico-entrega-Office-Name                                                       |
| LDAP-Display-Name | physicalDeliveryOfficeName                                                          |
| Tamanho              | \-                                                                                  |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                              |
| Frequência de atualização  | Quando o registro do usuário é criado e sempre que o local do escritório precisa ser alterado. |
| Attribute-Id      | 2.5.4.19                                                                            |
| System-ID-GUID    | bf9679f7-0de6-11d0-a285-00aa003049e2                                                |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                         |



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
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                          |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                           |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                            |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                            |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                             |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                    |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                    |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                               |
| MAPI-Id                | 0x3A19                                                                                                           |
| System-Only            | Falso                                                                                                            |
| É de valor único       | Verdadeiro                                                                                                             |
| É indexado             | Verdadeiro                                                                                                             |
| No catálogo global      | Falso                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                    |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                    |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                    |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                    |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                    |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                    |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                    |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                    |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





