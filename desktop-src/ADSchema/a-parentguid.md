---
title: Atributo pai-GUID
description: Este é um atributo construído, inventado para dar suporte ao controle DirSync. Esse atributo contém o objectGUID do pai de um objeto ao replicar a criação, renomeação ou movimentação de um objeto.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Atributo pai-GUID AD Schema
- Esquema de AD do atributo parentGUID
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825298"
---
# <a name="parent-guid-attribute"></a>Atributo pai-GUID

Este é um atributo construído, inventado para dar suporte ao controle DirSync. Esse atributo contém o objectGUID do pai de um objeto ao replicar a criação, renomeação ou movimentação de um objeto.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | GUID-pai                                           |
| LDAP-Display-Name | parentGUID                                            |
| Tamanho              | 16 bytes                                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                      |
| Frequência de atualização  | Durante a replicação                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1224                               |
| System-ID-GUID    | 2df90d74-009f-11d2-aa4c-00c04fd7d83a                  |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md) |



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
|------------------------|--------------|
| ID do link                | \-           |
| MAPI-Id                | \-           |
| System-Only            | True         |
| É de valor único       | True         |
| É indexado             | Falso        |
| No catálogo global      | Falso        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S: |
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
| System-Only            | True         |
| É de valor único       | True         |
| É indexado             | Falso        |
| No catálogo global      | Falso        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes usadas em        | \-           |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|--------------|
| ID do link                | \-           |
| MAPI-Id                | \-           |
| System-Only            | True         |
| É de valor único       | True         |
| É indexado             | Falso        |
| No catálogo global      | Falso        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S: |
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
| System-Only            | True         |
| É de valor único       | True         |
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
| System-Only            | True         |
| É de valor único       | True         |
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
| System-Only            | True         |
| É de valor único       | True         |
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
| System-Only            | True         |
| É de valor único       | True         |
| É indexado             | Falso        |
| No catálogo global      | Falso        |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes usadas em        | \-           |



 

 




