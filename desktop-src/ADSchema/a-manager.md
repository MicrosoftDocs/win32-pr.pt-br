---
title: Atributo manager
description: Contém o nome diferenciado do usuário que é o gerente do usuário. O objeto de usuário do gerente contém uma propriedade directReports que contém referências a todos os objetos de usuário que têm suas propriedades de gerente definidas para esse nome diferenciado.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo manager
- esquema do AD do atributo manager
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b17f3252963e03c86b5b25a3651606a004afe672f1c8ec07f419ddff3a826
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301256"
---
# <a name="manager-attribute"></a>Atributo manager

Contém o nome diferenciado do usuário que é o gerente do usuário. O objeto de usuário do gerente contém uma propriedade directReports que contém referências a todos os objetos de usuário que têm suas propriedades de gerente definidas para esse nome diferenciado.



| Entrada | Valor |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Gerente                                                                     |
| Ldap-Display-Name | manager                                                                     |
| Tamanho              | \-                                                                          |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                      |
| Frequência de atualização  | Quando o registro do usuário é criado e sempre que o gerenciador precisa mudar. |
| Attribute-Id      | 0.9.2342.19200300.100.1.10                                                  |
| System-Id-Guid    | bf9679b5-0de6-11d0-a285-00aa003049e2                                        |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)                                     |



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
| ID do link                | 42                                                                 |
| MAPI-Id                | 0x8005                                                             |
| System-Only            | Falso                                                              |
| Tem valor único       | Verdadeiro                                                               |
| É indexado             | Falso                                                              |
| No Catálogo Global      | Verdadeiro                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000010                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Tem valor único       | Verdadeiro                                                                                                                   |
| É indexado             | Falso                                                                                                                  |
| No Catálogo Global      | Verdadeiro                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Tem valor único       | Verdadeiro                                                                                                                   |
| É indexado             | Falso                                                                                                                  |
| No Catálogo Global      | Verdadeiro                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Tem valor único       | Verdadeiro                                                                                                                   |
| É indexado             | Falso                                                                                                                  |
| No Catálogo Global      | Verdadeiro                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Tem valor único       | Verdadeiro                                                                                                                   |
| É indexado             | Falso                                                                                                                  |
| No Catálogo Global      | Verdadeiro                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID do link                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Tem valor único       | Verdadeiro                                                                                                                   |
| É indexado             | Falso                                                                                                                  |
| No Catálogo Global      | Verdadeiro                                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





