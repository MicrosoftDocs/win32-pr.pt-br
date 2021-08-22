---
title: Atributo PARENT-GUID
description: Esse é um atributo construído, com suporte para o controle DirSync. Esse atributo contém o objectGuid do pai de um objeto ao replicar a criação, a renomeação ou a movimentação de um objeto.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo PARENT-GUID
- Esquema do AD do atributo parentGUID
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f42ba5aedc73f04d8967b84bcfbff39c54ce0dbcdf769e48a747ffa0d3e8c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119325426"
---
# <a name="parent-guid-attribute"></a>Atributo PARENT-GUID

Esse é um atributo construído, com suporte para o controle DirSync. Esse atributo contém o objectGuid do pai de um objeto ao replicar a criação, a renomeação ou a movimentação de um objeto.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | GUID pai                                           |
| Ldap-Display-Name | parentGUID                                            |
| Tamanho              | 16 bytes                                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                      |
| Frequência de atualização  | Durante a replicação                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1224                               |
| System-Id-Guid    | 2df90d74-009f-11d2-aa4c-00c04fd7d83a                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|--------------|
| ID do link                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Verdadeiro         |
| Tem valor único       | Verdadeiro         |
| É indexado             | Falso        |
| No Catálogo Global      | Falso        |
| Descritor de segurança NT | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes usadas em        | \-           |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------|
| ID do link                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Verdadeiro         |
| Tem valor único       | Verdadeiro         |
| É indexado             | Falso        |
| No Catálogo Global      | Falso        |
| Descritor de segurança NT | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes usadas em        | \-           |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|--------------|
| ID do link                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Verdadeiro         |
| Tem valor único       | Verdadeiro         |
| É indexado             | Falso        |
| No Catálogo Global      | Falso        |
| Descritor de segurança NT | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes usadas em        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------|
| ID do link                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Verdadeiro         |
| É de valor único       | Verdadeiro         |
| É indexado             | Falso        |
| No catálogo global      | Falso        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes usadas em        | \-           |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------|
| ID do link                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Verdadeiro         |
| É de valor único       | Verdadeiro         |
| É indexado             | Falso        |
| No catálogo global      | Falso        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes usadas em        | \-           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------|
| ID do link                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Verdadeiro         |
| É de valor único       | Verdadeiro         |
| É indexado             | Falso        |
| No catálogo global      | Falso        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes usadas em        | \-           |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------|
| ID do link                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Verdadeiro         |
| É de valor único       | Verdadeiro         |
| É indexado             | Falso        |
| No catálogo global      | Falso        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes usadas em        | \-           |



 

 




