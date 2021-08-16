---
title: Destination-Indicator atributo
description: Isso faz parte da especificação X.500 e não é usado pelo NTDS.
ms.assetid: 3c8c8df1-25d7-4ef6-bec4-66b12318b3f0
ms.tgt_platform: multiple
keywords:
- Destination-Indicator atributo AD Schema
- Esquema do AD do atributo destinationIndicator
topic_type:
- apiref
api_name:
- Destination-Indicator
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e9869296d9d1d09400d2ff0ba68953acb107e62ed6d58a716f3d8d6afc504
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508996"
---
# <a name="destination-indicator-attribute"></a>Destination-Indicator atributo

Isso faz parte da especificação X.500 e não é usado pelo NTDS.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Destination-Indicator                |
| Ldap-Display-Name | destinationIndicator                 |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 2.5.4.27                             |
| System-Id-Guid    | bf967951-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**String(IA5)**](s-string-ia5.md)  |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                          |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                           |
| Tem valor único       | Falso                                                                                                                                                                                                                                                                                                           |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                           |
| No Catálogo Global      | Falso                                                                                                                                                                                                                                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Tem valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| No Catálogo Global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                               |
| MAPI-Id                | 0x8070                                                                                                           |
| System-Only            | Falso                                                                                                            |
| Tem valor único       | Falso                                                                                                            |
| É indexado             | Falso                                                                                                            |
| No catálogo global      | Falso                                                                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes usadas em        | [**Organização**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Função organizacional**](c-organizationalrole.md)<br/> [**Unidade organizacional**](c-organizationalunit.md)<br/> [**Residencial-pessoa**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





