---
title: System-Only atributo
description: Um valor booliano que especifica se apenas Active Directory pode modificar a classe. Classes somente de sistema só podem ser criadas ou excluídas pelo agente do sistema de diretório.
ms.assetid: 78d2da1f-bdf1-452b-bc64-78088f3630dd
ms.tgt_platform: multiple
keywords:
- Esquema de System-Only do atributo AD
- Esquema de AD do atributo systemOnly
topic_type:
- apiref
api_name:
- System-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c28707c2cc2d9070ff639dd9c9e9d934a0a5569e32ae40b067e639e6a21e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835857"
---
# <a name="system-only-attribute"></a>System-Only atributo

Um valor booliano que especifica se apenas Active Directory pode modificar a classe. Classes somente de sistema só podem ser criadas ou excluídas pelo agente do sistema de diretório.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | System-Only                          |
| LDAP-Display-Name | systemOnly                           |
| Tamanho              | 4 bytes                              |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.170               |
| System-ID-GUID    | bf967a46-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Boolean**](s-boolean.md)         |



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
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Verdadeiro                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No catálogo global      | Falso                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Verdadeiro                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No catálogo global      | Falso                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> [**Esquema de classe**](c-classschema.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Verdadeiro                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                      |
| É indexado             | Falso                                                                                                     |
| No catálogo global      | Falso                                                                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
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
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
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
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
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
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
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
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> [**Esquema de classe**](c-classschema.md)<br/> |



 

 





