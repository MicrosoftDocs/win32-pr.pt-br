---
title: Atributo Schema-ID-GUID
description: O identificador exclusivo de um atributo.
ms.assetid: 50f0a4b6-dded-42db-9ac5-123f2885c658
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Schema-ID-GUID
- Esquema do AD do atributo schemaIDGUID
topic_type:
- apiref
api_name:
- Schema-ID-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbf6f45b2c4518c0140eaf3188447740849ad79933d4e4eb71fe57f769f0455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837039"
---
# <a name="schema-id-guid-attribute"></a>Atributo Schema-ID-GUID

O identificador exclusivo de um atributo.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------|
| CN                | Schema-ID-GUID                                                      |
| Ldap-Display-Name | schemaIDGUID                                                        |
| Tamanho              | 16 bytes                                                            |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                                    |
| Frequência de atualização  | Esse valor é definido quando o objeto é criado e não pode ser alterado. |
| Attribute-Id      | 1.2.840.113556.1.4.148                                              |
| System-Id-Guid    | bf967923-0de6-11d0-a285-00aa003049e2                                |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)               |



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
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Verdadeiro                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No Catálogo Global      | Falso                                                                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Esquema de atributo**](c-attributeschema.md)<br/> [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Verdadeiro                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No Catálogo Global      | Falso                                                                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Esquema de atributo**](c-attributeschema.md)<br/> [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Verdadeiro                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No Catálogo Global      | Falso                                                                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Verdadeiro                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No catálogo global      | Falso                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Verdadeiro                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No catálogo global      | Falso                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Verdadeiro                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No catálogo global      | Falso                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Verdadeiro                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No catálogo global      | Falso                                                                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                              |
| Range-Lower            | 16                                                                                                        |
| Range-Upper            | 16                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Esquema de atributo**](c-attributeschema.md)<br/> [**Esquema de classe**](c-classschema.md)<br/> |



 

 





