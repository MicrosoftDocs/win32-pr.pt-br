---
title: Atributo title
description: Contém o cargo do usuário. Essa propriedade geralmente é usada para indicar o cargo formal, como Programador Sênior, em vez de classe profissional, como programador. Normalmente, ele não é usado para títulos de sufixo, como Esq. ou DDS.
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- Atributo de título Esquema do AD
- atributo title Esquema do AD
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8885a557e8fbec17d6d58d68fdea0f99039f0e09e34a8da01954dc7b4979fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645026"
---
# <a name="title-attribute-ad-schema"></a>Atributo title (Esquema do AD)

Contém o cargo do usuário. Essa propriedade geralmente é usada para indicar o cargo formal, como Programador Sênior, em vez de classe profissional, como programador. Normalmente, ele não é usado para títulos de sufixo, como Esq. ou DDS.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------|
| CN                | Título                                                                     |
| Ldap-Display-Name | título                                                                     |
| Tamanho              | \-                                                                        |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                    |
| Frequência de atualização  | Quando o registro do usuário é criado e sempre que o título precisa ser alterado. |
| Attribute-Id      | 2.5.4.12                                                                  |
| System-Id-Guid    | bf967a55-0de6-11d0-a285-00aa003049e2                                      |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                               |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Tem valor único       | Verdadeiro                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No Catálogo Global      | Falso                                                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Tem valor único       | Verdadeiro                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No Catálogo Global      | Falso                                                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Tem valor único       | Verdadeiro                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No Catálogo Global      | Falso                                                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Tem valor único       | Verdadeiro                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No Catálogo Global      | Falso                                                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Tem valor único       | Verdadeiro                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No Catálogo Global      | Falso                                                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Tem valor único       | Verdadeiro                                                                                                                            |
| É indexado             | Falso                                                                                                                           |
| No Catálogo Global      | Falso                                                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes usadas em        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Pessoa Residencial**](c-residentialperson.md)<br/> |



 

 





