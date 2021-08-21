---
title: Atributo ms-DS-Site-Affinity
description: O atributo ms-DS-Site-Affinity é usado pelo Gerenciador de Contas de Segurança para expansão de grupo durante a avaliação do token.
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- Atributo ms-DS-Site-Affinity Esquema do AD
- Esquema do AD do atributo msDS-Site-Affinity
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1d3fc359388f5303be808786a929840a409d29505949601b54bd9c7a8b18cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544576"
---
# <a name="ms-ds-site-affinity-attribute"></a>Atributo ms-DS-Site-Affinity

O **atributo ms-DS-Site-Affinity** é usado pelo Gerenciador de Contas de Segurança para expansão de grupo durante a avaliação do token.



| Entrada | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| CN                | ms-DS-Site-Affinity                                                                     |
| Ldap-Display-Name | msDS-Site-Affinity                                                                      |
| Tamanho              | BLOB binário de vários valores, em que cada valor é sizeof(GUID) + sizeof(LARGE \_ INTEGER). |
| Privilégio de atualização  | \-                                                                                      |
| Frequência de atualização  | Por padrão, uma vez a cada três meses.                                                     |
| Attribute-Id      | 1.2.840.113556.1.4.1443                                                                 |
| System-Id-Guid    | c17c5602-bcb7-46f0-9656-6370ca884b72                                                    |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                   |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Falso                             |
| É indexado             | Verdadeiro                              |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Falso                             |
| É indexado             | Verdadeiro                              |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Falso                             |
| É indexado             | Verdadeiro                              |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Falso                             |
| É indexado             | Verdadeiro                              |
| No catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Falso                             |
| É indexado             | Verdadeiro                              |
| No catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



 

 





