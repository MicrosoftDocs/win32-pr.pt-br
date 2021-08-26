---
title: Atributo EFSPolicy
description: A política de sistema de arquivos com criptografia.
ms.assetid: e5d5e0f8-5bce-4ada-a2ec-734532a968e9
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo EFSPolicy
- Esquema de AD do atributo eFSPolicy
topic_type:
- apiref
api_name:
- EFSPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee6ae775e74ffd72009d9ac45e9c8926a37186362533cdb478ffb11f694d0ca0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054166"
---
# <a name="efspolicy-attribute"></a>Atributo EFSPolicy

A política de sistema de arquivos com criptografia.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | EFSPolicy                                             |
| LDAP-Display-Name | eFSPolicy                                             |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | \-                                                    |
| Frequência de atualização  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.268                                |
| System-ID-GUID    | 8e4eb2ec-4712-11d0-a1a0-00c04fd930c9                  |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                              |
| MAPI-Id                | \-                                                                                              |
| System-Only            | Falso                                                                                           |
| É de valor único       | Falso                                                                                           |
| É indexado             | Falso                                                                                           |
| No catálogo global      | Falso                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                    |
| Range-Lower            | \-                                                                                              |
| Range-Upper            | \-                                                                                              |
| Search-Flags           | 0x00000000                                                                                      |
| System-Flags           | 0x00000010                                                                                      |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                              |
| MAPI-Id                | \-                                                                                              |
| System-Only            | Falso                                                                                           |
| É de valor único       | Falso                                                                                           |
| É indexado             | Falso                                                                                           |
| No catálogo global      | Falso                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                    |
| Range-Lower            | \-                                                                                              |
| Range-Upper            | \-                                                                                              |
| Search-Flags           | 0x00000000                                                                                      |
| System-Flags           | 0x00000010                                                                                      |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                              |
| MAPI-Id                | \-                                                                                              |
| System-Only            | Falso                                                                                           |
| É de valor único       | Falso                                                                                           |
| É indexado             | Falso                                                                                           |
| No catálogo global      | Falso                                                                                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                    |
| Range-Lower            | \-                                                                                              |
| Range-Upper            | \-                                                                                              |
| Search-Flags           | 0x00000000                                                                                      |
| System-Flags           | 0x00000010                                                                                      |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                              |
| MAPI-Id                | \-                                                                                              |
| System-Only            | Falso                                                                                           |
| Tem valor único       | Falso                                                                                           |
| É indexado             | Falso                                                                                           |
| No Catálogo Global      | Falso                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                    |
| Range-Lower            | \-                                                                                              |
| Range-Upper            | \-                                                                                              |
| Search-Flags           | 0x00000000                                                                                      |
| System-Flags           | 0x00000010                                                                                      |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                              |
| MAPI-Id                | \-                                                                                              |
| System-Only            | Falso                                                                                           |
| Tem valor único       | Falso                                                                                           |
| É indexado             | Falso                                                                                           |
| No Catálogo Global      | Falso                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                    |
| Range-Lower            | \-                                                                                              |
| Range-Upper            | \-                                                                                              |
| Search-Flags           | 0x00000000                                                                                      |
| System-Flags           | 0x00000010                                                                                      |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                              |
| MAPI-Id                | \-                                                                                              |
| System-Only            | Falso                                                                                           |
| Tem valor único       | Falso                                                                                           |
| É indexado             | Falso                                                                                           |
| No Catálogo Global      | Falso                                                                                           |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                    |
| Range-Lower            | \-                                                                                              |
| Range-Upper            | \-                                                                                              |
| Search-Flags           | 0x00000000                                                                                      |
| System-Flags           | 0x00000010                                                                                      |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> |



 

 





