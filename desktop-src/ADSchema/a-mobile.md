---
title: Telefone-Mobile-Primary
description: O número de telefone celular primário.
ms.assetid: c35fbaf1-e3f2-45df-98bd-e47ed79373ee
ms.tgt_platform: multiple
keywords:
- Telefone do AD de atributo móvel-primário
- esquema do AD do atributo móvel
topic_type:
- apiref
api_name:
- Phone-Mobile-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65002852c265c53f35abd5ff42a2fb2a74d8c0eade4c96bfc72720cdf30ba2d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118687490"
---
# <a name="phone-mobile-primary-attribute"></a>Telefone-Mobile-Primary

O número de telefone celular primário.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Telefone-Mobile-Primary                                                             |
| Ldap-Display-Name | Serviço Móvel                                                                           |
| Tamanho              | \-                                                                               |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                           |
| Frequência de atualização  | Quando o registro do usuário é criado e sempre que o número de telefone precisa ser alterado. |
| Attribute-Id      | 0.9.2342.19200300.100.1.41                                                       |
| System-Id-Guid    | f0f8ffa3-1191-11d0-a060-00aa006c33ed                                             |
| Sintaxe            | [**String(Unicode)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------|
| ID do link                | \-                                                                 |
| MAPI-Id                | 0x3A1C                                                             |
| System-Only            | Falso                                                              |
| Tem valor único       | True                                                               |
| É indexado             | Falso                                                              |
| No Catálogo Global      | Falso                                                              |
| Descritor de segurança NT | O:BAG:BAD:S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A1C                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| Tem valor único       | True                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                    |
| No Catálogo Global      | Falso                                                                                                                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A1C                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| Tem valor único       | True                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                    |
| No Catálogo Global      | Falso                                                                                                                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A1C                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| É de valor único       | True                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                    |
| No catálogo global      | Falso                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A1C                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| É de valor único       | True                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                    |
| No catálogo global      | Falso                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A1C                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| É de valor único       | True                                                                                                                                                     |
| É indexado             | Falso                                                                                                                                                    |
| No catálogo global      | Falso                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





